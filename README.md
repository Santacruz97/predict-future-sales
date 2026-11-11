# Predict Future Sales

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

Análisis exploratorio de datos (EDA) del dataset [Predict Future Sales](https://www.kaggle.com/competitions/competitive-data-science-predict-future-sales/data) de Kaggle, con las ventas diarias de la cadena rusa 1C Company entre enero de 2013 y octubre de 2015. El análisis prepara la etapa de forecasting, cuyo objetivo es predecir las ventas mensuales de cada par tienda-producto en noviembre de 2015.

El análisis completo está en [`notebooks/01_exploratory_data_analysis.ipynb`](notebooks/01_exploratory_data_analysis.ipynb), y las gráficas generadas en [`reports/figures/`](reports/figures/).

## Estructura del proyecto

```
├── data
│   ├── external           <- Datos de terceros.
│   ├── interim            <- Datos intermedios transformados.
│   ├── processed          <- Datos finales para modelar.
│   └── raw                <- CSV originales de Kaggle (no se versionan).
├── docs                   <- Proyecto base de mkdocs.
├── models                 <- Modelos entrenados y sus predicciones.
├── notebooks              <- Notebooks de Jupyter, incluido el EDA.
├── predict_future_sales   <- Código fuente del proyecto.
├── references             <- Enunciado del proyecto y material de consulta.
├── reports
│   └── figures            <- Gráficas generadas por el notebook.
├── Makefile               <- Comandos de conveniencia de la plantilla.
├── pyproject.toml         <- Metadatos y configuración de herramientas.
└── requirements.txt       <- Dependencias del entorno.
```

## Instalación del entorno

El proyecto requiere Python 3.14.

En Windows (PowerShell):

```powershell
git clone https://github.com/Santacruz97/predict-future-sales.git
cd predict-future-sales
py -3.14 -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

En macOS o Linux:

```bash
git clone https://github.com/Santacruz97/predict-future-sales.git
cd predict-future-sales
python3.14 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Datos

Los datos no se incluyen en el repositorio. Descarga los CSV desde la [página de datos de la competencia](https://www.kaggle.com/competitions/competitive-data-science-predict-future-sales/data), que requiere una cuenta gratuita de Kaggle, y colócalos en `data/raw/`. Como `data/` no se versiona, debes crear esa carpeta después de clonar:

```
data/raw/
├── item_categories.csv
├── items.csv
├── sales_train.csv
├── sample_submission.csv
├── shops.csv
└── test.csv
```

## Ejecución

Con el entorno activado, abre el notebook y selecciona el kernel de `.venv`:

```bash
jupyter notebook notebooks/01_exploratory_data_analysis.ipynb
```

Las secciones dependen de la limpieza hecha en las secciones anteriores, así que el notebook debe ejecutarse completo y en orden.
