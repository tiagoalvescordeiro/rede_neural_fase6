# Projeto Fase 6 – Rede Neural YOLO e Visão Computacional

Este repositório contém a solução inicial do **Projeto Fase 6** da disciplina de IA da FIAP. O objetivo geral é desenvolver um sistema de visão computacional baseado na família YOLO, criar um dataset de duas classes, treinar o modelo com diferentes quantidades de épocas e comparar os resultados. Além disso, são propostas extensões (“Ir Além”) com ESP32-CAM e Transfer Learning.

## Conteúdo do repositório

- **`TiagoAlves_rm561791_pbl_fase6.ipynb`** – notebook Jupyter/Colab com o passo a passo do projeto. Nele você encontrará a geração do dataset sintético (círculos vermelhos e quadrados azuis), a configuração do arquivo `dataset.yaml`, orientações para instalação do YOLOv5 no Google Colab, comandos de treinamento com 30 e 60 épocas e seções para avaliação e conclusões. Abra o notebook no Colab para executar as células de código.
- **`fase6_dataset/`** – diretório contendo o dataset sintético com 80 imagens (64 para treino, 8 para validação e 8 para teste) e os respectivos arquivos de rótulo em formato YOLO. Este dataset serve como exemplo de preparação; você pode substituir por um conjunto de imagens real conforme os requisitos do enunciado.
- **`dataset.yaml`** – arquivo de configuração que mapeia as pastas de treino, validação e teste do dataset e define as classes (círculo e quadrado). Esse arquivo será utilizado pelo script de treinamento do YOLOv5.

## Como utilizar

1. **Clonar ou baixar este repositório.**
2. **Abrir o notebook no Google Colab** (recomendado) e executar todas as células. O notebook apresenta comentários em português explicando cada etapa.
3. **Treinar o modelo** com os comandos de treinamento fornecidos. Ajuste o número de épocas conforme desejado (por exemplo, 30 e 60) e observe as métricas geradas ao final do treinamento (`precision`, `recall` e `mAP`).
4. **Avaliar e comparar** os resultados das execuções com diferentes parâmetros. Registre suas conclusões nas células de markdown do notebook.

> **Obs.:** este repositório é um guia inicial. Para cumprir integralmente os requisitos da Fase 6, substitua o dataset sintético por um conjunto de imagens real (no mínimo 40 imagens de um objeto A e 40 imagens de um objeto B), realize a anotação com o [Make Sense AI](https://makesense.ai) e treine o modelo YOLOv5 conforme os passos descritos no notebook e no material de apoio da FIAP【35347222857509†L870-L977】.

## Vídeo demonstrativo

Grave um vídeo curto (até 5 minutos) demonstrando o funcionamento do seu modelo. No vídeo você pode mostrar a geração do dataset, o treinamento, a detecção em imagens de teste e comentar os resultados. Faça upload para o YouTube como “não listado” e insira o link nesta seção.

## Referências

- Material de apoio da Fase 6: guias sobre preparação de datasets e treinamento de modelos YOLO, incluindo exemplos de comandos de clonagem, instalação de requisitos e execução do treinamento【35347222857509†L870-L977】.
- Ultralytics YOLOv5: [https://github.com/ultralytics/yolov5](https://github.com/ultralytics/yolov5)

