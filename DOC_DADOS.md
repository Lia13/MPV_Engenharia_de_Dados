# Documentação dos Dados - Acidentes de Trânsito PRF 2021

## 1. Origem
- **Fonte Primária**: Portal de Dados Abertos da PRF
- **Método de Obtenção**: Download direto manual
- **Arquivo Original**: `si_bol_2021.csv`

## 2. Licenciamento
```text
Dados disponibilizados sob a Lei de Acesso à Informação (12.527/2011)
Permitido uso para fins acadêmicos e de pesquisa
```

## 3. Dicionário de Campos
| Nome no CSV | Nome Transformado | Tipo | Descrição |
|-------------|-------------------|------|-----------|
| DATA HORA_BOLETIM | data_hora_boletim | timestamp | Data e hora do acidente |
| TIPO_ACIDENTE | tipo_acidente | string | Código do tipo de acidente |

## 4. Problemas e Tratamentos
- **Problema**: Datas em formato inconsistente
- **Solução**: Conversão com `to_timestamp()`
- **Problema**: Campos com encoding incorreto
- **Solução**: Ajuste com `ISO-8859-1`
