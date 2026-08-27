[README_RC10_SOLO_FIRMWARE_2.11.md](https://github.com/user-attachments/files/31530862/README_RC10_SOLO_FIRMWARE_2.11.md)
# PSX DESR en español — RC10

Traducción experimental del XMB al español para PSX DESR de segunda generación.

## Compatibilidad

Esta versión está destinada **exclusivamente** a los modelos DESR-5500, DESR-5700, DESR-7500 y DESR-7700 con firmware **2.11**.

La validación funcional completa se ha realizado en una DESR-7500 con firmware 2.11: aparecen y funcionan correctamente la copia a Memory Stick, su icono, la copia a DVD y el resto de funciones de vídeo, sin desplazamientos entre opciones y acciones.

### Firmware 2.06: no compatible

No instales RC10 en firmware 2.06. En una DESR-7500 con 2.06, el XMB llega a arrancar, pero se pierde la función de copia a Memory Stick y el menú de funciones de vídeo queda desalineado: los textos e iconos pueden verse, pero varias acciones abren la opción situada debajo de la seleccionada. La última función de la lista puede quedar inaccesible.

En otras palabras: puede parecer que funciona, pero perderás una función y otras tres o cuatro quedarán desplazadas respecto a su posición real.

### Firmware 2.10: pendiente de prueba

La compatibilidad con firmware 2.10 todavía no está validada. Hay indicios de que podría comportarse como 2.11, pero no se debe interpretar como una garantía ni instalarlo hasta completar la prueba en una consola de ensayo.

## Advertencia y responsabilidad

Este proyecto se ofrece gratuitamente, de forma experimental y sin garantía. No es software oficial de Sony y lo instalas bajo tu exclusiva responsabilidad.

Está dirigido a personas que ya saben realizar copias completas, restaurar el sistema de una PSX DESR y actuar con calma ante una transferencia fallida. Si no dispones de copia de seguridad, no sabes restaurarla o no aceptas la posibilidad de tener que repetir el proceso, no instales esta versión.

Las transferencias grandes mediante wLaunchELF/uLaunchELF hacia el HDD de una PSX DESR pueden congelarse o fallar de forma aparentemente aleatoria incluso cuando se siguen correctamente las instrucciones. Este riesgo forma parte del proceso de instalación.

## Antes de instalar: copia de seguridad obligatoria

Haz una copia completa de todas las particiones y archivos del HDD de tu PSX DESR antes de modificar nada.

Como mínimo, conserva fuera de la consola una copia íntegra de:

- `hdd0:/__system/dic/`
- `hdd0:/__system/xosd/packages/`

No continúes si no dispones de esa copia. Copiar los archivos nuevos por encima no elimina archivos sobrantes ni sustituye una restauración completa de las carpetas originales.

## Instalación

Necesitas un método fiable para ejecutar wLaunchELF/uLaunchELF y un USB preparado para tu consola.

1. Descarga el release RC10 y descomprímelo en el USB.
2. Entra en la carpeta `dic/` del release.
3. Copia su contenido en:

   ```text
   hdd0:/__system/dic/
   ```

4. Entra en `xosd/packages/` del release.
5. Selecciona y copia **todas las carpetas** incluidas allí.
6. Pégalas en:

   ```text
   hdd0:/__system/xosd/packages/
   ```

7. Acepta con `OK` todas las confirmaciones de sobrescritura.
8. Espera a que termine por completo la transferencia. No salgas del gestor de archivos, no reinicies, no apagues y no cortes la corriente durante la copia.
9. Cuando haya acabado sin errores, reinicia la PSX DESR y comprueba el XMB.

## Si la copia se congela o falla

No saques conclusiones precipitadas: una operación grande puede parecer congelada durante varios minutos.

- Si parece congelada, espera varios minutos para comprobar si termina sola.
- Si se recupera y muestra `Paste failed`, reinicia la PSX DESR y repite **todo** el proceso de copia desde el principio.
- Si no se recupera, fuerza el apagado manteniendo pulsado el botón `POWER` durante unos segundos. Después repite el proceso completo de copia.

Si después de una instalación el XMB no arranca correctamente, restaura las carpetas `dic` y `xosd/packages` completas desde tu copia de seguridad original; no intentes arreglarlo copiando archivos sueltos al azar.

## Soporte

No se ofrece garantía ni recuperación individual ante averías, pérdidas de datos, instalaciones incompletas o transferencias fallidas. Tampoco se presta soporte técnico por mensajes privados o redes sociales.

Los informes técnicos reproducibles que indiquen modelo exacto, firmware, método de instalación y disponibilidad de copia de seguridad pueden ayudar a mejorar futuras versiones.
