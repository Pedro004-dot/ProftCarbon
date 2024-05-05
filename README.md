# Classificador de Vegetação via Imagens de Satélite

## Descrição

Este projeto utiliza o ambiente Google Colab e a API do Google Earth Engine (GEE) para processar e analisar imagens do satélite Sentinel-2. O objetivo principal é classificar os pixels de uma série histórica de imagens de uma fazenda agropecuária, calculando índices de vegetação. Esses dados são utilizados para contabilidade de emissão de carbono, contribuindo para estudos ambientais e de sustentabilidade na agricultura.

## Tecnologias Utilizadas

•⁠  ⁠*Ambiente de Desenvolvimento:* Google Colab
•⁠  ⁠*API:* Google Earth Engine (GEE)
•⁠  ⁠*Linguagem de Programação:* Python
•⁠  ⁠*Método de Classificação:* Random Forest

## Como Configurar e Executar

### Pré-Requisitos

•⁠  ⁠Conta Google para acesso ao Google Colab.
•⁠  ⁠Acesso à API do Google Earth Engine.

### Configuração

1.⁠ ⁠Acesse o Google Colab e crie um novo notebook.
2.⁠ ⁠Certifique-se de estar autenticado no Google Earth Engine:
   ⁠ python
   import ee
   ee.Authenticate()
   ee.Initialize()
    ⁠

### Execução

1.⁠ ⁠Importe as bibliotecas necessárias:
   ⁠ python
   import ee
   from sklearn.ensemble import RandomForestClassifier
    ⁠

2.⁠ ⁠Carregue as imagens do Sentinel-2 usando GEE:
   ⁠ python
   collection = ee.ImageCollection('COPERNICUS/S2').filterDate('2020-01-01', '2020-12-31').filterBounds(ee.Geometry.Point(-52, -12))
    ⁠

3.⁠ ⁠Calcule os índices de vegetação e prepare os dados para o modelo Random Forest.

4.⁠ ⁠Treine o modelo de Random Forest e classifique os pixels.

### Nota
As etapas de cálculo de índices de vegetação e treinamento do modelo podem variar dependendo das especificidades dos dados e do objetivo do estudo. Consulte a documentação específica para detalhes adicionais.

## Contribuição

Para contribuir com este projeto, por favor, envie um pull request ou abra uma issue para discussão das modificações propostas.


## Contato

Para mais informações, entre em contato através do e-mail: pedro.gustavo6565@gmail(mailto:SeuEmail@exemplo.com).

---

Esse template cobre as principais informações que você deve incluir no README. Certifique-se de personalizar o conteúdo de acordo com as especificidades do seu projeto e adicione qualquer outra informação relevante que acredite ser necessária.
