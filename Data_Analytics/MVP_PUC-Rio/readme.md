# [Análise Exploratória do Crime no Rio de Janeiro]([./Data_Analytics/MVP_PUC-Rio/MVP_Análise_de_Dados_e_Boas_Práticas_(Bruno_Reis).ipynb]) 
**Bruno Reis · MVP — Análise de Dados e Boas Práticas · PUC-Rio**

---

## Sobre o projeto

Este trabalho investiga as tendências históricas do crime na cidade do Rio de Janeiro entre 2003 e 2026, cruzando dados de ocorrências policiais com estimativas populacionais por delegacia. O objetivo é entender não apenas *quanto* crime ocorre, mas *onde*, *quando* e em *quais categorias* — e se esse crescimento acompanha ou supera o crescimento da população.

Os dados são públicos e provêm do [ISP-RJ (Instituto de Segurança Pública)](https://www.ispdados.rj.gov.br):

- **Estatísticas de segurança:** série histórica mensal por CISP desde janeiro de 2003
- **População:** estimativas anuais por CISP de 2000 a 2022

---

## Hipóteses investigadas

1. O crime no Rio proliferou acima do crescimento populacional? Onde? Em quais categorias?
2. Há localidades *outlier* em que o crime cresceu além da média da sua zona?
3. Há tipos de crime *outlier* que cresceram além da média de suas categorias?
4. Os tipos de crime mais frequentes divergem significativamente entre zonas?

---

## Estrutura dos dados

Após o pré-processamento, o dataset cobre **apenas o município do Rio de Janeiro** e conta com **10.124 instâncias** (uma por CISP por mês) e 66 atributos. As ocorrências foram agrupadas em cinco categorias:

| Categoria | O que inclui |
|---|---|
| **Violentos** | Homicídio doloso, lesão corporal, latrocínio, estupro, intervenções policiais e outros |
| **Trânsito** | Homicídio culposo e lesão corporal culposa em contexto de trânsito |
| **Roubos** | Roubo a transeunte, de veículo, de carga, em coletivo, bancário e outros |
| **Furtos** | Furto de veículo, de pessoa, em coletivo, de celular e outros |
| **Outros** | Sequestro, extorsão, estelionato e similares |

As CISPs foram associadas a cinco zonas geográficas da cidade — **Norte, Sul, Oeste, Central e Sudoeste** — usando a tabela territorial oficial do ISP, complementada com um histórico de desmembramentos e mudanças de AISP para resolver valores faltantes.

---

## Principais descobertas

### O crime não cresceu uniformemente

Ao indexar todas as categorias com base 100 em 2003 e comparar com o crescimento populacional por zona, emerge um padrão claro de divergência: o crime cresceu acima da população em praticamente todas as zonas, mas com ritmos e perfis distintos.

### Crimes violentos recuaram; outros avançaram

A análise das médias anuais por categoria revela uma tendência que não é intuitiva:

- **Crimes violentos, de trânsito e roubos** apresentaram **queda** ao longo do período — com destaque para o roubo de veículos, que caiu pela metade, e para os crimes violentos, que recuaram de forma consistente após meados dos anos 2000.
- **Furtos** cresceram, com o furto de celular registrando dois saltos expressivos no período pós-pandemia.
- **Outros crimes** foram a categoria de maior crescimento absoluto — impulsionada quase que exclusivamente pelo **estelionato**, que saiu de valores residuais e tornou-se um dos crimes mais frequentes da cidade.

Esse padrão sugere uma possível **migração do perfil criminal**: da violência física e do roubo para a fraude, acompanhando tendências de digitalização e urbanização.

### Assimetria espacial nos crimes violentos

Os dados desagregados por zona mostram que **lesão corporal dolosa** é, de longe, o crime mais frequente em todas as regiões — e que a Zona Oeste concentra as maiores médias tanto de homicídio doloso quanto de lesão corporal. A Zona Sul apresenta consistentemente os menores índices de violência, mesmo quando normalizado por 100 mil habitantes.

### O dado bruto distorce; o per capita revela

Um achado metodológico relevante: comparar contagens absolutas entre zonas é enganoso, pois a Zona Norte e a Zona Oeste têm populações muito maiores que a Zona Sul e a Zona Central. A taxa por 100 mil habitantes muda significativamente o ranking entre zonas em várias categorias — reforçando a importância da normalização populacional para qualquer conclusão sobre criminalidade regional.

---

## Limitações conhecidas

- Os dados de população só chegam até **2022**, enquanto os registros de crime vão até 2026. As análises per capita estão, portanto, restritas a esse período.
- Alguns tipos de crime só passaram a ser registrados em datas intermediárias do período (feminicídio a partir de 2024, roubo e furto de bicicleta a partir de 2014, drogas a partir de 2006), o que impede comparações históricas completas para essas subcategorias.
- Treze CISPs da capital não possuíam unidade territorial cadastrada na tabela oficial do ISP. A maior parte foi recuperada via histórico de desmembramentos; uma (CISP 45) não pôde ser resolvida automaticamente.

---

## Próximos passos

- Responder formalmente as hipóteses 2, 3 e 4 com visualizações e testes estatísticos
- Identificar CISPs e tipos de crime *outlier* dentro de cada zona
- Construir modelo preditivo de regressão para projetar tendências por zona e categoria
- Incorporar dados populacionais estimados para 2023–2026 via interpolação ou projeção

---

## Reprodução

```bash
# Dependências
pip install pandas numpy matplotlib seaborn scikit-learn

# Os datasets são carregados diretamente das URLs públicas no início do notebook.
# Não é necessário baixar nada manualmente.
```

**Notebook:** `MVP_-_Análise_de_Dados_e_Boas_Práticas__Bruno_Reis_.ipynb`


## Notebooks
* [MVP_Análise_de_Dados_e_Boas_Práticas_(Bruno_Reis)]
