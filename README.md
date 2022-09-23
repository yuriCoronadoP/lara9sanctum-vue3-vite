# SPA AUTHENTICATION USING LARAVEL 9 SANCTUM, VU3 AND VITE

SANCTUM Brinda un sistema de autenticacion ligero dependientes de servicios de autenticacion  de sesion basados en cookies incorporados en Laravel.

## Como trabaja laravel SANCTUM

Antes de iniciar a codificar a ciegas sin ningun entendimiento sobre lo que ocurre detras, vamos a revisar como Sanctum trabaja.
Laravel Sanctum usa autenticacion de sesion basados en cookies Laravel para autenticar usuarios desde el cliente. Aquí está el flujo:

1. Se hace una request a la cookie CSRF desde Sanctum en el cliente, el cual permite hacer request protegida por CSRF a puntos finales normales como /login
2. Haces un request al punto final normal de Laravel como /login.
3. Laravel emite una cookie que mantiene la sesión del usuario.
4. Cualquier solicitud a su API ahora incluye esta cookie, por lo que su usuario se autentica durante el tiempo de vida de esa sesión.