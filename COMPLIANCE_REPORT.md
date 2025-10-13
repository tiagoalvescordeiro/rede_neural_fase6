# Verificação do Repositório — Fase 6

Esta verificação confronta os artefatos presentes no repositório com as exigências descritas no enunciado das Entregas 1 e 2 da Fase 6.

## Sumário Executivo

| Critério | Situação | Evidências | Observações |
| --- | --- | --- | --- |
| Organização do dataset (mínimo de 40 imagens por classe e splits 32/4/4) | Atende | Arquivo `fase6_dataset.zip` possui 32 imagens de treino, 4 de validação e 4 de teste para cada classe (`circle`, `square`). | Estrutura atende ao enunciado, porém o dataset está compactado; o README não explica como utilizá-lo. |
| Notebook Jupyter/Colab nomeado corretamente | Atende | `TiagoAlves_rm561791_pbl_fase6.ipynb`. | Nome segue o padrão com nome, RM e fase. |
| Notebook executado com saídas presentes | Não atende | Todas as células de código estão com `execution_count = null` e sem outputs. | É necessário executar o notebook antes da entrega. |
| Código comentado e descrito em Markdown | Parcial | Há introdução e conclusões no notebook. | Faltam descrições detalhadas das etapas intermediárias e comentários contextualizando os resultados gerados. |
| README com documentação introdutória | Parcial | README apresenta visão geral e instruções. | Não inclui link para o notebook, nem link do vídeo demonstrativo exigido. |
| Vídeo demonstrativo (até 5 minutos, link no README) | Não atende | README contém placeholder `INSERIR_LINK_DO_VÍDEO_AQUI`. | Incluir URL do vídeo não listado conforme orientação. |
| Integração do notebook ao GitHub | Parcial | Notebook está presente. | Ausência de execução impede a validação completa do passo a passo. |

## Detalhes por Critério

### Dataset
O arquivo `fase6_dataset.zip` contém a estrutura `images/` e `labels/` com 32 imagens de treino, 4 de validação e 4 de teste para cada classe (`square` e `circle`), totalizando 80 imagens, atendendo ao mínimo estabelecido. 【ddb003†L1-L14】

### Notebook
O notebook `TiagoAlves_rm561791_pbl_fase6.ipynb` está nomeado conforme solicitado, porém todas as células de código permanecem sem execução (`execution_count = null`) e não há saídas registradas. 【F:TiagoAlves_rm561791_pbl_fase6.ipynb†L22-L325】

### Documentação
O README oferece visão geral e instruções, mas falta a integração solicitada com o notebook (link direto) e com o vídeo demonstrativo — há apenas um placeholder indicando onde o link deveria estar. 【F:README.md†L1-L66】

### Vídeo
Como o README mantém o placeholder `INSERIR_LINK_DO_VÍDEO_AQUI`, conclui-se que o link obrigatório para o vídeo de até 5 minutos não foi disponibilizado. 【F:README.md†L44-L57】

## Recomendações

1. Executar completamente o notebook antes da entrega, garantindo que todas as células tenham `execution_count` válido e exibam saídas relevantes.
2. Complementar as células Markdown com análises dos resultados (métricas, comparações entre modelos) conforme solicitado no enunciado.
3. Atualizar o README com links diretos para:
   - Notebook (GitHub/Colab);
   - Vídeo demonstrativo não listado no YouTube.
4. Explicar no README como utilizar o dataset compactado (`fase6_dataset.zip`) ou disponibilizar as pastas já organizadas.

Com essas correções, o repositório ficará alinhado às exigências do projeto Fase 6.
