# Adóptame - Cambia una vida

Este proyecto es una página web diseñada para promover la adopción de mascotas. A continuación, se describen las decisiones de diseño y el funcionamiento de las animaciones implementadas.

## Decisiones de Diseño

1. **Estructura Visual:**
   - Se ha utilizado un diseño limpio y centrado, con un encabezado llamativo que incluye un título y un subtítulo para captar la atención del usuario.
   - La sección de presentación proporciona un mensaje claro y motivador sobre la importancia de la adopción.
   - La galería de mascotas está organizada en un contenedor flexible para mostrar las imágenes de las mascotas con sus respectivas etiquetas.

2. **Colores y Tipografía:**
   - Se seleccionaron colores cálidos como el naranja y tonos tierra para transmitir cercanía y calidez.
   - La tipografía `Arial, sans-serif` fue elegida por su legibilidad y simplicidad.

3. **Responsividad:**
   - Se implementaron estilos responsivos para garantizar que la página se vea bien en dispositivos móviles y pantallas más pequeñas.
   - Los elementos de la galería y los botones se ajustan en tamaño y espaciado según el ancho de la pantalla.

4. **Interactividad:**
   - Se añadieron efectos de hover en los elementos de la galería y en el botón de llamada a la acción para mejorar la experiencia del usuario.

## Animaciones Implementadas

1. **Animación de Entrada de la Galería:**
   - Los elementos de la galería tienen una animación de entrada llamada `fadeInUp`, que los hace aparecer desde abajo con un efecto de desvanecimiento.
   - Cada elemento tiene un retraso (`animation-delay`) para que aparezcan de forma escalonada.

   ```css
   @keyframes fadeInUp {
     0% {
       opacity: 0;
       transform: translateY(50px);
     }
     100% {
       opacity: 1;
       transform: translateY(0);
     }
   }
    ```

2. **Parpadeo de Ojos:**
    - Los ojos de los SVG del perro y el gato tienen una animación de parpadeo (blink) que se repite de forma infinita.
    - Se utiliza transform: scaleY para simular el cierre y apertura de los ojos.

    ```css
    @keyframes blink {
        0%, 92%, 100% {
            transform: scaleY(1);
        }
        95% {
            transform: scaleY(0.1);
        }
        }
    ```

3. **Movimiento de Bigotes del Gato:**

    - Los bigotes del gato tienen una animación (move-bigotes) que los hace oscilar ligeramente hacia los lados.

    ```css
    @keyframes move-bigotes {
        0%, 95%, 100% {
            transform: rotate(0deg);
        }
        96%, 98% {
            transform: rotate(3deg);
        }
        97%, 99% {
            transform: rotate(-3deg);
        }
        }
    ```

4. **Movimiento de la Boca del Perro:**

    - La boca del perro tiene dos animaciones combinadas: un trazo progresivo (draw) y un movimiento de sacudida (shake-mouth).
    ```css
    @keyframes draw {
        from {
            stroke-dashoffset: 1000;
        }
        to {
            stroke-dashoffset: 10;
        }
    }

    @keyframes shake-mouth {
        0%, 100% {
            transform: rotate(0deg);
        }
        25% {
            transform: rotate(2deg);
        }
        75% {
            transform: rotate(-2deg);
        }
    }
    ```

## Cómo Funciona
- Los elementos SVG del perro y el gato están diseñados para ser interactivos y dinámicos, utilizando animaciones CSS para darles vida.
- La galería utiliza flexbox para organizar los elementos de manera uniforme y centrada.
- Las animaciones están configuradas con propiedades como animation-delay y infinite para crear un efecto continuo y atractivo.

Este diseño busca un diseño simple pero atractivo y sobre todo adaptable a cualquier tipo de dispositivo, bien sea móvil, tablet o desktop.