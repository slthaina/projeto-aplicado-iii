# Sistema de Recomendação de Artigos Científicos sobre Sustentabilidade

Projeto desenvolvido para a disciplina Projeto Aplicado III utilizando técnicas de Processamento de Linguagem Natural (PLN) e filtragem por conteúdo para recomendação de artigos científicos na área de sustentabilidade.

---

## Objetivo

O objetivo deste projeto é desenvolver um sistema capaz de recomendar artigos científicos semanticamente relacionados a partir de títulos e resumos acadêmicos coletados automaticamente via API OpenAlex.

O sistema busca auxiliar estudantes e pesquisadores na exploração de literatura científica relacionada a mudanças climáticas, energia renovável, biodiversidade e sustentabilidade ambiental.

---

## Tecnologias Utilizadas

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* Requests
* OpenAlex API

---

## Metodologia

O pipeline do sistema foi desenvolvido nas seguintes etapas:

### 1. Coleta de Dados

Coleta automática de artigos científicos utilizando a API OpenAlex.

Consultas temáticas utilizadas:

* Climate change
* Sustainability
* Environmental science
* Renewable energy
* Biodiversity
* Deforestation
* Greenhouse gas
* Ocean acidification
* Water scarcity
* Wildfire

---

### 2. Pré-processamento Textual

* Conversão para minúsculas
* Remoção de caracteres especiais
* Remoção de stopwords
* Limpeza textual com expressões regulares

---

### 3. Filtragem Temática

Filtragem baseada em palavras-chave organizadas em:

* termos fortes;
* termos médios.

A filtragem teve como objetivo garantir maior aderência temática ao domínio ambiental.

---

### 4. Vetorização TF-IDF

Representação vetorial dos textos utilizando TF-IDF com:

* n-gramas;
* ponderação maior para títulos;
* normalização L2.

---

### 5. Similaridade de Cosseno

Cálculo da similaridade entre artigos científicos utilizando similaridade de cosseno sobre a matriz TF-IDF normalizada.

---

### 6. Sistema de Recomendação

Recomendação de artigos semanticamente relacionados a partir:

* de título parcial;
* índice do artigo;
* similaridade textual.

---

## Corpus Utilizado

* 1000 artigos coletados inicialmente
* 569 artigos após filtragem temática
* Publicações entre 2020 e 2024

---

## Resultados

O sistema apresentou melhores resultados em subtemas bem representados no corpus, como:

* energia renovável;
* mudanças climáticas;
* biodiversidade.

A matriz TF-IDF final foi composta por:

* 569 artigos;
* 5000 features textuais.

A similaridade média observada foi aproximadamente:

* 0.0333

Os resultados indicam um corpus heterogêneo composto por múltiplos subtemas ambientais.

---

## Estrutura do Repositório

```text
projeto-aplicado-iii/
│
├── notebooks/
├── datasets/
├── imagens/
├── documentacao/
├── videos/
├── README.md
└── requirements.txt
```

---

## Conteúdo das Pastas

### notebooks/

Notebook principal desenvolvido no Google Colab.

### datasets/

Datasets bruto e filtrado utilizados no projeto.

### imagens/

Gráficos, heatmaps, histogramas e visualizações utilizadas na análise dos resultados.

### documentacao/

Artigo final do projeto em PDF.

### videos/

Links dos vídeos de apresentação e demonstração do sistema.

---

## Execução

Instale as dependências:

```bash
pip install -r requirements.txt
```

Execute o notebook principal localizado em:

```text
notebooks/pipeline_openalex_v3.ipynb
```

---

## Trabalhos Futuros

Como possíveis melhorias futuras:

* utilização de embeddings semânticos;
* adoção de modelos transformer;
* expansão do corpus;
* avaliação quantitativa com métricas padronizadas de recomendação.

---

## Autor

Thaina Silva Leite

Projeto Aplicado III
