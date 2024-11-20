# Análisis de Maquetación: Herman Miller Brand Standards

## 1. Estrategias de Maquetación

### 1.1 Diseño Responsivo

La web utiliza un diseño completamente responsivo que se adapta a diferentes tamaños de pantalla. Esto se logra mediante:

- Uso de unidades flexibles (%, vw, vh)
- Media queries para ajustar el diseño en diferentes breakpoints
- Flexbox y Grid para layouts flexibles

### 1.2 Sistema de Grid

Se implementa un sistema de grid personalizado para mantener una alineación consistente en toda la web. Esto proporciona:

- Consistencia visual
- Facilidad de mantenimiento
- Escalabilidad del diseño

### 1.3 Componentes Modulares

La web está construida con componentes modulares reutilizables, lo que permite:

- Consistencia en el diseño
- Desarrollo más rápido
- Facilidad de mantenimiento y actualización

## 2. Uso de Variables CSS

Las variables CSS (propiedades personalizadas) se utilizan extensivamente para optimizar el trabajo de maquetación:

### 2.1 Paleta de Colores

```css
:root {
  --color-primary: #FF0000;
  --color-secondary: #0000FF;
  --color-text: #333333;
  --color-background: #FFFFFF;
}
```

### 2.2 Tipografía

```css
:root {
  --font-primary: 'Helvetica Neue', sans-serif;
  --font-secondary: 'Georgia', serif;
  --font-size-base: 16px;
  --line-height-base: 1.5;
}
```

### 2.3 Espaciado

```css
:root {
  --spacing-small: 8px;
  --spacing-medium: 16px;
  --spacing-large: 24px;
  --spacing-xlarge: 32px;
}
```

### 2.4 Breakpoints

```css
:root {
  --breakpoint-sm: 576px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 992px;
  --breakpoint-xl: 1200px;
}
```

## 3. Ejemplos Prácticos

### 3.1 Uso de Variables CSS

```css
.button {
  background-color: var(--color-primary);
  color: var(--color-background);
  font-family: var(--font-primary);
  font-size: var(--font-size-base);
  padding: var(--spacing-small) var(--spacing-medium);
}
```

### 3.2 Media Query con Variables CSS

```css
@media (min-width: var(--breakpoint-md)) {
  .container {
    max-width: 720px;
  }
}
```

### 3.3 Flexbox para Layout Responsivo

```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
  gap: var(--spacing-medium);
}

.flex-item {
  flex: 1 1 300px;
  padding: var(--spacing-medium);
  background-color: var(--color-secondary);
}
```

### 3.4 Grid para Diseño de Página

```css
.grid-layout {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--spacing-large);
  padding: var(--spacing-xlarge);
}
```

## 4. Consejos para Practicar

1. Recrea secciones específicas de la web de Herman Miller utilizando las técnicas mencionadas.
2. Experimenta con diferentes valores en las variables CSS para ver cómo afectan al diseño global.
3. Intenta crear un sistema de componentes modular basado en los patrones de diseño de Herman Miller.
4. Practica la creación de layouts responsivos utilizando Flexbox y Grid con las variables CSS definidas.
5. Desarrolla un tema oscuro utilizando las mismas variables CSS, cambiando solo los valores en un selector de tema.

## 5. Ejemplo 'design-principles.html'

### 5.1 Puntos clave del ejemplo

1. **Reutilización de estilos**: La nueva página utiliza el mismo archivo `styles.css` del ejemplo original, manteniendo la consistencia en el diseño.
2. **CSS específico**: Creamos un archivo CSS separado (`design-principles.css`) para los estilos específicos de esta página, siguiendo el principio de separación de responsabilidades.
3. **Grid Layout**: Utilizamos `grid-template-columns: repeat(12, 1fr);` para crear un sistema de grid flexible y responsivo.
4. **Responsive Design**: El layout se ajusta en diferentes breakpoints, cambiando el número de columnas que ocupa cada principio.
5. **Consistencia en la navegación**: Actualizamos la navegación en ambas páginas para mantener la coherencia en la estructura del sitio.

### 5.2 Para practicar y entender mejor este ejemplo

1. Intenta añadir más principios de diseño y observa cómo se ajustan automáticamente en el grid.
2. Experimenta con diferentes valores para `grid-column: span X;` en los elementos `.principle`.
3. Prueba a implementar un diseño asimétrico, haciendo que algunos principios ocupen más columnas que otros.
4. Añade imágenes o iconos a cada principio de diseño y ajusta el CSS para acomodarlos.
5. Crea una nueva página (por ejemplo, "Productos") y enlázala de la misma manera en la navegación.
