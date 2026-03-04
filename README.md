# CodeLab-Unisabana-Projects
¡Bienvenido a CodeLab Unisabana Projects! 🎉 Este es un laboratorio práctico donde cada píxel se convierte en dato — y cada dato vuelve a ser imagen. Este proyecto transforma imágenes JPG en matrices RGB dentro de Excel y viceversa, haciendo visible la lógica detrás del color digital.
¿Qué hace este proyecto? 💡
MóduloEntradaSalidaV1 — Imagen a PíxelesJPGExcel con celdas coloreadasV2 — Matriz a ImagenExcel con valores R,G,B o HEXExcel visual con celdas coloreadasV3 — Imagen a Matriz RGB NuméricaJPGExcel con valores R,G,B por celdaBonus — PloteoJPGVisualización con Matplotlib

🚀 Quickstart
1. Requisitos
bashpip install pillow openpyxl matplotlib

Este notebook corre en Google Colab. Asegúrate de montar tu Google Drive antes de ejecutar cualquier celda.

pythonfrom google.colab import drive
drive.mount('/content/drive')
2. Configura tus rutas
En cada módulo encontrarás variables de ruta claramente marcadas:
pythonruta_imagen_input  = "/content/drive/MyDrive/tu_carpeta/imagen.jpg"
ruta_excel_output  = "/content/drive/MyDrive/tu_carpeta/output.xlsx"
tamano_maximo      = (50, 50)  # Controla la resolución del pixel art
3. Ejecuta celda por celda
Cada módulo es independiente. Puedes ejecutarlos en orden o ir directamente al que necesitas.

📦 Estructura del Notebook
Pixel_Programing.ipynb
│
├── 🔌 Setup
│   ├── Montar Google Drive
│   └── Importar librerías (PIL, openpyxl, matplotlib)
│
├── 🖼️ V1 — JPG → Excel de colores
│   ├── procesar_imagen()       ← Carga y redimensiona el JPG
│   ├── crear_hoja_excel()      ← Pinta celdas con HEX por píxel
│   └── main()                  ← Orquesta el flujo completo
│
├── 🔁 V2 — Matriz de colores → Excel visual
│   ├── read_excel_colors()     ← Lee valores R,G,B o HEX de celdas
│   └── write_colors_to_excel() ← Genera nuevo Excel con celdas pintadas
│
├── 🔢 V3 — JPG → Matriz RGB numérica
│   ├── procesar_imagen()       ← Convierte a modo RGB explícito
│   ├── crear_excel_rgb_numeros() ← Escribe "R,G,B" como texto en cada celda
│   └── main_iteracion_3()      ← Incluye diagnósticos de píxeles
│
└── 📊 Bonus — Visualización y resolución
    ├── mostrar_imagen()        ← Plotea la imagen con Matplotlib
    └── image_to_excel()        ← Versión con escala y ajuste de celdas

🧠 Conceptos clave
¿Qué es una matriz RGB?
Cada imagen digital es una cuadrícula de píxeles. Cada píxel almacena tres valores numéricos entre 0 y 255: Rojo (R), Verde (G) y Azul (B). Este notebook hace esa estructura invisible... visible.
¿Por qué Excel?
Excel actúa como lienzo: cada celda = un píxel. Colorear celdas con openpyxl permite visualizar la imagen como una cuadrícula de datos puros — ideal para entender el procesamiento de imágenes sin infraestructura compleja.

⚙️ Parámetros importantes
ParámetroDescripciónValor recomendadotamano_maximoResolución del output en Excel(50, 50) para empezarscaleFactor de escala en V20.5 = mitad del tamañoimg.convert('RGB')Garantiza consistencia de canalesSiempre activado en V3

⚠️ Imágenes grandes (>200×200 px) pueden generar archivos Excel muy pesados y lentos. Ajusta tamano_maximo según necesites.


🗂️ Librerías utilizadas
LibreríaUsoPillow (PIL)Abrir, convertir y redimensionar imágenesopenpyxlCrear y manipular archivos .xlsxmatplotlibVisualizar imágenes en ColabosVerificar existencia de archivos

👥 Autores
Desarrollado como parte del laboratorio de Sistemas de Información Gerencial
Universidad de La Sabana · 2026-1

📄 Licencia
Este proyecto es de uso académico y educativo libre.
Si lo usas o lo adaptas, ¡dale crédito al laboratorio! 🙌
