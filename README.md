# Optimus

![Spain]("https://github.com/hampusborgos/country-flags/blob/main/png250px/es.png")

Optimus es un framework ligero y optimizado para el desarrollo rápido de aplicaciones web. Está diseñado para mejorar el rendimiento de las aplicaciones al cargar elementos rápidamente y manejar errores de forma efectiva en el lado del cliente.

![Optimus Logo](https://example.com/optimus-logo.png)

## Características

- **Optimización de rendimiento**: Carga rápida de elementos en la interfaz de usuario.
- **Manejo de errores integrado**: Muestra mensajes de error claros en la interfaz en caso de fallos.
- **Facilidad de uso**: Sintaxis simple para la definición de estado y renderización de componentes.

> [!IMPORTANT]\
> It is currently in the pre-alpha phase which is a project that surely has many flaws. So help me find them.

## Instalación

Puedes instalar Optimus directamente desde npm o incluirlo como un script en tu proyecto.

```bash
npm install @drxcodev/optimus
```

# Uso Básico
Para empezar a usar Optimus en tu proyecto, sigue estos pasos simples:

1. Inicializa el framework en tu archivo JavaScript principal:
```js
document.addEventListener("DOMContentLoaded", () => {
  async function loadTemplate(state) {
    // Simula un retraso para el ejemplo de carga diferida
    await new Promise(resolve => setTimeout(resolve, 1000));
    return (
      '<div>' +
        '<h1>Hello Optimus</h1>' +
      '</div>'
    );
  }

  window.app = new OptimizedFramework({
    el: '#app',
    state: {
      message: 'Hola, Mundo optimizado!'
    },
    template: loadTemplate
  });
});

```

2. Crea un contenedor en tu HTML donde se renderizará la aplicación:
```html
<div id="app"></div>
```

3. Personaliza la función `loadTemplate` y el estado inicial según las necesidades de tu aplicación.

# Ejemplos

## Cambio de mensaje
Este ejemplo muestra cómo cambiar dinámicamente el mensaje en la aplicación usando `setState`:
```html
<button onclick="window.app.setState({ message: '¡Nuevo mensaje!' })">Cambiar mensaje</button>
```
> [!WARNING]\
> It is currently disabled.

# Manejo de Errores
**Optimus maneja automáticamente los errores y los muestra en la interfaz de usuario.**

# Opciones

- **Estado de la ubicación local por continente:**
  Puedes editar en que continente puedes lanzar el servidor para ver como de diferentes maneras puedes ver el rendimiento de la web
  - Ves a `test/propieties/user.yaml`
  - En `user.yaml`
    ```yaml
    local: automatic # !: EU, USA, LATAM, ASIA, EUASIA, AFRICA, OCE
    ```
  
  > [!WARNING]\
  > Actualmente esta deshabilitado porque sigue en desarrollo, pronto estará

# Ignora los siguientes apartados

_Ignora los siguientes apartados, algunos están en prueba y no son relevantes_

| [lab/](https://github.com/DrxcoDev/Optimus/tree/main/lab) |

# Contribución
**¡Contribuciones son bienvenidas! Si quieres contribuir a Optimus, sigue estos pasos:**

1. Haz un fork del repositorio y clónalo en tu máquina local.
2. Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).
3. Realiza tus cambios y haz commit (git commit -am 'Añade nueva funcionalidad').
4. Sube tus cambios al repositorio (git push origin feature/nueva-funcionalidad).
5. Abre un pull request en GitHub.

## Nuestra tabla de contribucion:
![Alt](https://repobeats.axiom.co/api/embed/0a2b986977a12c59db1e422646f9599605bcd3c8.svg "Repobeats analytics image")
