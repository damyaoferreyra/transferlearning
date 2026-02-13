# transferlearning
Este projeto é um Classificador de Imagens em Tempo Real que utiliza Inteligência Artificial para identificar objetos, animais e cenários em fotografias.

# Image Classifier com MobileNetV2 📸

Este repositório contém um script em Python para classificação de imagens utilizando o modelo **MobileNetV2**. O projeto utiliza aprendizado de transferência (Transfer Learning) com pesos pré-treinados na base de dados **ImageNet**, sendo capaz de identificar 1.000 categorias de objetos diferentes.

## 🚀 Funcionalidades

* Carregamento do modelo pré-treinado **MobileNetV2**.
* Processamento e redimensionamento automático de imagens para $224 \times 224$ pixels.
* Predição de objetos com exibição da probabilidade de acerto.
* Visualização da imagem testada utilizando `matplotlib`.

## 🛠️ Tecnologias Utilizadas

* **Python 3.x**
* **TensorFlow / Keras:** Para o motor de Deep Learning.
* **NumPy:** Para manipulação de arrays e tensores.
* **Matplotlib:** Para exibição visual dos resultados.

## 📋 Pré-requisitos

Antes de executar o código, instale as bibliotecas necessárias:

```bash
pip install tensorflow numpy matplotlib
```
## 💻 Como Executar

    Prepare o Ambiente: Certifique-se de que a imagem que deseja testar está no caminho correto (ex: /content/images/gato03.jpg).

    O Código: O script realiza o carregamento dos pesos (weights='imagenet') e define a camada de saída (include_top=True).

    Execução:
    Python

    # Exemplo de chamada da função
    identificar_imagem('caminho/da/sua/foto.jpg')

## 🧠 Detalhes do Processamento Técnico

Para que a rede neural compreenda a imagem, o script realiza as seguintes etapas matemáticas:

    Redimensionamento: A imagem é convertida para 224×224 pixels.

    Criação de Batch: Adiciona-se uma dimensão extra, transformando o array em (1,224,224,3).

    Normalização: Os valores dos pixels (0-255) são mapeados para o intervalo [−1,1] através da função preprocess_input.

    Inferência: O modelo processa os dados e o decode_predictions converte o vetor de probabilidades final no nome da categoria (ex: "Egyptian cat").
