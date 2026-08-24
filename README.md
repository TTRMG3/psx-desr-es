# PSX DESR ES-EN

Traducción dual inglés–español para la interfaz XMB de Sony PSX DESR, basada en
los recursos de idioma dual de Vitas.

## Estado

**v0.9 pre-release.** Probada físicamente en una **DESR-7500 con firmware 2.11**.
No es un firmware ni sustituye los archivos `.rel`: son recursos de idioma
(principalmente `.dic` y `.xml`). Aún quedan pantallas por pulir y verificar.

## Cómo funciona

El HDD-OSD actúa como selector de banco:

| Idioma seleccionado en HDD-OSD | Resultado en XMB |
| --- | --- |
| English | Inglés |
| Japanese | Español, donde ya existe traducción; inglés como reserva en los módulos pendientes |

Así se evita que la opción japonesa cargue ruso.

## Compatibilidad conocida

- Destinado a la familia PSX2: DESR-5500, DESR-5700, DESR-7500 y DESR-7700.
- Validado en una DESR-7500, sistema 2.11.
- No instalar a ciegas en series o versiones diferentes. Haz copia completa de
  los archivos que vayas a reemplazar antes de tocar la consola.

## Instalación de la pre-release

1. Parte de una instalación dual funcional de Vitas que corresponda exactamente
   a tu modelo y versión de sistema.
2. Guarda una copia de todos los archivos originales que vayas a sustituir.
3. Instala `psx_desr_2.11_en_es_v0.9.1_RUTAS_CORREGIDAS.zip`, conservando su
   estructura de carpetas. Es el paquete recomendado.
4. Copia `system/dic/` a `system/dic/` de la consola y
   `system/xosd/packages/` a `system/xosd/packages/`. **La carpeta `dic`
   global no va dentro de `packages`.**
5. En HDD-OSD selecciona **Japanese** para activar el español. Selecciona
   **English** para volver íntegramente al inglés.

La versión 0.9.1 ya incorpora el arreglo del banco japonés, Easy Setup y la
reserva inglesa de los módulos que aún no están traducidos. Es el único paquete
de instalación publicado para evitar confusiones.

## Limitaciones y cómo colaborar

- Es una pre-release: revisa los textos en tu propia máquina y comunica modelo,
  versión de sistema, ruta del archivo y una foto cuando encuentres un fallo.
- No se garantiza compatibilidad con cualquier versión de PSX ni con paquetes
  duales de procedencia distinta.
- Los PNG con texto incrustado necesitan tratamiento individual; no forman parte
  de esta versión.
- No se incluyen ejecutables, firmware, claves ni archivos `.rel`.

## Créditos

Creado por **Teo Tormo** y **Jarvis**.

La base del mecanismo de idioma dual y el trabajo previo pertenecen a
**Vitas**. Este proyecto es una traducción comunitaria e independiente; no está
afiliado a Sony ni a Vitas.

Sony, PSX y PlayStation son marcas de sus respectivos propietarios.
