# NotiAndChatFlutter
DAM-2023

## Guía para utilizar la aplicación Chat Flutter
1. Descarga del Proyecto
Descarga el proyecto desde el repositorio correspondiente. Puedes clonarlo desde Git o descargar el archivo ZIP.
 
    git clone <url_del_repositorio>

    cd <nombre_del_proyecto>

2. Configuración de Firebase
Asegúrate de tener Firebase instalado y configurado correctamente. Utiliza los siguientes comandos para vincular tu proyecto de Flutter con Firebase:

    firebase login

    dart pub global activate flutterfire_cli

    flutterfire configure

3. Integración de Firebase en Flutter
Añade las dependencias necesarias para Firebase en tu proyecto Flutter:

    flutter pub add firebase_core

    flutter pub add firebase_auth

    flutter pub add cloud_firestore

   
4. Configuración de Cloud Firestore
Accede a la consola de Firebase y habilita Cloud Firestore. Asegúrate de ajustar las reglas de seguridad de Firestore permitiendo lecturas y escrituras:

   → firebase.rules

    rules_version = '2';

    service cloud.firestore {

      match /databases/{database}/documents {
        match /{document=**} {
          allow read, write: if true;
        }
      }
    }
   
Después, actualiza las reglas ejecutando:

    flutter pub run firebase_tools setup:rules

5. Ejecución del Proyecto
  Finalmente, ejecuta el proyecto Flutter:

      flutter run
Results:

[![perifl-Hola.png](https://i.postimg.cc/sDTmD2CH/perifl-Hola.png)](https://postimg.cc/D8bLxnZ1)

[![Whats-App-Image-2023-11-30-at-10-41-41-AM.jpg](https://i.postimg.cc/wxcFZVfp/Whats-App-Image-2023-11-30-at-10-41-41-AM.jpg)](https://postimg.cc/Btbx1xfY)


# Guía para Integrar Notificaciones Push en una Aplicación Flutter con Firebase
1. Descarga de la Aplicación
Descarga el proyecto de la aplicación Flutter desde el repositorio. Puedes clonarlo o descargarlo como un archivo ZIP.
  git clone <url_del_repositorio>

  cd <nombre_del_proyecto>

2. Configuración de Firebase
   Creación del Proyecto en Firebase:
   
   Ve a la Consola de Firebase y crea un nuevo proyecto.
   Sigue las instrucciones para agregar tu aplicación Flutter a Firebase.

   Configuración de Firebase en la Aplicación Flutter:
      firebase login

      dart pub global activate flutterfire_cli

      flutterfire configure

      flutter pub add firebase_core

      flutter pub add firebase_messaging
3. Configuración de Firebase Cloud Messaging (FCM)
    Creación de una Campaña de Notificaciones:

    En la consola de Firebase, ve a "Cloud Messaging" y crea una campaña para las notificaciones.
   
4. Obtención del Token FCM
   Obtención y Registro del Token en la Aplicación

7. Ejecutar la Aplicación
Finalmente, ejecuta el aplicación Flutter

# Results
[![noti1.png](https://i.postimg.cc/6pk97RkM/noti1.png)](https://postimg.cc/ZWLk29KN)

[![noti2.png](https://i.postimg.cc/FzCvhJbg/noti2.png)](https://postimg.cc/n9mgkrPC)
