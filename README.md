# App Dice Roller 🎲

## Cambios realizados:

   *   __*string.xml segun idioma:*__
   
       * Lo primero que hice fue dar click derecho encima del *string.xml* y abrir el *Translation Editor*. Este editor nos pemitirá cambiar los idiomas de los   strings que ahi se encuentran. Para ello, clickamos donde la bola del mundo que encontramos arriba y seleccionamos el idioma deseado. A continuacion, cmabiamos el idioma de cada uno de los strings en sus celdas correspondientes y por ultimo comprobamos que se ha creado un nuevo *string.xml* pero con una etiqueta a la derecha del nombre que indica el idioma que hemos elegido.
 
       * --> [Click aquí](https://github.com/Endermaiter/JuegoDado/commit/6fce3fa487f43a579a60f6c0def56263ef2c077b) para ver los cambios realizados.
       
   *   __*Cambiar strings en el layout:*__
   
       * Ahora tenemos qu cambiar el string que viene dentro del boton ("Lanzar") por *"@stirng/roll"*. De esta forma tomara el valor de ese string ubicado en el archivo *string.xml* y se modificara en funcion del idioma seleccionado en los ajustes de nuestro telefono.
       
       * --> [Click aquí](https://github.com/Endermaiter/JuegoDado/commit/bd5c1fcbff20420c92bf7fd5109576595a4862e2) para ver los cambios realizados.
   
   *  __*Cambiar las imagenes en drawable:*__
   
       * El primer paso es descargar una imagen cualquiera de internet, la que nosotros queramos, pero en formato **SVG**. Una vez descargada, solo tendremos que reemplazarla. Hacemos click derecho sobre la carpeta *drawable* y en el apartado new, le damos a ***Vector Asset***. Nos abrira una interfaz de importación de imagenes SVG, donde tendremos que seleccionar la opcion de importar archivos desde archivos locales y, para ahorrar trabajo de cambiar codigo, renombraremos el archivo con el nombre de la imagen que queramos sustituir. Automaticamente se sobreescribirá y, por ejemplo, la imagen *dice_1.xml* ya pasaría a ser otra.
       
       * --> [Click aqui](https://github.com/Endermaiter/JuegoDado/commit/229527b4c59f333dc6dfba49f8d47b0246fa57f5) para ver los cambios realizados.
   
  *  __*Cambiar la funcion random por algo similar:*__
  
       * Yo, en mi caso, hice lo siguiente:
       ```
       private fun rollDice() {
          val numeros = listOf(1, 2, 3, 4, 5, 6)
          val drawableResource = when (numeros.random()) {
              1 -> R.drawable.dice_1
              2 -> R.drawable.dice_2
              3 -> R.drawable.dice_3
              4 -> R.drawable.dice_4
              5 -> R.drawable.dice_5
              else -> R.drawable.dice_6
          }
          diceImage.setImageResource(drawableResource)
        }
        ```
      * --> [Click aqui](https://github.com/Endermaiter/JuegoDado/commit/172760339bc028bbaebf2b77f227afbea0729924) para ver los cambios realizados.
      
  * __*Modificar el boton para usar material.io y que tenga asociado un icono:*__
  
      *Evidentemente, lo primero que debemos hacer será descargar el icono de internet. En mi caso, descargué [*este*](https://fonts.google.com/icons?icon.platform=android) que lo encontre en la pagina de **Google Fonts** a la que me redirigió *material.io*. A continuación, importé la imagen en la carpeta *drawable* (Click derecho > New > Image Asset). Ahora solo tenemos que asociar el icono al boton. Lo hacemos entrando a los atributos del boton y, en el apartado drawableLeft, seleccionamos el icono previamente importado (El XML se modifica automaticamente). Ya tenemos el boton con el icono deseado asociado.
      
      * --> [Click aqui](https://github.com/Endermaiter/JuegoDado/commit/3e0740caf6c287141238e1ae2ae9ec0f48357e30) para ver los cambios realizados.
      
      
