# AlanMRamirez

##Face animals recognition 
<h6>Este proyecto es una red neural convolucional enfocada en la identificacion de tres categorias: gato, perro y animales salvajes(zorro, leon, tigre, entre otros) </h6>:tw-1f42f::tw-1f431: :tw-1f436: :tw-1f43a:
![](https://forum.huawei.com/enterprise/es/data/attachment/forum/202106/07/121019qq9i4d9rsk4rog4z.png?CCN2.png)
## Librerias utilizadas en este proyecto fueron Tensorflow y Keras
<p>Se utilizaron estas dos librerias en particular debido a su gran facilidad al momento de tener que crear cada una de las capas de la red neuronal</p>

##Creacion de la red neuronal convolucional

    model_base = Sequential()
    
    model_base.add(Conv2D(32, (3,3), activation='relu', input_shape=(100,100,3)))
    model_base.add(MaxPooling2D((2,2)))
    
    model_base.add(Conv2D(64, (3,3), activation='relu'))
    model_base.add(MaxPooling2D((2,2)))
    
    model_base.add(Conv2D(128, (3,3), activation='relu'))
    model_base.add(MaxPooling2D((2,2)))
    
    model_base.add(Flatten())
    model_base.add(Dropout(0.2))
    model_base.add(Dense(64,activation='relu'))
    model_base.add(Dropout(0.3))
    model_base.add(Dense(128,activation='relu'))
    model_base.add(Dropout(0.2))
    model_base.add(Dense(256,activation='relu'))
    model_base.add(Dropout(0.3))
    model_base.add(Dense(3,activation='softmax'))
<p>
Para esta red se utilizaron las siguientes capas:</p>
<ul>
<li>Tres capas convolucionales de 32, 64 y 128 filtros  y una matriz de 3x3</li>
<li>Tres capaz de maxpoling de 2x2</li>
<li>Para la red neuronal utilice un flatten, con 4 dropouts y tres capaz densas de 64, 128 y 256 neuronas con la funcion de activacion relu</li>
<li>Para la capa de salida utilice 3 neuronas y una funcion softmax para poder obtener la probabilidad de cada una de las categorias redondeada a un 100%</li>
</ul>

