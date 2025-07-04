# 📱 Lector de QR y Cámara con Apache Cordova

![Apache Cordova](https://img.shields.io/badge/Apache-Cordova-E83835?style=for-the-badge&logo=apache&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

> Aplicación móvil multiplataforma simple desarrollada con Apache Cordova que demuestra el uso de la cámara del dispositivo para tomar fotos y escanear códigos QR.

## 📜 Sobre el Proyecto

Este proyecto es una aplicación móvil híbrida creada para aprender y demostrar cómo Apache Cordova puede actuar como un puente entre tecnologías web (HTML, CSS, JavaScript) y las funcionalidades nativas de un dispositivo móvil.

El objetivo principal es mostrar la integración de plugins de Cordova para acceder al hardware del teléfono, en este caso, la cámara.

### La Estructura de un Proyecto Cordova

Un proyecto Cordova tiene una estructura de carpetas específica:
* **`/www`**: Es el corazón de la aplicación. Contiene todo el código web (`index.html`, `css/`, `js/`) que conforma la interfaz y la lógica de la app.
* **`/platforms`**: Carpeta generada por Cordova que contiene el código del proyecto nativo para cada plataforma (ej. `/android`, `/ios`).
* **`/plugins`**: Contiene el código nativo de los plugins que se añaden al proyecto (como el de la cámara o el scanner QR).
* **`config.xml`**: El archivo de configuración principal de la aplicación. Aquí se define el nombre, el ID del paquete, los permisos y los plugins que utilizará la app.

<br>

## ✨ Características

* **Captura de Fotografías:** Utiliza el plugin `cordova-plugin-camera` para abrir la cámara del dispositivo, tomar una foto y mostrarla directamente en la pantalla de la aplicación.
* **Escaneo de Códigos QR:** Implementa el plugin `cordova-plugin-qrscanner` para activar un escáner en tiempo real que decodifica la información de un código QR y la muestra en una alerta.

<br>

## 🛠️ Construido Con

* [Apache Cordova](https://cordova.apache.org/) - Framework para el desarrollo de apps móviles híbridas.
* HTML5, CSS3, JavaScript
* **Plugins de Cordova:**
    * `cordova-plugin-camera`: Para acceder a la cámara.
    * `cordova-plugin-qrscanner`: Para escanear códigos QR.

<br>

## 🚀 Empezando

Para compilar y ejecutar este proyecto, necesitas tener configurado el entorno de desarrollo de Apache Cordova.

### Prerrequisitos

* [Node.js y npm](https://nodejs.org/en/)
* **Apache Cordova CLI:**
    ```bash
    npm install -g cordova
    ```
* **SDK de la plataforma deseada:**
    * Para Android: [Android Studio](https://developer.android.com/studio) y el SDK de Android.
    * Para iOS: [Xcode](https://developer.apple.com/xcode/) (solo en macOS).

### Instalación y Ejecución

1.  **Clona el repositorio:**
    ```bash
    git clone https://github.com/JACarlin/cordovaApp_QR_reader.git
    ```
2.  **Navega a la carpeta del proyecto:**
    ```bash
    cd cordovaApp_QR_reader
    ```
3.  **Añade una plataforma** (por ejemplo, Android):
    ```bash
    cordova platform add android
    ```
4.  **Instala los plugins necesarios:**
    ```bash
    cordova plugin add cordova-plugin-camera
    cordova plugin add cordova-plugin-qrscanner
    ```
5.  **Construye la aplicación:**
    ```bash
    cordova build android
    ```
    Esto generará el archivo `.apk` de instalación en la carpeta `platforms/android/app/build/outputs/apk/debug/`.

6.  **Ejecuta la aplicación en un emulador o dispositivo conectado:**
    ```bash
    # Para ejecutar en un dispositivo conectado por USB o un emulador abierto
    cordova run android
    
    # O para ejecutar en un emulador directamente
    cordova emulate android
    ```
    *Nota: La cámara y el escáner QR funcionan mejor en un dispositivo físico real.*

<br>

## 📖 Uso de la Aplicación

1.  Abre la aplicación en tu dispositivo.
2.  Presiona el botón **"Toma Foto"** para activar la cámara y capturar una imagen. La foto aparecerá en el espacio designado.
3.  Presiona el botón **"Leer QR"** para abrir el escáner. Apunta la cámara a un código QR.
4.  Cuando el escáner detecte y decodifique el QR, mostrará el contenido del mismo en una alerta.

<br>
