# Welcome to Remix!

- [Remix Docs](https://remix.run/docs)

## Development

From your terminal:

```sh
npm run dev
```

This starts your app in development mode, rebuilding assets on file changes.

## Deployment

First, build your app for production:

```sh
npm run build
```

Then run the app in production mode:

```sh


Instalación de Dependencias
Para instalar las dependencias necesarias para el proyecto, sigue estos pasos:

Clona el repositorio a tu máquina local:

bash

Copiar
git clone https://github.com/AngelaCTTorres/comfama-read-con-remix.git
Navega al directorio del proyecto:

bash

Copiar
cd comfama-read-con-remix
Instala las dependencias utilizando npm o yarn:

bash

Copiar
npm install
o

bash

Copiar
yarn install
Arranque del Proyecto
Para arrancar el proyecto en modo desarrollo, utiliza el siguiente comando:

bash

Copiar
npm run dev
o

bash

Copiar
yarn dev
Esto iniciará un servidor de desarrollo y podrás acceder al proyecto en tu navegador en http://localhost:3000.

Conceptos Clave
Links
En Remix, los links se utilizan para cargar recursos como hojas de estilo. Puedes definirlos en tu componente utilizando la función links.

tsx

Copiar
import { LinksFunction } from "remix";

export const links: LinksFunction = () => [
  { rel: "stylesheet", href: appStylesHref },
];
Loaders
Los loaders son funciones que cargan datos en tu aplicación antes de que la página se renderice. Se utilizan para obtener datos del servidor.

tsx

Copiar
import { LoaderFunction } from "remix";

export const loader: LoaderFunction = async () => {
  const data = await fetchData();
  return { data };
};
Rutas Dinámicas
Las rutas dinámicas permiten crear rutas que contienen parámetros variables. En Remix, puedes definir rutas dinámicas utilizando corchetes en el nombre del archivo.

plaintext

Copiar
routes
├── posts
│   └── $postId.tsx
Rutas Anidadas
Las rutas anidadas permiten organizar tu aplicación en una jerarquía de rutas. Utilizan el componente <Outlet /> para renderizar las rutas hijas.

tsx

Copiar
import { Outlet } from "remix";

export default function Parent() {
  return (
    <div>
      <h1>Ruta Padre</h1>
      <Outlet />
    </div>
  );
}
Componente Outlet
El componente <Outlet /> se utiliza en rutas padres para renderizar los componentes hijos. Es una forma de definir zonas en tu aplicación donde se cargarán las sub-rutas.

tsx

Copiar
import { Outlet } from "remix";

export default function Parent() {
  return (
    <div>
      <h1>Ruta Padre</h1>
      <Outlet /> {/* Aquí se renderizan los componentes hijos */}
    </div>
  );
}
npm start
```

Now you'll need to pick a host to deploy it to.

### DIY

If you're familiar with deploying node applications, the built-in Remix app server is production-ready.

Make sure to deploy the output of `remix build`

- `build/server`
- `build/client`
