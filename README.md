# SIC25gt-noCompila


# Guía Rápida de Instalación y Configuración

Este documento proporciona una guía rápida para instalar y configurar el entorno necesario para ejecutar el sistema de reconocimiento facial con interfaz en Tkinter.

---

## 1. Requisitos Previos

Antes de comenzar, asegúrate de tener instalado lo siguiente:
- **Python 3.x** (Se recomienda la versión más reciente)
- **pip** (Administrador de paquetes de Python)
- **virtualenv** (Opcional pero recomendado para un entorno aislado)

Para verificar si Python está instalado, ejecuta en la terminal:
```bash
python --version
```
Si no está instalado, descárgalo desde [python.org](https://www.python.org/).

Para instalar `virtualenv`, usa:
```bash
pip install virtualenv
```

---

## 2. Crear y Activar un Entorno Virtual

Se recomienda usar un entorno virtual para gestionar las dependencias del proyecto. Sigue estos pasos:

1. Crea un entorno virtual:
   ```bash
   virtualenv venv
   ```
2. Activa el entorno virtual:
   - En Windows:
     ```bash
     venv\Scripts\activate
     ```
   - En macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

Para desactivar el entorno virtual en cualquier momento, usa:
```bash
deactivate
```

---

## 3. Instalación de Dependencias

Ejecuta los siguientes comandos dentro del entorno virtual para instalar las bibliotecas necesarias:

```bash
pip install opencv-python
pip install numpy
pip install pandas
pip install deepface
```

Las siguientes bibliotecas ya vienen incluidas con Python y no requieren instalación adicional:
- `os`
- `pickle`
- `time`
- `datetime`
- `tkinter` (incluido en la instalación estándar de Python)

---

## 4. Solución de Problemas

### Error: "No se pudo acceder a la cámara"
- Asegúrate de que la cámara está conectada y que ningún otro programa la esté usando.
- Prueba ejecutar:
  ```bash
  python -c "import cv2; print(cv2.VideoCapture(0).isOpened())"
  ```
  Si devuelve `False`, revisa los permisos de la cámara en tu sistema operativo.

### Error: "Modulo 'deepface' no encontrado"
- Verifica que estás dentro del entorno virtual antes de ejecutar el script.
- Prueba reinstalar DeepFace:
  ```bash
  pip install --upgrade deepface
  ```

---

