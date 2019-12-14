# Vanilla_JS_Canvas
Drawing Canvas made with vanilla javascript<br>
![ezgif com-video-to-gif](https://user-images.githubusercontent.com/55618626/70845419-cdcbd400-1e91-11ea-9a2a-9cc58e49a590.gif)

![image](https://user-images.githubusercontent.com/55618626/70845436-0ff51580-1e92-11ea-9387-9d8c123a72aa.png)

## Getting Started
It's a canvas that you can paint, fill in color, and clear the canvas. Inspired by Apple drawing pad. 
### Used
- HTML
- CSS
- Javascript
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)\(This is from HTML\)
### Explanation for functions
#### Canvas API?
It's a API provided by javascript and HTML <canvas> element for drawing graphics. In the **Canvas** API there is **CanvasRenderingContext2D** interface which helps drawing shapes, text, images, and other objects. 
```js
const canvas = document.querySelector("#jsCanvas");
const ctx = canvas.getContext('2d');
  
canvas.width = 700;
canvas.height = 550;

ctx.fillStyle = "white";
ctx.fillRect(0, 0, canvas.width, canvas.height);
ctx.lineWidth = 2.5; 
ctx.strokeStyle = INITIAL_COLOR;
ctx.fillStyle = INITIAL_COLOR;
```

#### Saving image
By using `toDateURL`method in canvas, you can bring the data URL containing a representation of the image\(default PNG\). In addition, you have to make an `<a>`tag to use `download`method. 
```js
const image = canvas.toDataURL();
const link = document.createElement('a');
link.href = image;
link.download = "PaintJS";
link.click();
```
