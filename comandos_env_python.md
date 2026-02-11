# Comandos generales pra gestión de entornos virtuales de python

Sitio oficial de python : [Python sitio oficial](https://www.python.org/)
Accede al indice de paquetes de python aqui: [Pypi sitio oficial](https://pypi.org/)

Debe tenerse claro la diferencia de un entorno virtual de python en el sistema operativo y el software que viene instalado por defecto con ubuntu linux.

| Comandos                                                          | Descripción                                                                                               |
| ----------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `which python3`                                                   | describe de donde se esta usando python                                                                   |
| `python3 -- version`                                              | verifica que versión de python se esta usando                                                             |
| `sudo apt update && sudo apt install -y python3-venv python3-pip` | actualiza el sistema operativo e instala el gestor de entornos virtuales de python y el gesto de paquetes |
| `cd /home/<nombre_usuario> && python3 -m venv .venv`              | se ubica en la ruta home - usuario y crea el entorno virtual con nombre .venv                             |
| `source ~/home/<nombre_usuario>/.venv/bin/activate`               | activa el entorno virtual                                                                                 |
| `pip install --upgrade pip`                                       | actualiza pip dentro del entorno virtual                                                                  |
| `pip freeze`                                                      | lista las librerías instaladas en el entorno virtual                                                      |

## Librerias a instalar

### Existen 2 opciones:

- #### De manera directa:

```bash
pip install numpy pandas scikit-learn scipy sympy matplotlib seaborn plotly bokeh torch tensorflow keras jax numba jupyterlab ipython fastapi[standard] uvicorn pydantic django scrapy beautifulsoup4 requests polars loguru wheel black dash pillow python-dotenv pytz selenium streamlit
```

- #### Con requirements.txt:

Crear un archivo requirements.txt (y se espera estar ubicado en la ruta donde se encuentra este archivo para ejecutar el comando de instalación) y guardar lo siguiente:

```
numpy
pandas
scikit-learn
scipy
sympy
matplotlib
seaborn
plotly
bokeh
torch
tensorflow
keras
jax
numba
jupyterlab
ipython
fastapi[standard]
uvicorn
pydantic
django
scrapy
beautifulsoup4
requests
polars
loguru
wheel
black
dash
pillow
python-dotenv
pytz
selenium
streamlit
```

luego ejecutar ubicado en la ubicación de requirements.txt (con el entorno virtual activado): 
```bash
pip install -r requirements.txt
```