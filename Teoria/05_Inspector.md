# Inspector
Gestiona los atributos de cada objeto.

  <p align="center">
    <img width="400" alt="image" src="https://github.com/user-attachments/assets/fe19279b-ee2c-4be0-89a7-5dece34fb0ba" />
  </p>

- Transform: modifica la posición, rotación y escala (tamaño) del objeto.
  En videojuegos 2D solo se manejan la X e Y para posición y escala. La Z es rotación.
  En videojuegos 3D se usan todas las coordenadas para los tres tipos de transformación.

  <p align="center">
    <img width="400" alt="image" src="https://github.com/user-attachments/assets/20f150df-37df-420f-be8b-1872777b3474" />
  </p>

- Sprite Renderer: componente que hace que se vea el sprite y le da atributos.
  
  <p align="center">
    <img width="400" alt="image" src="https://github.com/user-attachments/assets/69b2d786-a772-4022-9205-0a6fa33c60d7" />
  </p>
  
  - Sprite: escoge el sprite (png) del objeto. Ya sea seleccionado a través de la imágen o arrastrando el sprite al selector.
  - Color: tiñe la imágen, no le modifica el color base que tiene.
  - Flip: voltea en horizontal (X) y en vertical (Y) el sprite.
  - Draw Mode: se usa para el fondo del juego. Si se pone en Tiled, sirve para poder expandir el fondo del mapa, tanto en horizontal (X) como en vertical (Y).
    Esto sirve para evitar añadir el mismo sprite varias veces a Scene, uno tras otro.

   <p align="center">
    <img width="347" height="160" alt="image" src="https://github.com/user-attachments/assets/76575c18-a300-40d5-9897-c9f800114a19" />
    <img width="1166" height="500" alt="image" src="https://github.com/user-attachments/assets/ded17a41-1ecf-4272-a629-25f7bf70fe8f" />
  </p>
    
     El Mesh Type del sprite sheet ha de estar en Full Rect para que no de error con el Tiled. (recomendado tenerlo usarlo siempre para juegos en 2D).

  <p align="center">
    <img width="348" height="261" alt="image" src="https://github.com/user-attachments/assets/b431aa01-7b55-4fa2-8b06-a4fc1b954f24" />
  </p>
