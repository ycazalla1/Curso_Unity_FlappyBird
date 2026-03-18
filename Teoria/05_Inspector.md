# Inspector
Gestiona los atributos de cada objeto.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/fe19279b-ee2c-4be0-89a7-5dece34fb0ba" />

- Transform: modifica la posición, rotación y escala (tamaño) del objeto.
  En videojuegos 2D solo se manejan la X e Y para posición y escala. La Z es rotación.
  En videojuegos 3D se usan todas las coordenadas para los tres tipos de transformación.

  <img width="400" alt="image" src="https://github.com/user-attachments/assets/20f150df-37df-420f-be8b-1872777b3474" />

- Sprite Renderer: componente que hace que se vea el sprite y le da atributos.
  
   <img width="400" alt="image" src="https://github.com/user-attachments/assets/69b2d786-a772-4022-9205-0a6fa33c60d7" />
  
  - Sprite: escoge el sprite (png) del objeto. Ya sea seleccionado a través de la imágen o arrastrando el sprite al selector.
  - Color: tiñe la imágen, no le modifica el color base que tiene.
  - Flip: voltea en horizontal (X) y en vertical (Y) el sprite.
  - Draw Mode: se usa para el fondo del juego.
