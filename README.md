# RUIDS - Robust Unsupervised Intrusion Detection System

Este proyecto implementa el modelo RUIDS descrito en el artículo *"Robust unsupervised network intrusion detection with self-supervised masked context reconstruction"* (Computers & Security, 2023).

RUIDS combina aprendizaje auto-supervisado con transformers y reconstrucción de contexto enmascarado para detectar intrusiones en redes sin necesidad de datos etiquetados.

---

## 📂 Contenido
- `ruids_colab_impl.py`: Notebook listo para ejecutar en Google Colab.
- Carga y preprocesamiento de datos
- Entrenamiento del modelo RUIDS
- Evaluación de detección de intrusiones

---

## ⚙️ Requisitos
- Python 3.8+
- PyTorch >= 1.10
- Scikit-learn
- Google Colab (opcional, recomendado)

Puedes instalar dependencias con:
```bash
pip install torch scikit-learn
