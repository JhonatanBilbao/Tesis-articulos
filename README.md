# IDS-INT: Transformer-Based Intrusion Detection System

Este repositorio contiene una implementación experimental del modelo **IDS-INT** (Intrusion Detection System using Transformer-based Transfer Learning for Imbalanced Network Traffic), propuesto por **Farhan Ullah et al. (2024)**. El código ha sido adaptado para ejecutarse en **Google Colab** y emplea modelos basados en **Transformer**, balanceo con **SMOTE**, y una arquitectura híbrida **CNN-LSTM** para la detección de ataques en tráfico de red.

## 📄 Artículo base

**Título:** IDS-INT: Intrusion detection system using transformer-based transfer learning for imbalanced network traffic  
**Autores:** Farhan Ullah, Shamsher Ullah, Gautam Srivastava, Jerry Chun-Wei Lin  
**Publicado en:** Digital Communications and Networks, Vol. 10, 2024, pp. 190–204  
**DOI:** [10.1016/j.dcan.2023.03.008](https://doi.org/10.1016/j.dcan.2023.03.008)

## 🧪 Descripción del proyecto

Este proyecto implementa un sistema inteligente de detección de intrusos utilizando:

- **Transformers (BERT large)** para el aprendizaje de representaciones semánticas del tráfico de red.
- **SMOTE (Synthetic Minority Oversampling Technique)** para balancear clases minoritarias.
- **CNN-LSTM** como arquitectura de clasificación de ataques en tráfico balanceado.
- Interpretabilidad del modelo con **LIME** y **SHAP**.

## 🧠 Dataset utilizados

Los modelos han sido evaluados sobre tres conjuntos de datos estándar:

- [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
- [CIC-IDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)
- [NSL-KDD](https://www.unb.ca/cic/datasets/nsl.html)

> ⚠️ Los datasets no están incluidos en este repositorio. Deben descargarse manualmente desde sus fuentes oficiales.

## ⚙️ Requisitos

La implementación fue desarrollada y probada en **Google Colab**. Las bibliotecas principales incluyen:

- `transformers`
- `scikit-learn`
- `imblearn`
- `tensorflow` / `keras`
- `lime`
- `shap`
- `pandas`, `numpy`, `matplotlib`, etc.

Para ejecutar en Google Colab, no es necesaria instalación previa. Basta con abrir el archivo `.ipynb` y seguir las celdas.

## 🚀 Ejecución

1. Abrir el notebook en [Google Colab](https://colab.research.google.com/).
2. Subir los datasets necesarios o montar Google Drive.
3. Ejecutar las celdas en orden, asegurándose de ajustar rutas si es necesario.
4. Visualizar los resultados y las explicaciones mediante LIME y SHAP.

## 📈 Resultados esperados

Los modelos alcanzan altos niveles de precisión, según el artículo original:

- **UNSW-NB15:** ~99.2% Accuracy con CNN-LSTM
- **CIC-IDS2017:** ~99.3% Accuracy
- **NSL-KDD:** ~98.5% Accuracy

## 🧩 Estructura del código

- Preprocesamiento del dataset y etiquetado
- Aplicación de SMOTE para balanceo
- Entrenamiento con modelo CNN-LSTM
- Evaluación con métricas: Accuracy, F1-score, Recall, Precision
- Interpretación del modelo (Explainable AI)

## 📝 Cita recomendada

Si utilizas este código en tu investigación, por favor cita el artículo original:

> Ullah, F., Ullah, S., Srivastava, G., & Lin, J. C.-W. (2024). IDS-INT: Intrusion detection system using transformer-based transfer learning for imbalanced network traffic. *Digital Communications and Networks*, 10, 190–204. https://doi.org/10.1016/j.dcan.2023.03.008

## 📬 Contacto

Para dudas o comentarios sobre esta implementación, puedes crear un issue o adaptar el código bajo la licencia correspondiente.

---

**Licencia:** Uso académico basado en la licencia del artículo original ([CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)).


