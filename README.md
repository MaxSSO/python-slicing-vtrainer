# Python Slicing Trainer

Aplicación [Vue.js](https://vuejs.org/) que simula el Slicing Notation de Python.



## Demo

in progress ...



## Probar en Local

Para probar localmente basta con ejecutar:

```
yarn install
yarn serve
```

o

```
npm install
npm run serve
```

Por defecto la aplicación debería ejecutarse en el puerto `localhost:8080`.



## ¿Cómo funciona?

El texto "Hello World!" se renderiza mediante una [propiedad computada](https://vuejs.org/v2/guide/computed.html#Computed-Properties) que dependiendo de los valores de los inputs: `start` y `end`, corta la palabra haciendo uso de la función [slice](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/String/slice) de los strings de JavaScript.

```javascript
computed: {
  slicedWord () {
    if (!this.start && !this.end) {
      return this.word
    } else if (!this.end) {
      return this.word.slice(this.start)
    } else {
      return this.word.slice(this.start, this.end)
    }
  }
}
```
