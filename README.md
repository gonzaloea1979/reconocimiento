# Terminal POS — entregas completas

## Version actual: 1.0.2

[Descargar ZIP completo 1.0.2](https://github.com/gonzaloea1979/reconocimiento/raw/refs/heads/main/Terminal_POS_1_0_2_Mejorado.zip)

Mismas funciones comerciales, con mejoras de estabilidad:

- Protección frente al doble envío en ventas, compras y pagos.
- Reintentos con respuesta perdida recuperan la confirmación anterior sin duplicar movimientos.
- Registro comercial y confirmación se guardan o revierten juntos; persisten tras reiniciar.
- Mensajes de PDF e impresión reflejan el resultado real.
- Compilador protege una instalación usada dentro de dist y comprueba el ZIP final antes de informar éxito.

Validación: **79 archivos de prueba aprobados**, 0 fallidos, 0 omitidos en Linux.
Las pruebas nuevas también se ejecutaron desde una extracción del ZIP entregado.

El ZIP contiene el programa completo, recursos, pruebas e instrucciones en `MEJORAS_1_0_2.txt`.
Incluye el kit para compilar en Windows; **no contiene un EXE precompilado**.
La compilación y ejecución real del EXE, impresión y validación visual siguen pendientes en Windows.

Descomprimir en una carpeta nueva y probar con una copia de los datos antes de actualizar.
La actualización conserva los datos y agrega automáticamente el registro de confirmaciones.
No recalcula saldos históricos incorrectos. Conservar respaldos externos verificados.

## Version anterior: 1.0.1

[Descargar ZIP completo 1.0.1](https://github.com/gonzaloea1979/reconocimiento/raw/refs/heads/main/Terminal_POS_1_0_1_Corregido.zip)

Incluye las correcciones originales de saldos concurrentes, efectivo esperado y cierre de caja,
también conservadas en 1.0.2. Validación original: 76 archivos aprobados en Linux.

## Descargar

Hacer clic en el enlace. Si GitHub abre la página del ZIP, elegir **Download raw** (flecha de descarga).
Cada ZIP tiene su archivo `.sha256` para comprobar integridad.
