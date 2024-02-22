---
description: >-
  Todos los recursos necesarios para integrar tus programas, aplicaciones o webs
  con mythMC.
---

# Cómo funciona nuestra API

Actualmente nuestra [API](https://es.wikipedia.org/wiki/API) tiene la capacidad de leer datos o estadísticas en tiempo real desde la base de datos del servidor. Podríamos expandir las funciones en un futuro a medida que surjan nuevas ideas y retos.

## Requisitos

* Nociones básicas del protocolo [REST](https://www.redhat.com/es/topics/api/what-is-a-rest-api)
* Nociones básicas del formato [JSON](https://es.wikipedia.org/wiki/JSON)
* Acceso a cualquier sistema con [curl](https://curl.se/download.html) para poder realizar pruebas

{% hint style="info" %}
Puedes ejecutar `curl` desde la terminal de tu sistema operativo para comprobar si ya tienes el programa.

En macOS y la mayoría de distribuciones de Linux ya viene preinstalado.
{% endhint %}

## Posibles usos

* Una web que obtenga y procese los datos de cada usuario históricamente
* Un bot de Discord que compruebe el ranking de los mejores clanes cada hora
* Una aplicación que almacene y compare tus estadísticas antes y después de tu última sesión de juego

El hecho de que el protocolo REST no requiera de ningún cliente específico para obtener datos abre ampliamente el campo de posibilidades para poder desarrollar cualquier tipo de integración que se te ocurra. El límite está en tu creatividad.

<details>

<summary>Condiciones de uso de nuestra API</summary>

Permitimos el uso de nuestra API siempre y cuando se cumpla con nuestras condiciones:

* Tu integración se verá limitada si intenta realizar más de **2 peticiones/minuto**. Los usuarios con una [suscripción](https://wiki.mythmc.ovh/guia/suscripciones) activa tienen un límite de **20 peticiones/minuto**.
* Nos reservamos el derecho a almacenar temporalmente tu dirección IP con el fin de detectar posibles abusos de nuestra API. Tu IP no se compartirá en ningún momento con nadie externo al equipo de desarrolladores.
* Nos reservamos el derecho a revocar tu acceso en cualquier momento si consideramos que tu integración tiene un propósito dañino.

</details>
