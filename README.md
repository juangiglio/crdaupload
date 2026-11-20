# README upload_rinex.py

Este script permite subir archivos **RINEX** desde un directorio local a los servidores de **CRDASIR** (Centro Regional de Datos Alternos SIRGAS) de manera automatizada y asincrónica.

## 🚀 Requisitos

- Python 3.8 o superior
- Conexión a internet
- Credenciales válidas de acceso


## Para instalar python

### Windows

Para verificar si python se encuentra instalado presione la tecla windows+r y escriba cmd, de enter, escriba el siguiente comando:

```bash
python --version

```
Si no aparece la versión de python puede instalarlo desde la [página oficial de python](https://www.python.org/downloads/) o desde la [tienda de Microsoft](https://apps.microsoft.com/detail/9mssztt1n39l?ocid=webpdpshare).


### Linux

Para verificar si python se encuentra instalado escriba siguiente comando en el terminal:
```bash
python --version

```

Si no aparece la versión de python instálelo de acuerdo a la distribución de linux.



## 🛠 Instalación

Clona el repositorio o descarcárgalo en tu directorio local. Realiza la instalación básica o con entorno virtual.


### Instalación básica
1. Instalar dependencias, desde la carpeta donde se encuentra el script:
   ```bash
   pip install -r requirements.txt
   ```

### Instalación con entorno virtual 

1. Crea un entorno virtual (opcional pero recomendado)
   
   Es una buena práctica utilizar un entorno virtual para gestionar las dependenciasto. Para crear un entorno virtual, ejecuta los siguientes comandos desde el directorio en el que se encuentra la aplicación:

   Crear un entorno virtual en la carpeta 'venv'
   ```bash
   python -m venv venv
   ```
   Activa el entorno virtual en Windows
   ```bash
   venv\Scripts\activate
   ```
   Activa el entorno virtual en MacOS/Linux
   ```bash
   
   source venv/bin/activate
   ```

1. Instala las dependencias (librerías necesarias)
   ```bash
   pip install -r requirements.txt
   ```

## Modo de uso

### Carga de archivos
   Para cargar archivos RINEX desde un directorio se puede utilizar el argumento `-d <directorio>`
   
   En linux:
   ```bash
   python upload_rinex.py -d ./rinex_data/
   ```
   En windows:
   ```bash
   python upload_rinex.py -d c:\rinex_data
   ```

   - A continuación ingrese su usuario y contraseña.
   - Si la autenticación es correcta se comenzará con la subida masiva de archivos.
   - Se subirán archivos .Z o .gz.
   - Se presentarán errores si:
      - La nomenclatura de los archivos no sigue el estándar RINEX v2 o V3.
      - La estación no es de la red SIRGAS
      - El archivo RINEX es de una fecha anterior a fecha de inicio de la estación en la red SIRGAS.

### Cambio de contraseña
   Para cambiar la contraseña ejecute el siguiente comando y siga las instrucciones.

   ```bash
   python upload_rinex.py --change-password
   ```
   

