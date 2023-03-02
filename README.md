
# Slider snap

![version](https://img.shields.io/github/manifest-json/v/Natjo/slider-snap)

Slider


## Parameters
| Parameter | Type | Description |
| ------ | ------ | ------ |
| el | HTMLElement | Element |

## Methods
| Method | Type | Description |
| ------ | ------ | ------ |
| create | function | Activate the slider |
| destroy | function | Desactivate the slider |


## Classique

### Html 
```html
<div class="container slider myslider">
    <ul class="slider-content" aria-label="Last news">
        <li class="item"><a href="">1</a></li>
        <li class="item"><a href="">2</a></li>
        <li class="item"><a href="">3</a></li>
        <li class="item"><a href="">4</a></li>
        <li class="item"><a href="">5</a></li>
        <li class="item"><a href="">6</a></li>
        <li class="item"><a href="">7</a></li>
        <li class="item"><a href="">8</a></li>
    </ul>
    <button class="slider-btn prev" aria-hidden="true" tabindex="-1">prev</button>
    <button class="slider-btn next" aria-hidden="true" tabindex="-1">next</button>
</div>
```

### javascript
```javascript
const sliders = document.querySelectorAll('.slider');
sliders.forEach(slider => {
    const myscroll = new Slider(slider);
    myscroll.enable();
});

```

### css slider in container
```css
.myslider{
    @media (min-width: 600px){
        --col: 12;
        --nb: 4;
    }
}
```


## Full

### Html 
```html
<div class="slider full myslider" aria-label="Last news">
    <button class="slider-btn prev" aria-hidden="true" tabindex="-1">prev</button>
    <button class="slider-btn next" aria-hidden="true" tabindex="-1">next</button>
    <ul class="slider-content">
        <li class="item"><a href="">1</a></li>
        <li class="item"><a href="">2</a></li>
        <li class="item"><a href="">3</a></li>
        <li class="item"><a href="">4</a></li>
        <li class="item"><a href="">5</a></li>
        <li class="item"><a href="">6</a></li>
    </ul>
</div>
```

### css slider fulll width
```css
.myslider{
    grid-template-columns: var(--offset) auto var(--offset);

    .slider-content{
        grid-column: 1/-1;
    }
    .slider-btn{
        grid-column: 2;
    }

    @media (max-width: 599px){
        --nb: 2;
    }
    @media (min-width: 600px){
        --col: 12;
        --nb: 4;
    }
}

```

## Demo
<a href="https://codepen.io/natjo/pen/eYGWwEo?editors=1111" target="_blank">See codepen demo</a>