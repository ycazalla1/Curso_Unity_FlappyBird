# Mover fondo
En este apartado se mostrará cómo podemos simular que el fondo se mueve, en este caso el suelo:
Existen dos maneras de mover el fondo:
- Moviendo su textura.
- Moviendo el propio objeto, que hace de fondo.

## Mover el objeto
Se divide en dos secciones, la gráfica i la de programación.

### Sección gráfica I
1. Se añade un segundo objeto con el mismo sprite.
2. Fusionamos ambos objetos manteniendo V, usando la herramienta de movimiento. Esto hace que cuando acercamos uno al lado del otro, se "pegan".
 
  <p align="center">
    <img width="500" alt="image" src="https://github.com/user-attachments/assets/b7e0d2a2-e00d-42e0-bb36-cafc0f27bae0" />
  </p>
  
3. Si se puede ver en la unión, de la imágen de arriba, se ve que hay un corte en el suelo. Eso rompería la simulación de que es el mismo suelo que se mueve.
   Para solucionar eso se pone el Tile Mode en Adaptative, quedando así:

   <p align="center">
    <img width="500" alt="image" src="https://github.com/user-attachments/assets/508ed568-4e7f-4bd8-908f-095381314536" />
   </p>

> [!TIP]
> Es mejor tener ambos objetos separados, y en un mismo objeto padre. Esto es debido a que los moveremos independientemente.

### Sección código
  4. Con esto podemos comenzar a hacer el script. Creamos un nuevo script C#, dentro de la carpeta Scripts (si no existe se crea).

   <p align="center">
    <img width="339" height="234" alt="image" src="https://github.com/user-attachments/assets/9e3fa412-cefb-4493-92a5-b5f4fd711b31" />
   </p>
  
  5. Luego, le asignamos el script a ambos objetos.
  
  #### Script
  ```
  public class Suelo : MonoBehaviour
  {
      // Referencia al Transform de otro objeto
      public Transform anotherFloor;

      void Start()
      {
          
      }
  
      void Update()
      {
          // Mueve el suelo hacia la izquierda a una velocidad constante
          transform.position -= new Vector3(0.7f * Time.deltaTime, 0, 0);
  
          // Cuando el suelo se aleja lo suficiente, lo reposicionamos para crear un efecto de suelo infinito
          if (transform.position.x <= -5f)
          {
              // Reposiciona el suelo a la derecha del otro suelo (el 5f es el ancho del suelo | SpriteRender > Draw Mode (Tiled) > Size)
              // Yo le pongo 4.99f para que se solapen mejor los suelos y aparezca ningún espacio sin controlar
              transform.position = new Vector3(anotherFloor.position.x + 4.99f, transform.position.y, transform.position.z);
          }
      }
  }
  ```
### Sección gráfica II
  6. Cuando tenemos el script guardado, solo hemos de asignar el otro suelo a nuestra variable Transform en Unity.
     Podemos hacerlo de dos formas:
     - Opción 1: arrastrar el otro objeto suelo, desde Hierarchy, a la variable.
     - Opción 2: darle al punto de la variable, y allí escoger el objeto.

       <p align="center">
        <img width="297" height="63" alt="image" src="https://github.com/user-attachments/assets/d01adfa5-418d-4c4e-a65a-12207c3eb4d8" />
       </p>

## Resultado
Así es cómo quedaría el suelo con efecto infinito:

<p align="center">
 <img width="500" alt="suelo_infinito" src="https://github.com/user-attachments/assets/ebe12bce-abc7-450a-9f08-9e3e7612549a" />
</p>
