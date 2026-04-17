# Calculadora de Precificacao 3D

SPA estatica para calcular preco final de impressao 3D com:

- Custo de material
- Custo de energia
- Custo de mao de obra
- Custo de depreciacao de maquina
- Taxa de falha/seguranca
- Margem de lucro

## Como usar localmente

Como e um projeto estatico, basta abrir o arquivo `index.html` no navegador.

## Publicar no GitHub Pages

1. Crie um repositorio no GitHub e envie os arquivos (`index.html` e `README.md`).
2. No GitHub, abra `Settings` > `Pages`.
3. Em `Build and deployment`, selecione `Deploy from a branch`.
4. Em `Branch`, selecione `main` e pasta `/ (root)`.
5. Salve e aguarde a URL publica ser gerada.

## Formula aplicada

- Custo Material = (Preco Rolo / Peso Rolo) \* Peso Peca
- Custo Energia = (Potencia Watts / 1000) _ Tempo Horas _ Valor kWh
- Custo Mao de Obra = (Valor Hora / 60) \* Tempo Setup
- Custo Depreciacao = (Valor Maquina / Vida Util Horas) \* Tempo Horas
- Total = (Material + Energia + Mao de Obra + Depreciacao) _ (1 + Taxa Falha) _ (1 + Margem Lucro)
