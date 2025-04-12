# Análise de Acidentes Rodoviários - PRF 2021

## 📌 Objetivo do Trabalho

Este projeto tem como objetivo **identificar padrões e fatores de risco** em acidentes rodoviários através da construção de um pipeline de dados na nuvem, utilizando a plataforma Databricks. Os resultados visam subsidiar políticas públicas de prevenção e segurança viária.

### Questões de Pesquisa:
*Qual a distribuição temporal dos acidentes (hora, dia da semana, tipo de dia)?*
Objetiva entender em que períodos os acidentes ocorrem com mais frequência, buscando padrões sazonais e horários críticos.

*Quais são os tipos de acidentes mais frequentes e com maior taxa de mortalidade?*
Investiga quais modalidades de acidentes ocorrem com mais frequência e quais estão mais associadas a desfechos fatais.

*Como fatores como condições climáticas e tipo de pavimento influenciam os acidentes?*
Avalia se o clima (ex.: chuva, sol) e o tipo de pavimento estão relacionados com a frequência ou gravidade dos acidentes.

*Existe alguma região com incidência significativamente maior de acidentes?*
Identifica possíveis áreas críticas na cidade, com concentração elevada de registros.

*Quais combinações de fatores estão mais associadas a vítimas fatais?*
Analisa a relação entre múltiplas variáveis (como horário, clima, tipo de acidente, etc.) e a ocorrência de mortes.

*Qual a proporção de acidentes com vítimas que ocorrem em locais não sinalizados?*
Busca entender a importância da sinalização viária e sua ausência em locais com registro de vítimas.

## 🛠️ Metodologia

### Fluxo de Dados
```mermaid
graph LR
    A[Fonte PRF] --> B[Extract]
    B --> C[Transform]
    C --> D[Load]
    D --> E[Análise]
    E --> F[Visualização]
```

### Tecnologias Utilizadas
- **Plataforma**: Databricks (Community Edition)
- **Formato de Armazenamento**: Delta Lake
- **Linguagens**: PySpark, SQL
- **Visualização**: Matplotlib, Seaborn

## 📂 Estrutura do Projeto

### Principais Tabelas
| Nome | Tipo | Descrição |
|------|------|-----------|
| `acidentes_prf_2021_clean` | Delta | Dados tratados completos |
| `acidentes_2021` | View | Camada simplificada para análise |

### Arquivos Importantes
- `CATALOGO_DADOS.md`: Catálogo completo de campos
- `EVIDENCIAS.md`: Capturas dos campos visuais fora do notebook.
- `MPV engenharia de Dados.ipynb`: Notebook com todas as etapas e documentação.


## 📊 Resultados Esperados

- Identificação de **horários e trechos críticos**
- Análise de **padrões sazonais**
- Relação entre **condições ambientais** e gravidade dos acidentes
- Sugestões para **campanhas de prevenção** direcionadas

## 📝 Licença e Atribuição

- **Fonte dos Dados**: [Dados Gov - Relação de ocorrências de acidentes de trânsito com vítima]([https://dados.gov.br/dados/conjuntos-dados/relacao-de-ocorrencias-de-acidentes-de-transito-com-vitima](https://dados.gov.br/dados/conjuntos-dados/relacao-de-ocorrencias-de-acidentes-de-transito-com-vitima))
- **Licença**: [Dados Abertos](http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2011/lei/l12527.htm)
- **Citação**: "Dados de acidentes rodoviários 2021 - PRF Brasil"

> ℹ️ Este projeto foi desenvolvido como trabalho acadêmico para a disciplina de Engenharia de Dados.
