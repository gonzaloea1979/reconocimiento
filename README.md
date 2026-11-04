# Terminal POS 1.0.1 corregido

[Descargar el ZIP completo](https://github.com/gonzaloea1979/reconocimiento/raw/refs/heads/main/Terminal_POS_1_0_1_Corregido.zip)

Si GitHub muestra la página del archivo, elegir **Download raw** (flecha de descarga).

## Contenido

Programa completo, recursos, pruebas y kit para compilar el EXE en Windows.
Corrige saldos concurrentes de clientes, cálculo del efectivo esperado y cierre de caja concurrente.
Incluye instrucciones en `CORRECCIONES_1_0_1.txt`, dentro del ZIP.

## Validación

76 archivos de prueba aprobados en Linux con Python 3.12 y SQLite 3.53.1; sin fallos ni omisiones.
No incluye un EXE precompilado. La compilación, impresión y validación visual requieren pruebas en Windows.

Descomprimir en una carpeta nueva. Conservar respaldos y probar con una copia de los datos antes de actualizar.
Los saldos históricos incorrectos no se recalculan automáticamente.
