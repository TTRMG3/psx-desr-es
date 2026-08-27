[README_RC10_SOLO_FIRMWARE_2.11-2.md](https://github.com/user-attachments/files/31531174/README_RC10_SOLO_FIRMWARE_2.11-2.md)
# PSX DESR en español — RC10

Traducción experimental del XMB al español para PSX DESR de segunda generación.

## Alcance del proyecto

RC10 modifica **323 archivos de sistema**:

- 150 diccionarios `.dic`
- 149 archivos `.xml`
- 23 imágenes `.png`
- 1 recurso `.rgn`

El archivo incluye además 9 documentos de texto con notas de versiones y pruebas. No se modifican ejecutables `.rel`.

El trabajo acumulado de traducción, adaptación, empaquetado, restauraciones y pruebas en consola ha requerido aproximadamente **40–60 horas**.

## Principio de diseño

La intención no es rediseñar la PSX DESR ni convertirla en una interfaz moderna: es hacer comprensible su XMB conservando la identidad visual, la estructura y el comportamiento de Sony.

Se respetan las rutas originales, los módulos existentes, los iconos y gráficos que no necesitan texto, y la disposición de la interfaz. Solo se sustituyen recursos de idioma y los gráficos que contienen texto japonés cuando hacerlo no altera el diseño ni la función prevista por el sistema.

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

## Créditos

Creado por [Teo Tormo](https://www.arcadeartisan.com) y su fiel amigo Jarvis.

---

# PSX DESR in Spanish — RC10

Experimental Spanish translation of the XMB for second-generation PSX DESR systems.

## Project scope

RC10 modifies **323 system files**:

- 150 `.dic` dictionaries
- 149 `.xml` files
- 23 `.png` images
- 1 `.rgn` resource

The archive also includes 9 text documents containing release and testing notes. No `.rel` executables are modified.

The combined translation, adaptation, packaging, restoration and on-console testing work represents approximately **40–60 hours**.

## Design principle

The aim is not to redesign the PSX DESR or turn it into a modern interface. It is to make its XMB understandable while preserving Sony's visual identity, structure and behaviour.

Original paths, existing modules, icons and graphics that do not need text are retained, as is the interface layout. Only language resources and graphics containing Japanese text are replaced, and only where doing so does not alter the intended design or system function.

## Compatibility

This release is intended **exclusively** for DESR-5500, DESR-5700, DESR-7500 and DESR-7700 systems running firmware **2.11**.

Full functional validation has been carried out on a DESR-7500 running firmware 2.11: Memory Stick copy, its icon, DVD copy and the remaining video functions appear and work correctly, with no mismatch between menu entries and actions.

### Firmware 2.06: not compatible

Do not install RC10 on firmware 2.06. On a DESR-7500 running 2.06, the XMB does boot, but the Memory Stick copy feature disappears and the video-function menu becomes misaligned: labels and icons may still be visible, but several entries open the action below the one selected. The final item in the list may become inaccessible.

In other words: it may look as if it works, but you will lose one function and three or four others will be shifted from their real action.

### Firmware 2.10: pending testing

Compatibility with firmware 2.10 has not yet been validated. There are indications it may behave like 2.11, but this must not be interpreted as a guarantee and it should not be installed until testing has been completed on a dedicated test console.

## Warning and responsibility

This project is provided free of charge, experimentally and without warranty. It is not official Sony software and you install it entirely at your own risk.

It is intended for people who already know how to make complete backups, restore a PSX DESR system and react calmly to a failed file transfer. If you do not have a backup, do not know how to restore it, or cannot accept the possibility of having to repeat the procedure, do not install this release.

Large transfers to the HDD of a PSX DESR through wLaunchELF/uLaunchELF may freeze or fail seemingly at random even when the instructions are followed correctly. This risk is inherent to the installation process.

## Before installing: mandatory backup

Make a complete backup of all partitions and files on your PSX DESR HDD before changing anything.

At minimum, keep a complete copy outside the console of:

- `hdd0:/__system/dic/`
- `hdd0:/__system/xosd/packages/`

Do not continue without that backup. Copying the new files over the old ones does not remove leftover files and is not a substitute for a complete restoration of the original folders.

## Installation

You need a reliable method of running wLaunchELF/uLaunchELF and a USB drive prepared for your console.

1. Download the RC10 release and extract it to the USB drive.
2. Open the release's `dic/` folder.
3. Copy its contents to:

   ```text
   hdd0:/__system/dic/
   ```

4. Open `xosd/packages/` in the release.
5. Select and copy **all folders** contained there.
6. Paste them into:

   ```text
   hdd0:/__system/xosd/packages/
   ```

7. Confirm every overwrite prompt with `OK`.
8. Wait until the transfer has completed fully. Do not leave the file manager, restart, power off or disconnect power while the copy is in progress.
9. Once it has finished without errors, restart the PSX DESR and check the XMB.

## If copying freezes or fails

Do not jump to conclusions: a large operation may appear frozen for several minutes.

- If it appears frozen, wait several minutes to see whether it completes on its own.
- If it recovers and shows `Paste failed`, restart the PSX DESR and repeat **the entire** copy process from the beginning.
- If it does not recover, force a shutdown by holding the `POWER` button for a few seconds. Then repeat the complete copy procedure.

If the XMB does not start correctly after installation, restore the complete `dic` and `xosd/packages` folders from the original backup; do not try to repair it by copying individual files at random.

## Support

No warranty or individual recovery assistance is provided for hardware failures, data loss, incomplete installations or failed transfers. Technical support is not provided through private messages or social media.

Reproducible technical reports that include the exact model, firmware, installation method and confirmation that a backup exists can help improve later release candidates.

## Credits

Created by [Teo Tormo](https://www.arcadeartisan.com) and his faithful friend Jarvis.
