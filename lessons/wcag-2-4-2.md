# WCAG 2.4.2: Página de titulo dinámico

## Descripción

Este criterio de éxito busca garantizar que las páginas web incluyan un título descriptivo que indique claramente su propósito o contenido.

Esto implica que cada página debe tener un título único y significativo que sea fácilmente identificable por los usuarios y las tecnologías de asistencia. Por ejemplo, una página de contacto debe tener un título como "Contáctanos" en lugar de algo genérico como "Página 1". Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al facilitar la navegación y comprensión del contenido.

## Caso

Al ingresar dentro de CompraFácil, no importa la sección o ruta en la que se encuentre el usuario, todas las pantallas vienen acompañadas por el mismo título "CompraFácil". Esta práctica genera confusión significativa para los usuarios, especialmente aquellos que dependen de lectores de pantalla o tienen múltiples pestañas abiertas, ya que no pueden distinguir entre diferentes secciones del sitio basándose únicamente en el título de la página.

Esto dificulta la navegación, la comprensión del contexto actual y la capacidad de regresar a una sección específica cuando se tienen varias páginas del mismo sitio abiertas simultáneamente.

## Solución

Es posible realizar un mapeo dinámico para cada sección principal de CompraFácil, de tal manera que el título sea descriptivo con el contenido que se presenta:

```javascript
// Map component titles to their respective names
const titles = {
  catalog: 'Catalogo',
  blog: 'Blog',
  login: 'Iniciar Sesión',
  register: 'Registro',
  assistance: 'Asistencia',
  cart: 'Carrito de Compras',
  card: 'Tarjeta de Crédito',
  addcard: 'Agregar Tarjeta de Crédito',
  location: 'Ubicación',
  addlocation: 'Agregar Ubicación',
  payment: 'Método de Pago'
}

// Dynamic page component
function DynamicPage(props) {
  // Use either passed prop or URL parameter
  const params = useParams();
  const componentKey = (props.componentName || params.componentName || 'catalog').toLowerCase();

  const Component = components[componentKey] || Catalog;

  // Dynamically update the document title using the titles object
  useEffect(() => {
    const componentTitle = titles[componentKey] || 'CompraFácil'; // Fallback to "CompraFácil" if no title is found
    document.title = `${componentTitle}`;
  }, [componentKey]);

  return (
    <Background>
      <Component />
    </Background>
  );
}
```

## Criterio de éxito

Todas las pantallas deben tener un título principal y describir claramente su propósito.

## Mas información

[Understanding SC 2.4.2: Page Titled (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/page-titled)
