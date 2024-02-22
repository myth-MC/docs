---
description: Aprende a manejar tus claves de acceso a la API desde el mismo servidor.
---

# Desde el servidor

Puedes manejar tus claves de acceso desde el servidor mediante el uso de los siguientes comandos:

<table data-full-width="false"><thead><tr><th width="149">Comando</th><th width="140">Argumento(s)</th><th width="337">Descripción</th><th data-type="checkbox">Restringido</th></tr></thead><tbody><tr><td><strong>/api</strong></td><td><strong>key</strong></td><td>Genera una clave de acceso</td><td>false</td></tr><tr><td></td><td><strong>key</strong> list</td><td>Muestra todas tus claves. Haz clic sobre la que quieras usar para copiarla</td><td>false</td></tr><tr><td></td><td><strong>key</strong> list &#x3C;usuario></td><td>Muestra las claves de acceso de &#x3C;usuario></td><td>true</td></tr><tr><td></td><td><strong>key add</strong> &#x3C;usuario></td><td>Agrega una nueva clave de acceso a &#x3C;usuario></td><td>true</td></tr><tr><td></td><td><strong>key remove</strong> &#x3C;usuario> &#x3C;id/all></td><td>Elimina una clave de acceso de &#x3C;usuario> o todas directamente</td><td>true</td></tr><tr><td></td><td><strong>check</strong> &#x3C;usuario></td><td>Comprueba cuántas claves de acceso tiene &#x3C;usuario> y si está restringido del uso de la API</td><td>true</td></tr><tr><td></td><td><strong>ban</strong> &#x3C;usuario></td><td>Restringe a &#x3C;usuario> del uso de la API</td><td>true</td></tr><tr><td></td><td><strong>unban</strong> &#x3C;usuario></td><td>Devuelve a &#x3C;usuario> el acceso a la API. Tendrá que regenerar sus claves</td><td>true</td></tr></tbody></table>

{% hint style="info" %}
Sintaxis:

* \<argumento requerido>
* (argumento opcional)
* elección/múltiple
{% endhint %}
