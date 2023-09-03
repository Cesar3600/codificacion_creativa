
# CODIFICACION CREATIVA


## VARIABLES AND FUNCTIONS
Estamos repasando la estructura interna de un archivo html

### ---beginPath()---
Inicia el proceso de grafico

### StrokeStyle
Le da estilo al trazado

### lineWidth
Define el ancho del trazado

### .arc(250,250,80,0,Math.PI*2 )
define un arco, posicion en x:250, en y:250, radio:80, inicio de trazado, fin de trazado

### --stroke--
permite el dibujo

***

## ---VARIABLES AND FUNCTIONS---
puedes declarar valores antes de el beginpath a modo de variables globales

ej: mira el efecto que tiene linewidth




>[!IMPORTANT]
>### reactangle
> context.react(pos x, pos y, width, height)
>


```
  context.beginPath();
  context.lineWidth=33;
  context.rect(100,100,400,400)
  context.stroke()
```


>[!IMPORTANT]
>### circle or arc
> context.arc(pos x, pos y, radio, begin draw, end draw)
>

```
  context.beginPath()
  context.lineWidth=77;
  context.strokeStyle='white'
  context.arc(300,300,100,0,Math.PI*2)
  context.stroke()
```

***

## MATRICES Y BUCLES

las matrices son un conjunto de valores agrupados



```
for(let i = 0;i < 5; i++){
  for(let j = 0;j < 5; j++){
    let width = 60;
    let height = 60;
    let gap = 20;
    let x = 100 +  (width + gap) * i;
    let y = 100 +  (width + gap) * j;
  
    context.beginPath();
    context.rect(x,y,width,height);
    context.stroke();
    if(i==4 || i==0 || j==0 || j==4){
      context.beginPath()
      context.rect(x+8,y+8,width-16,height-16)
      context.stroke()
    }

  }
}

```

tambien podemos agregar el random al diseno

```
for(let i = 0;i < 5; i++){
  for(let j = 0;j < 5; j++){
    let width = 60;
    let height = 60;
    let gap = 20;
    let x = 100 +  (width + gap) * i;
    let y = 100 +  (width + gap) * j;
  
    context.beginPath();
    context.rect(x,y,width,height);
    context.stroke();
    if(Math.random() > 0.5){
      context.beginPath()
      context.rect(x+8,y+8,width-16,height-16)
      context.stroke()
    }

  }
}
```
