# Ynnovar Financeiro

Sistema de acompanhamento financeiro e contábil da Ynnovar, construído a partir da
planilha Controle Financeiro. App Laravel separado do site institucional, com painel
Filament restrito à diretoria.

## Por que app separado

O site institucional é público e recebe upload de currículo. Se o financeiro morasse
no mesmo app e no mesmo banco, uma falha ali passaria a expor folha de pagamento.
Mesmo VPS, banco próprio, subdomínio próprio.

## Criando o projeto

```bash
composer create-project laravel/laravel ynnovar-financeiro
cd ynnovar-financeiro

composer require filament/filament
php artisan filament:install --panels

composer require maatwebsite/excel
```

Depois copie `app/`, `database/migrations/` e `database/seeders/` deste pacote por cima
do projeto recém-criado.

```bash
php artisan migrate
php artisan db:seed
php artisan make:filament-user
```

## O modelo, em uma frase

A planilha tem quinze abas, mas é um livro de lançamentos mais um plano de contas.
Todo o resto — DRE, totais de fixo e variável, custo operacional — é agrupamento.

### Tabelas

| Tabela | Papel |
| --- | --- |
| `contas` | Plano de contas em árvore. Só folha recebe lançamento. |
| `lancamentos` | O livro. Uma linha por movimento, de qualquer natureza. |
| `centros_custo` | Sede e os postos: Florinda, Alphaville, Mondubim, Conjunto Ceará. |
| `clientes`, `contratos` | Receita recorrente, com dia de faturamento e vigência. |
| `socios` | Igor, Roberto e Amanda. |
| `importacoes`, `importacao_linhas` | Cada importação e a linha crua que a originou. |
| `regras_classificacao` | O de-para entre o texto da planilha e o plano de contas. |

### Três decisões que valem explicar

**Valor é sempre positivo.** O sinal vem do grupo da conta, via
`GrupoDre::sinal()`. Evita o problema que a planilha tem, de número negativo
formatado de um jeito que esconde o sinal.

**Aporte de sócio não é resultado.** O grupo `patrimonio` devolve sinal zero, então
aporte nunca entra no cálculo do resultado operacional. Era exatamente isso que a
linha "Valor final" da planilha misturava: em agosto ela mostra R$ 42.019,14
positivo quando a operação fechou o mês com R$ 5.258,08 de prejuízo.

**`aporte_id` liga a despesa ao aporte que a bancou.** Quando o Igor paga R$ 600 de
fechadura do próprio bolso, o valor aparece duas vezes na planilha: como aporte e
como despesa administrativa. Não é duplicidade — o aporte financia, a despesa
consome. Sem esse campo, o importador acharia que é linha repetida e deduplicaria
errado.

## Importação

Idempotente por competência: reimportar setembro apaga e regrava só setembro.
Os lançamentos de origem `planilha` são soft-deletados antes de regravar; os de
origem `manual` nunca são tocados. É o que permite a migração gradual — quando
alguém começar a lançar direto no sistema, os dois convivem na mesma tabela.

Cada linha importada guarda o payload cru em `importacao_linhas.payload`, para
auditar quando o total não bater com a DRE da planilha.

## O que ainda não existe

- Serviço de importação do `.xlsx` e a fila de revisão
- Resources e widgets do Filament
- Papéis e permissões (folha por colaborador precisa ficar em área restrita)
- Testes

## Folha de pagamento

A aba Previsões tem nome completo, salário e encargos de cada colaborador. Isso não
entra nas tabelas deste pacote. Quando entrar, vai em tabela própria, com permissão
própria, fora do painel que a diretoria abre em reunião.
