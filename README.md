# Inteligencia Artificial (IA)

¡Bienvenido/a al repositorio de la materia de Inteligencia Artificial! 🤖✨

Este repos está pensado para organizar trabajos prácticos, notebooks y pequeños scripts de ejemplo utilizados durante la cursada. Aquí encontrarás material reproducible, instrucciones claras para ejecutar los ejercicios y una guía rápida del contenido.

---

## 🗂️ Estructura del proyecto

```
/IA
├── README.md                         # Este archivo: guía y documentación general
├── main.py                           # Script base de ejemplo (hello world / boilerplate)
└── tp2_Juan_Manuel_Aidar_2025.ipynb  # Notebook del TP2 (2025)
```

---

## 🎯 Objetivos de la materia / repo
- Familiarizarse con conceptos fundamentales de IA y aprendizaje automático.
- Practicar el flujo de trabajo reproducible con notebooks (Jupyter) y Python.
- Documentar resultados, decisiones de modelado y conclusiones.
- Consolidar buenas prácticas (entornos, dependencias, versionado y claridad de código).

---

## 🚀 Cómo ejecutar

### 1) Requisitos
- Python 3.10+ (recomendado)
- Jupyter Notebook o JupyterLab (para abrir .ipynb)
- Paquetes comunes para IA/DS (según el TP):
  - numpy, pandas, matplotlib, scikit-learn, seaborn, etc.

Sugerencia: usar un entorno virtual (venv o conda).

```
# Crear y activar un entorno virtual con venv
python3 -m venv .venv
source .venv/bin/activate   # En Windows: .venv\Scripts\activate

# Instalar paquetes base (ajusta según lo que uses en el TP)
pip install numpy pandas matplotlib scikit-learn seaborn jupyter
```

### 2) Correr el script de ejemplo
```
python main.py
```
Deberías ver un saludo en la consola.

### 3) Abrir el notebook del TP2
```
jupyter notebook tp2_Juan_Manuel_Aidar_2025.ipynb
```
O bien con JupyterLab:
```
jupyter lab tp2_Juan_Manuel_Aidar_2025.ipynb
```

---

## 🧪 TP2 – Descripción breve
Este notebook incluye el desarrollo del Trabajo Práctico 2. Allí podrás encontrar:
- Análisis exploratorio de datos (EDA) si aplica.
- Preprocesamiento y preparación de features.
- Entrenamiento, validación y evaluación de modelos.
- Métricas, visualizaciones y conclusiones.

En la parte superior del notebook se listan las celdas necesarias para replicar los resultados. Asegúrate de ejecutar las celdas en orden.

---

## 🧰 Buenas prácticas recomendadas
- Mantener separado el código reutilizable en funciones (cuando sea posible).
- Fijar semillas aleatorias para reproducibilidad (por ejemplo, random_state en scikit-learn).
- Guardar versiones de datasets (o indicar claramente su fuente y cómo descargarlos).
- Documentar decisiones y resultados relevantes en el propio notebook y en este README.

---

## ✅ Checklist rápida antes de entregar un TP
- [ ] El notebook corre de principio a fin sin errores.
- [ ] Las librerías necesarias están listadas (y/o hay un requirements.txt).
- [ ] Se explican las decisiones tomadas y hay conclusiones claras.
- [ ] Se incluyen visualizaciones y métricas relevantes.
- [ ] Se fija random_state (si corresponde) y se controla data leakage.

---

## 📦 (Opcional) Archivo de dependencias
Si prefieres, puedes crear un archivo requirements.txt con las versiones exactas usadas:
```
pip freeze > requirements.txt
```
Luego, cualquier persona puede instalar con:
```
pip install -r requirements.txt
```

---

## 👤 Autoría
- Estudiante: Juan Manuel Aidar
- Año: 2025

Si tienes dudas o sugerencias, ¡abrí un issue o enviá un mensaje!

---

## 📚 Recursos útiles
- Documentación de scikit-learn: https://scikit-learn.org/
- Tutoriales de NumPy: https://numpy.org/learn/
- Pandas docs: https://pandas.pydata.org/docs/
- Matplotlib: https://matplotlib.org/stable/
- Seaborn: https://seaborn.pydata.org/

¡Éxitos en la cursada de IA! 🚀


---

## 🧹 Limpieza de notebooks (.ipynb): eliminar líneas y celdas duplicadas
Para eliminar líneas repetidas dentro de cada celda y (opcionalmente) celdas duplicadas completas, este repo incluye el script `dedup_ipynb.py`.

Uso básico:
```
python dedup_ipynb.py tp2_Juan_Manuel_Aidar_2025.ipynb
```
Genera un archivo `tp2_Juan_Manuel_Aidar_2025.dedup.ipynb` y muestra estadísticas de limpieza.

Opciones útiles:
- `--out RUTA`                Establece un archivo de salida personalizado.
- `--case-insensitive`        Ignora mayúsculas/minúsculas al detectar duplicados.
- `--strip-whitespace`        Ignora espacios extremos (strip) al comparar.
- `--no-collapse-blank`       No colapsa líneas en blanco consecutivas.
- `--keep-duplicate-cells`    Mantiene celdas idénticas (solo quita líneas repetidas dentro de cada celda).

Ejemplos:
```
# Limpieza agresiva (ignora espacios y mayúsculas/minúsculas)
python dedup_ipynb.py tp2_Juan_Manuel_Aidar_2025.ipynb --case-insensitive --strip-whitespace

# Mantener celdas duplicadas, solo limpiar líneas repetidas en cada celda
python dedup_ipynb.py tp2_Juan_Manuel_Aidar_2025.ipynb --keep-duplicate-cells

# Usar una ruta de salida específica
python dedup_ipynb.py tp2_Juan_Manuel_Aidar_2025.ipynb --out limpio.ipynb
```
