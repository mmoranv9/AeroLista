# AeroLista — Proyecto integrador

Aplicación web de reservación de pasajes desarrollada con **Python + Flask**, HTML, CSS, JavaScript, lista enlazada simple y persistencia JSON. Se implementaron los nueve métodos solicitados en `lista_pasajeros.py`.

## Requisitos
- Python 3.10 o superior
- Visual Studio Code
- Extensión Python para VS Code (recomendado)

## Ejecutar en Windows (VS Code)

1. Descomprime `aerolista.zip`.
2. En VS Code selecciona **Archivo → Abrir carpeta** y abre la carpeta `aerolista`.
3. Abre **Terminal → Nuevo terminal**.
4. Ejecuta estos comandos, uno por uno:

```powershell
python -m venv venv
venv\Scripts\activate
python -m pip install -r requirements.txt
python app.py
```

5. Abre el navegador en: http://127.0.0.1:5050

Para detener el servidor: `Ctrl + C` en la terminal.

## Estructura

```text
aerolista/
├── app.py
├── lista_pasajeros.py
├── pasajero.py
├── persistencia.py
├── prueba_consola.py
├── revisar.py
├── verificador.py
├── vuelo.py
├── requirements.txt
├── data/
│   └── ejemplo.json
├── static/
│   ├── css/
│   │   └── estilos.css
│   └── js/
│       ├── api.js
│       ├── avion.js
│       ├── buscar.js
│       ├── clic.js
│       ├── datos-demo.js
│       ├── eliminar.js
│       ├── listar.js
│       ├── main.js
│       ├── mensajes.js
│       ├── modificar.js
│       ├── pestanas.js
│       ├── progreso.js
│       ├── reservar.js
│       ├── semaforo.js
│       ├── tablero.js
│       ├── tooltip.js
│       ├── tren.js
│       ├── utilidades.js
│       └── vista3d.js
└── templates/
    └── index.html
```

## Métodos de lista enlazada implementados
1. `esta_vacia()`
2. `longitud()`
3. `listar()`
4. `buscar(numero)`
5. `buscar_por_asiento(asiento)`
6. `buscar_por_cedula(cedula)`
7. `modificar(numero, nuevo_nombre, nueva_edad, nuevo_asiento)`
8. `eliminar(numero)`
9. `filtrar_por_clase(clase)`

## Verificar los métodos
Con el entorno virtual activado, ejecuta:

```powershell
python -c "import verificador; [print(r['metodo'], r['estado'], r['detalle']) for r in verificador.revisar_todo()]"
```

El resultado esperado es `ok` en los nueve métodos. También puedes ejecutar `python prueba_consola.py` para la demostración básica.

## Datos
La primera ejecución carga `data/ejemplo.json`. Al crear, modificar o cancelar reservas, Flask genera y actualiza `data/reservas.json`. Ese archivo se conserva al cerrar el servidor.

**Importante:** no borres la carpeta `data`. No es necesario subir la carpeta `venv` al entregar el proyecto.
