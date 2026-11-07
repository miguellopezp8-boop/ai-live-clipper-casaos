# AI LIVE CLIPPER PRO — paquete CasaOS

Este paquete es una plantilla de repositorio privado para integrar la aplicación en un catálogo CasaOS personalizado.

## Requisitos previos
- El código fuente de AI LIVE CLIPPER PRO v1.1 debe estar en `/DATA/AppData/ai-live-clipper`.
- El disco USB debe estar montado de forma estable. La ruta propuesta en el `.env` es `/media/devmon/clipper`; hay que verificarla en CasaOS antes de iniciar.
- Mantener al menos 40 GB libres en el SSD para las imágenes y compilaciones, según la guía original del proyecto.

## Archivos
- `docker-compose.yml`: define los nueve servicios de la aplicación; los contextos de compilación apuntan al directorio de código ya existente.
- `.env.private-template`: plantilla de variables. No contiene contraseñas reales; crea secretos nuevos antes de usarla.
- `config.json`: ficha descriptiva de la aplicación para el catálogo.

## Importante
Este ZIP prepara los archivos del catálogo; por sí solo no hace que la app aparezca en la tienda oficial de CasaOS. Para que aparezca como una tarjeta instalable hay que publicar esta carpeta dentro de un repositorio Git accesible y añadir ese repositorio como App Store personalizado en CasaOS. La instalación no debe ejecutarse hasta verificar el montaje USB y completar el `.env`.

No ejecutar `docker compose down` sobre otras pilas ni modificar `nginx`, `cloudflared`, `jerrytattoo`, `taller`, `tienda` u otras aplicaciones existentes.
