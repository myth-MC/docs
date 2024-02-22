---
description: Información básica para obtener datos de usuarios.
---

# Usuarios

{% hint style="info" %}
Actualmente todas las peticiones utilizan como base la dirección <mark style="background-color:blue;">https://api.mythmc.ovh/v1/...</mark>\
Puedes ver todas las peticiones posibles haciendo [clic aquí](usuarios.md#lista-de-peticiones-posibles).
{% endhint %}

## Usar `curl` en la interfazUsar `curl` en la interfaz

1. **Instalar** [**curl**](https://curl.se/download.html) **si no está instalado aún en tu ordenador**. Puedes comprobarlo rápidamente desde la terminal de tu sistema operativo con el comando `curl --version`.
2. **Crear una clave de acceso** si aún no tienes una. Para ello, ve al servidor e introduce el comando `/api key`. Puedes consultar esta llave en cualquier momento usando el comando `/api key list`.
3. **Ejecutar una consulta de prueba.** Abre la terminal de tu sistema operativo y ejecuta cualquier petición especificando tu clave de acceso como header (mira el comando de abajo si no sabes cómo hacerlo). Si la petición se ejecuta correctamente obtendrás el código **200** junto a la respuesta.

Ejemplo:&#x20;

```bash
curl -H "X-API-Key: clave-de-acceso" "https://api.mythmc.ovh/v1/users/test/mytharites
```

## Incorporar el ejemplo en una IDE

Una vez hayamos comprobado que la conexión con la API es correcta y estable ya solo es cuestión de encontrar la forma de incorporar llamadas a una API REST usando tu lenguaje de programación de elección.

Por ejemplo, para el caso de Java:

```java
class call {
	public static void main(String[] args) {
		HttpRequest request = HttpRequest.newBuilder()
				.uri(URI.create("https://api.mythmc.ovh/v1/users/Udeilu/mytharites"))
				.header("X-API-Key", "tu-clave")
				.method("GET", HttpRequest.BodyPublishers.noBody())
				.build();
		// Faltaría guardar la respuesta
	}
}
```

O, si usamos JavaScript:

```javascript
fetch('https://api.mythmc.ovh/v1/users/Udeilu/mytharites', {
      method: 'GET',
      headers: {
            'X-API-Key': 'tu-clave',
            },
      })
      .then(response => response.json())
      .then(json => console.log(json));
```

En Google encontrarás muchos más ejemplos de cómo integrar una API usando cualquier lenguaje de programación que se te ocurra.

## Lista de peticiones posibles

Estas son todas las peticiones relacionadas con los clanes que puedes integrar.&#x20;

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/{consulta}" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

Las **{consultas}** posibles son:

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/mytharites" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/clan" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/kills_deaths" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/player_info" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/referral" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}

{% swagger src="../.gitbook/assets/openapi-2.json" path="/users/{nombre}/protocol" method="get" %}
[openapi-2.json](../.gitbook/assets/openapi-2.json)
{% endswagger %}
