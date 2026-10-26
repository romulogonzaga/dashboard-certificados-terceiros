# Dashboard de certificados NR — Terceiros

Painel HTML para importar uma planilha Excel e acompanhar certificados de treinamentos de empresas terceirizadas.

## Como usar

1. Baixe o repositório e abra `index.html` no navegador.
2. Clique em **Continuar** e selecione a planilha `.xlsx` ou `.xls`.
3. Use os filtros de período, empresa e treinamento.
4. Use **Baixar PDF** para exportar o painel.

As bibliotecas estão incluídas no HTML, permitindo uso sem internet. A planilha é processada no navegador e não é enviada para um servidor. É necessário importá-la novamente ao reabrir o painel.

## Estrutura da planilha

O importador procura as colunas **TREINAMENTO**, **DATA FINAL**, **DATA DE ASSINATURA** e **EMPRESA** nas primeiras 50 linhas das abas. Datas podem ser datas nativas do Excel ou texto em `dd/mm/aaaa` e `aaaa-mm-dd`. Linhas sem data final válida são ignoradas e contabilizadas na mensagem de importação. Datas de assinatura inválidas interrompem a importação com uma mensagem de erro.

## Indicadores

- Registros de treinamento no período de conclusão selecionado.
- Percentual e quantidade de certificados com data de assinatura.
- Quantidade de empresas atendidas.
- Prazo médio entre conclusão e assinatura.
- Registros e certificados assinados por mês de conclusão.
- Dez empresas com mais certificados pendentes.

Cada linha válida é contada como um registro. O painel não elimina duplicidades nem identifica turmas únicas.

## Dependências incluídas

- Chart.js 4.4.1
- SheetJS XLSX 0.18.5
- html2pdf.js 0.10.1

Os avisos de licença das bibliotecas permanecem no arquivo distribuído. O painel mantém os elementos visuais e fontes incorporadas da versão original.
