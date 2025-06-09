# RUIDS - Robust Unsupervised Intrusion Detection System

Este proyecto implementa el sistema RUIDS (Robust Unsupervised Intrusion Detection System) propuesto en el artículo:

**"Robust unsupervised network intrusion detection with self-supervised masked context reconstruction"** (Computers & Security, 2023).

## 📌 Descripción

RUIDS es un sistema de detección de intrusos en red sin supervisión que combina:

- Aprendizaje auto-supervisado usando Transformers.
- Reconstrucción de contexto enmascarado para tolerancia a datos anómalos.
- Detección de anomalías a través de la pérdida de reconstrucción.

## ⚙️ Componentes del modelo

- `TransformerBlock`: Extrae relaciones temporales entre muestras dentro de un contexto.
- `Encoder`: Embebe las muestras originales en un espacio latente.
- `Decoder`: Reconstruye las muestras enmascaradas para calcular el error.
- `Pérdida`: MSE sobre atributos enmascarados (no necesita etiquetas).

## 📁 Estructura del código

- `train_ruids`: Entrena el modelo usando sólo datos normales.
- `evaluate`: Evalúa el modelo en datos normales + anómalos usando AUC, F1, Accuracy.

## 🔬 Dataset utilizado

Este ejemplo usa un dataset sintético (usando `make_classification`). Puedes reemplazarlo por:

- [KDDCUP99](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)
- [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
- [CICIDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)

Formato esperado:

- Datos en formato NumPy o CSV.
- Todos los atributos deben ser numéricos (usa one-hot o codificación).

## 🚀 Instrucciones de uso

1. Abrir el notebook de Google Colab.
2. Ejecutar todas las celdas para:
   - Preprocesar los datos.
   - Entrenar el modelo sobre datos normales.
   - Evaluar el rendimiento sobre datos normales + anómalos.

## 📊 Métricas utilizadas

- `AUC`: Área bajo la curva ROC.
- `F1-score`: Medida balanceada entre precisión y recall.
- `Accuracy`: Proporción de muestras correctamente clasificadas.

## 🧪 Ejemplo de ejecución

```python
model = RUIDS(input_dim=X.shape[1]).to(device)
train_ruids(model, X_train)
evaluate(model, X_test_full, y_test_full)
```

## 🛠️ Requisitos

- Python ≥ 3.7
- PyTorch ≥ 1.10
- Scikit-learn

## 📄 Artículo original
Wang, W., Jian, S., Tan, Y., Wu, Q., & Huang, C. (2023). Robust unsupervised network intrusion detection with self-supervised masked context reconstruction. *Computers & Security*, 128, 103131. https://doi.org/10.1016/j.cose.2023.103131

## 📬 Contacto
Implementado por: **[Tu Nombre Aquí]**

Para fines académicos y experimentales. No garantiza rendimiento en producción sin ajustes.

---

**¡Explora, ajusta y adapta este modelo a tu conjunto de datos real!**

