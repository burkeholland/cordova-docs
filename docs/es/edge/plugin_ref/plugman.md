---

license: Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0
    
         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
    

   under the License.
---

# Utilizando Plugman para administrar Plugins

Desde la versión 3.0 adelante, Cordova implementa todo el dispositivo APIs como plugins y les deja desactivado por defecto. También soporta dos formas diferentes para agregar y quitar plugins. La primera es mediante el `cordova` descrito en la interfaz de línea de comandos CLI. La segunda es mediante el uso de una interfaz de línea de comandos de nivel inferior [plugman][1]. Esta guía se centra en el segundo enfoque, que puede ser útil para los desarrolladores que desean actualizar su versión de Córdoba, pero que aún no han adoptado Cordova CLI en su flujo de trabajo.

 [1]: https://github.com/apache/cordova-plugman/

Para obtener más información sobre plugman, vea [el archivo README en su repositorio][2].

 [2]: https://github.com/apache/cordova-plugman/blob/master/README.md

## Comandos básicos

Para instalar plugman, debe disponer de [node][3] instalado en su máquina:

 [3]: http://nodejs.org/

    npm install -g plugman
    

Aquí está la sintaxis para añadir un plugin para cada plataforma:

    plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin <name|url|path> [--plugins_dir <directory>] [--www <directory>] [--variable <name>=<value> [--variable <name>=<value> ...]]
    

Para desinstalar un plugin:

    plugman --uninstall --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin <id> [--www <directory>] [--plugins_dir <directory>]
    

## Instalación de Plugins de núcleo

Los ejemplos siguientes muestran cómo agregar plugins según sea necesario para que cualquier APIs Cordova utilizas en tu proyecto todavía funcionan después de actualizar a la versión 3.0. Para cada comando, debes seleccionar la plataforma de destino y directorio del proyecto de la plataforma de referencia.

*   cordova-plugin-battery-status plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-battery-status.git

*   cordova-plugin-camera plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-camera.git

*   cordova-plugin-console plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-console.git

*   cordova-plugin-contacts plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-contacts.git

*   cordova-plugin-device plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device.git

*   cordova-plugin-device-motion (accelerometer) plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device-motion.git

*   cordova-plugin-device-orientation (compass) plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device-orientation.git

*   cordova-plugin-dialogs plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-dialogs.git

*   cordova-plugin-file plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-file.git

*   cordova-plugin-file-transfer plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-file-transfer.git

*   cordova-plugin-geolocation plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-geolocation.git

*   cordova-plugin-globalization plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-globalization.git

*   cordova-plugin-inappbrowser plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git

*   cordova-plugin-media plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-media.git

*   cordova-plugin-media-capture plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-media-capture.git

*   cordova-plugin-network-information plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-network-information.git

*   cordova-plugin-splashscreen plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-splashscreen.git

*   cordova-plugin-vibration plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-vibration.git