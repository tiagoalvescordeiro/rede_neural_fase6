# Fase 6 — Projeto de Visão Computacional (YOLOv5, Baseline e CNN)

Este repositório contém a implementação da **Fase 6** do projeto de IA da FIAP para o grupo `rede_neural_fase6`. O objetivo é demonstrar o potencial de sistemas de visão computacional, comparando diferentes abordagens de detecção e classificação de objetos.

## Visão Geral

A cliente fictícia **FarmTech Solutions** deseja entender, na prática, como a visão computacional pode auxiliar em seus novos serviços para além do agronegócio. Como desenvolvedor(a) da empresa, você demonstra um modelo capaz de detectar dois objetos de interesse (classe A e classe B) utilizando **YOLOv5** e compara esse desempenho com abordagens alternativas. 

### Abordagens implementadas

1. **YOLOv5 customizado** — Treinado do zero para identificar as classes A e B com 30 e 60 épocas. 
2. **YOLOv5 pré‑treinado** (baseline zero‑shot) — Executado diretamente nas imagens de teste, sem ajuste, para servir de controle.
3. **CNN do zero** — Classificador binário de imagens que distingue entre as classes A e B, sem detecção de caixas.

## Estrutura do Projeto

- `TiagoAlves_rm561791_pbl_fase6.ipynb`: notebook principal com todo o passo a passo (montar Drive, preparar dataset, treinar, avaliar e comparar).
- `dataset/`: gerado pelo notebook após copiar as imagens do Google Drive e organizar os splits em `train/`, `val/` e `test/`.
- `dataset_cls/`: estrutura auxiliar para a CNN do zero (pastas por classe). 
- `yolov5/`: repositório clonado automaticamente no notebook para treinar e rodar inferências.
- `runs/`: diretórios criados pelo YOLOv5 com logs, pesos e imagens de predição.

## Passo a passo rápido

1. **Clone este repositório no Colab** ou importe o notebook diretamente no Colab.
2. **Monte o Google Drive** na primeira célula e ajuste as variáveis `ORIGEM_IMAGENS_A`, `ORIGEM_IMAGENS_B` (e, se já tiver rótulos YOLO, `ORIGEM_LABELS_A`, `ORIGEM_LABELS_B`) para apontar para suas pastas de imagens.
3. Execute a célula para **copiar as imagens** e gerar o `dataset.yaml`. Certifique-se de que possui pelo menos 40 imagens por classe (80 no total).
4. Prossiga com a instalação do YOLOv5 e treine os modelos de 30 e 60 épocas. 
5. Compare as métricas com a célula de análise e realize a **inferência** no conjunto de teste para obter exemplos visuais.
6. Rode o **baseline zero‑shot** para notar a diferença quando não há customização.
7. Execute a seção de **CNN do zero** para comparar a acurácia da classificação pura.

## Tabela de resultados (exemplo)

| Modelo                         | mAP/Acc (inserir depois) | Tempo de treino (s) | Tempo de inferência (ms/imagem) | Observações |
|-------------------------------|-------------------------|---------------------|---------------------------------|------------|
| **YOLOv5 customizado (30 ep)** | —                       | —                   | —                               | Ajuste fino para A/B |
| **YOLOv5 customizado (60 ep)** | —                       | —                   | —                               | Mais épocas, melhor mAP? |
| **YOLOv5 baseline**           | —                       | ~0                  | —                               | Não reconhece A/B |
| **CNN do zero**               | —                       | —                   | —                               | Classificação binária |

Substitua os valores acima após rodar o notebook. Utilize as imagens de predição (`runs/predict/...`) para ilustrar no relatório e no vídeo.

## Vídeo demonstrativo

Grave um vídeo de até **5 minutos** mostrando: 

1. Preparação do dataset e explicação das classes A e B;
2. Treinamento com 30 e 60 épocas e comparação de métricas;
3. Resultados de teste com o melhor modelo (imagens com bounding boxes);
4. Baseline YOLOv5 pré‑treinado e discussão sobre o baixo desempenho;
5. Classificador CNN do zero e comparação geral;
6. Principais conclusões e limitações.

Inclua o link do vídeo (modo *não listado*) aqui:

`[Vídeo Demonstração](INSERIR_LINK_DO_VÍDEO_AQUI)`

## Conclusões

- O modelo **YOLOv5 customizado** é capaz de detectar com boa precisão os objetos escolhidos, desde que haja quantidade suficiente de imagens rotuladas no treino. Aumentar o número de épocas costuma melhorar a mAP, mas atenção ao tempo de treinamento.
- O **baseline** (modelo pré‑treinado) serve como controle: como as classes A/B provavelmente não existem no conjunto COCO, ele falha em detectá-las, reforçando a importância da customização.
- A **CNN do zero** pode alcançar alta acurácia para classificar entre A e B, porém não fornece a localização do objeto na imagem.
- Para melhorar ainda mais, recomenda-se ampliar o dataset, diversificar ângulos/iluminações e considerar técnicas de *data augmentation*. 

Este README é um guia introdutório; para detalhes completos, consulte o notebook e os comentários dentro do código.
