# puertapp

## Tabla de contenidos

- [Sobre el proyecto](#about)
- [Comenzar](#getting_started)
- [Herramientas](#tools)
- [Demo](#demo)


## Sobre el proyecto <a name = "about"></a>

Desde Cargofive se envio un desafio el cual era "Te encontrarás con el análisis funcional del requerimiento junto a la HdU que se te entrega como desarrollador y a partir de ella debes:
● Construir la funcionalidad solicitada utilizando javascript con VueJS como
framework.
● Documentar y/o comentar el proceso desarrollado.
● Desarrollar una interfaz gráfica de alta calidad, con atención al detalle e intuitiva
para los usuarios.
● Asegurar el correcto funcionamiento del desarrollo entregado.
El formato de entrega debe ser un repositorio en Github, Gitlab o Bitbucket.
Nota: Desplegar este proyecto en un servidor, entregará un puntaje adicional.
Consumiendo una api que es http://apitest.cargofive.com/api/ports "
## Comenzar <a name = "getting_started"></a>

Estas instrucciones le proporcionarán una copia del proyecto en funcionamiento en su máquina local para fines de desarrollo y prueba.
### Instalacion

Una serie de ejemplos paso a paso que le indican cómo poner en marcha un entorno de desarrollo.


```
Hacer git clone del repositorio en github.
```
```
Usar npm i para instalar las dependencias del repositorio.
```
```
Levantar el proyecto con npm run serve
```
## Herramientas <a name = "tools"></a>
Las herramientas utilizadas fueron:
● Vue.js
● Vuetify
● Javascript
● CSS
● Vercel 

## Demo <a name = "demo"></a>

Este es el <a href="https://puertapp.vercel.app/" target="_blank">DEMO</a>







Tuve un solo problema que fue el siguiente 
![Captura de pantalla 2022-03-04 211134](https://user-images.githubusercontent.com/49873452/156858431-6f2586e6-2050-4a2f-9ed3-0e7f979daa19.png) 

El problema es que la API venia con protocolo http y no con https y por eso me generaba ese error, lo resolví usando esta linea " < meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests" > ".



