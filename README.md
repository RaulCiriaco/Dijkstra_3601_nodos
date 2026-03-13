# 🧮 Algoritmo de Dijkstra - Calculadora de Ruta Más Corta

Aplicación web interactiva que implementa el **algoritmo de Dijkstra** para encontrar la ruta más corta entre nodos de un grafo dirigido. Desarrollada con Flask (Python) en el backend y Cytoscape.js en el frontend para visualización interactiva.

## 📸 Capturas de Pantalla

*(Aquí puedes agregar capturas de tu aplicación funcionando)*

## 🚀 Características Principales

- **Visualización interactiva de grafos** con Cytoscape.js
- **Implementación del algoritmo de Dijkstra** para encontrar rutas óptimas
- **Creación dinámica de nodos** con colores únicos automáticos
- **Tabla de conexiones editable** para definir aristas y pesos
- **Resaltado automático** de la ruta más corta encontrada
- **Interfaz responsive** adaptable a dispositivos móviles
- **Diseño moderno** con efectos glassmorphism y gradientes

## 🛠️ Tecnologías Utilizadas

### Backend
- **Python 3.x** - Lenguaje de programación principal
- **Flask** - Framework web ligero
- **NetworkX** - Biblioteca para operaciones con grafos
  - Implementación del algoritmo de Dijkstra
  - Manejo de grafos dirigidos

### Frontend
- **HTML5** - Estructura de la aplicación
- **CSS3** - Estilos con Bootstrap 5 y personalizaciones
- **JavaScript (ES6+)** - Lógica del cliente
- **Cytoscape.js** - Visualización interactiva de grafos
- **Bootstrap 5** - Framework CSS para diseño responsive
- **Font Awesome** - Íconos profesionales

## 📋 Requisitos Previos

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Navegador web moderno

## 🔧 Instalación y Configuración

1. **Clonar el repositorio**
```bash
git clone https://github.com/tuusuario/dijkstra-calculator.git
cd dijkstra-calculator
```

2. **Crear y activar entorno virtual**
```bash
# En Windows
python -m venv venv
venv\Scripts\activate

# En macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. **Instalar dependencias**
```bash
pip install -r requirements.txt
```

4. **Ejecutar la aplicación**
```bash
python app.py
```

5. **Abrir en el navegador**
```
http://localhost:5000
```

## 📁 Estructura del Proyecto

```
dijkstra-calculator/
│
├── app.py                      # Aplicación principal Flask
├── requirements.txt             # Dependencias del proyecto
├── .gitignore                   # Archivos ignorados por git
│
├── static/                      # Archivos estáticos
│   ├── diagram.js               # Lógica del grafo Cytoscape
│   ├── shortestPath.js          # Lógica del algoritmo Dijkstra
│   └── css/
│       └── styles.css            # Estilos personalizados
│
├── templates/
│   └── index.html                # Página principal
│
└── README.md                      # Documentación del proyecto
```

## 📊 Endpoints de la API

### `GET /`
- Renderiza la página principal con el visualizador de grafos

### `POST /shortest-path`
- Calcula la ruta más corta entre dos nodos usando Dijkstra
- **Cuerpo de la petición (JSON)**:
```json
{
    "start": "1",
    "end": "3",
    "edges": [
        {"source": "1", "target": "2", "weight": 5},
        {"source": "2", "target": "3", "weight": 3}
    ]
}
```
- **Respuesta (JSON)**:
```json
{
    "path": ["1", "2", "3"],
    "distance": 8
}
```

## 🎯 Funcionalidades Detalladas

### 1. **Gestión de Nodos**
- Crear nodos iniciales con un número específico
- Agregar nuevos nodos dinámicamente
- Cada nodo tiene un color único para fácil identificación

### 2. **Gestión de Conexiones**
- Tabla interactiva para definir conexiones
- Agregar múltiples destinos por nodo origen
- Eliminar conexiones no deseadas
- Validación de datos antes de agregar al grafo

### 3. **Visualización de Grafos**
- Disposición automática tipo "breadthfirst"
- Etiquetas visibles en nodos y aristas
- Colores diferenciados por nodo
- Resaltado de la ruta más corta

### 4. **Algoritmo de Dijkstra**
- Implementación backend con NetworkX
- Manejo de grafos dirigidos con pesos
- Detección de rutas inexistentes
- Visualización de la ruta óptima

## 💻 Ejemplo de Uso

1. **Crear nodos iniciales**: Ingresa "3" y haz clic en "Dibujar nodos iniciales"
2. **Agregar conexiones** en la tabla:
   - Nodo origen "1" → destino "2" con distancia "5"
   - Nodo origen "2" → destino "3" con distancia "3"
3. **Hacer clic en "Agregar conexiones al grafo"**
4. **Calcular ruta más corta**: Selecciona nodo inicial "1" y final "3"
5. **Resultado**: La ruta 1 → 2 → 3 con distancia 8 se resaltará en el grafo

## 🎨 Diseño Visual

- **Gradientes elegantes**: Fondo y botones con degradados azules
- **Efecto glassmorphism**: Contenedor semitransparente con blur
- **Hover effects**: Animaciones suaves en botones y filas de tabla
- **Responsive design**: Adaptable a todos los dispositivos
- **Iconografía profesional**: Íconos de Font Awesome

## 📝 Archivos JavaScript

### `diagram.js`
- Inicialización y configuración de Cytoscape
- Funciones: `drawNodes()`, `addNewNode()`, `addRow()`, `removeRow()`
- Manejo de colores únicos por nodo
- Actualización de la tabla de conexiones

### `shortestPath.js`
- Comunicación con el backend Flask
- Función: `calculateShortestPath()`
- Resaltado de la ruta encontrada
- Validaciones de entrada

## 🔒 Manejo de Errores

- Validación de nodos existentes
- Prevención de conexiones duplicadas
- Manejo de rutas inexistentes
- Mensajes de error claros para el usuario


## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## ✨ Autor

**Raúl Ciriaco Castillo**
- 🎓 Ingeniería en Sistemas Computacionales - Grupo 3601
- 📧 ciriacoral1567@gmail.com
- 🐙 [GitHub](https://github.com/RaulCiriaco)


