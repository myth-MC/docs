---
description: >-
  Algo de orientación para resolver los posibles problemas que te puedas
  encontrar a la hora de usar nuestra API.
---

# Fallos comunes

Antes de nada, ante cualquier error recomendamos comprobar que la petición realizada sea válida. Para ello usaremos [curl](https://curl.se/download.html). Por ejemplo, si queremos realizar una petición a `.../v1/users/test/mytharites` usaremos el siguiente comando:

```sh
curl -H "X-API-Key: nuestra-clave" https://api.mythmc.ovh/v1/users/test/mytharites
```

Si la petición devuelve la respuesta esperada (ver [#lista-de-peticiones-posibles](usuarios.md#lista-de-peticiones-posibles "mention")) significa que **el problema esta en tu código**. Si, por contra, no obtienes respuesta, puede ser que nuestra API esté caída o que haya algún fallo en la conexión entre tu servicio y nuestra API (problema de DNS probablemente).

## Respuesta vacía (`[]`, `"{}"`, etcétera)

Una respuesta vacía significa que alguno de los argumentos especificados no figura en nuestra base de datos. Te recomendamos revisar que el nombre del usuario o clan sea correcto y que la petición sea la adecuada.

* [#lista-de-peticiones-posibles](clanes.md#lista-de-peticiones-posibles "mention") para peticiones relacionadas con **clanes**.
* [#lista-de-peticiones-posibles](usuarios.md#lista-de-peticiones-posibles "mention") para peticiones relacionadas con **usuarios**.

## Límite de peticiones alcanzado (`API Rate Limit Exceeded...`)

Todas las claves de acceso a nuestra API tienen por defecto un límite de **2 peticiones/minuto**. Si se supera este límite tendrás que esperar 1 minuto hasta la próxima petición.&#x20;

Si **necesitas expandir el límite** te recomendamos adquirir una suscripción para tener hasta **20 peticiones/minuto.**

## Otros errores

Si encuentras cualquier otro error y no sabes cómo solucionarlo te invitamos a preguntar en nuestro [Discord](https://discord.gg/y5Pz69AywB). Ten en cuenta que nuestra API todavía esta en fase **beta** y podría haber errores que no hayamos identificado aún.

