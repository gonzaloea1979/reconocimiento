# Terminal POS — entregas completas

## Version actual: 1.0.4

[Descargar ZIP completo 1.0.4](https://github.com/gonzaloea1979/reconocimiento/raw/refs/heads/main/Terminal_POS_1_0_4_Mejorado.zip)

Mismas funciones comerciales, con protecciones de respaldo y recuperación:

- Copias con la misma marca de tiempo no se sobrescriben; seis simultáneas verificadas.
- La retención conserva la copia recién creada aunque otras tengan fechas futuras.
- Origen de solo lectura: no se recrea una base desaparecida ni se publican archivos sin tablas como respaldos válidos.
- La copia termina con error ante bloqueos persistentes; errores de disco, permisos o verificación no se anuncian como éxito.
- Se verifican estructura SQLite y referencias entre tablas; se controla la desaparición de archivos durante listado/descarga.

**84 archivos de prueba aprobados**, 0 fallidos y 0 omitidos en Linux. Se restauró una base descargada en otra carpeta y se verificaron ventas, stock, deudas, caja y confirmaciones de reintento sin duplicados. Se probaron también fallos simulados y un bloqueo exclusivo real de SQLite.

**Compatibilidad:** si se detectan referencias inválidas, el respaldo se rechaza y el POS puede no iniciar con esa base. No borra ni repara los registros. Probar primero con una copia y conservar la instalación anterior y un respaldo externo.

Detalles e instrucciones: `MEJORAS_1_0_4.txt`, dentro del ZIP. El respaldo existente es de SQLite; fotos y tickets deben conservarse aparte. Incluye código y kit de compilación, **no un EXE precompilado**. La validación real en Windows y ante fallos físicos sigue pendiente.

## Version anterior: 1.0.3

[Descargar ZIP completo 1.0.3](https://github.com/gonzaloea1979/reconocimiento/raw/refs/heads/main/Terminal_POS_1_0_3_Mejorado.zip)

Conserva todas las correcciones anteriores y las mismas funciones comerciales.

- Pantalla de Ventas y Compras redondean cada renglón igual que el servidor; evita diferencias con cantidades fraccionadas.
- La vista del ticket cerrado utiliza los importes guardados. Cantidades acumuladas y vuelto usan aritmética decimal.
- Formato de fechas ISO más rápido en historiales, conservando los formatos anteriores.

Validación: **82 archivos de prueba aprobados**, 0 fallidos y 0 omitidos en Linux.
Se compararon 12.000 precios, 1.000 renglones y 2.016 fechas. Los casos fraccionados también se comprobaron con la API, SQLite, ticket PDF, reportes y Excel.
Carga sintética: 10.000 productos, 20.000 ventas y 60.000 renglones, sin errores HTTP.
La comparación aislada del formato de fechas pasó de 3,519 a 1,246 ms por 1.000 conversiones; no representa la mejora de toda la aplicación ni garantiza tiempos en Windows.

Incluye informes, pruebas y detalles en `MEJORAS_1_0_3.txt`, dentro del ZIP.
Descomprimir en una carpeta nueva y probar con una copia de los datos. No recalcula operaciones históricas.
**Incluye código y kit de compilación, no un EXE precompilado.** La ejecución, impresión y validación visual reales en Windows siguen pendientes.

## Version anterior: 1.0.2

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
