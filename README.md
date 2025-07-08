# Proyecto RecSys UC 2025 - 1 MIND dataset

Este repositorio contiene los scripts utilizados para el Proyecto RecSys UC 2025 - 1 MIND dataset. 

En estos scrips se trabaja con `behaviors.tsv` y `news.tsv` que pueden ser descargados desde https://msnews.github.io/ en la sección de MIND-small, específicamente el Training Set.

En algunos archivos está implementado el uso de embeddings preentrenados de https://nlp.stanford.edu/projects/glove/, específicamente se debe descargar el archivo `glove.6B.zip` y utilizar el archivo `glove.6B.300d.txt`. En caso de que no se quiera ocupar, se debe fijar `False` la variable `glove` definida en la celda correspondiente.

Cada archivo corresponde a:

- `LSTUR.ipynb`: modelo LSTUR entrenado con el dataset small.

- `FastFormerNRMS old batches.ipynb`: modelo NRMS + FastFormer implementando con la división de batches antigua.

- `NRMS old batches.ipynb`: modelo NRMS implementando con la división de batches antigua. Para poder correrlo se debe tener los archivos `behaviors_sample.tsv` y `news_sample.tsv` (archivos presentes en el repo). Se puede ejecutar con glove.

- `NRMSFastFormer new batches.ipynb`: modelo NRMS + FastFormer implementando con la división de batches nueva. Se puede ejecutar con glove. Este cuadernillo fue ejecutado con el dataset small.

- `nrms_fastformer_best.pt`: mejor modelo entrenado de `NRMSFastFormer new batches.ipynb`. Cabe recalcar que no está implementada la forma de cargar este archivo.

- `NRMSFastFormer_new_batches_word2vec.ipynb`: modelo entrenado con todo el dataset large y embedding preentrenados word2vec.

- `Best FastFormerNRMS.ipynb`: mejor modelo entrenado con todo el dataset large y embedding preentrenados GloVe. Además posee el cálculo de métricas de novedad y diversidad. También tiene ejemplos de recomendación.
