---
title: "3D Image Slider"
date: 2024-08-02T21:55:28-06:00
categories: [ "Image_Slider" ]
---
{{< rawhtml >}}
<p style="margin-bottom: 30px;">This example demonstrates a 3D rotating cube using CSS animations and transformations. The cube rotates around the Y-axis, and each side of the cube displays a different image.
</p>
{{< /rawhtml >}}


{{< rawhtml >}}


<style>
    .container:before {
        content: '';
        width: 100%;
        height: 100%;
        box-shadow: 0 0 75px 20px #0000001a, inset 0 0 350px 350px #0000001a;
        position: absolute;
        top: 90px;
        left: 0px;
        transform: rotateX(95deg) translateZ(-80px);
        animation: rotateShadow 16s infinite;
    }

    @keyframes rotateShadow {
        0% {
            transform: rotateX(95deg) translateZ(-80px) rotateZ(360deg);
        }

        25% {
            transform: rotateX(95deg) translateZ(-80px) rotateZ(270deg);
        }

        50% {
            transform: rotateX(95deg) translateZ(-80px) rotateZ(180deg);
        }

        75% {
            transform: rotateX(95deg) translateZ(-80px) rotateZ(90deg);
        }

        100% {
            transform: rotateX(95deg) translateZ(-80px) rotateZ(0deg);
        }
    }

    @keyframes rotate {
        0% {
            transform: rotateY(0deg);
        }

        25% {
            transform: rotateY(90deg);
        }

        50% {
            transform: rotateY(180deg);
        }

        75% {
            transform: rotateY(270deg);
        }

        100% {
            transform: rotateY(360deg);
        }
    }
</style>

<div class="container" style="width: 240px; height: 240px; perspective: 800px;">
    <div class="cube" style="height: 100%; width: 100%; position: relative; transform-style: preserve-3d; transform: all 0.8s ease-in-out; animation: rotate 16s infinite;">
        <img src="https://assets.lummi.ai/assets/QmW239ythzhEUCVHTDxSzCVaB8wkA16E4hiF6MmNwgRSin?auto=format&w=1500" style="position: absolute; width: 240px; height: 240px; backface-visibility: hidden; transform: rotateY(0deg) translateZ(120px);">
        <img src="https://assets.lummi.ai/assets/QmQHKeemS2YCLkdTBgQxyFbgwE2RHFr1F51AVhQFFcKCAy?auto=format&w=1500" style="position: absolute; width: 240px; height: 240px; backface-visibility: hidden; transform: rotateY(90deg) translateZ(120px);">
        <img src="https://assets.lummi.ai/assets/QmS3Y6cMYsRAbXF9t5zmRWwqNttpX65Ev9DvykuHsBCFb6?auto=format&w=1500" style="position: absolute; width: 240px; height: 240px; backface-visibility: hidden; transform: rotateY(-90deg) translateZ(120px);">
        <img src="https://assets.lummi.ai/assets/QmSRo6VjDToFt3xUhNZV2qWBDDq4UPSEsbaq8Es2B5aP1i?auto=format&w=1500" style="position: absolute; width: 240px; height: 240px; backface-visibility: hidden; transform: rotateY(180deg) translateZ(120px);">
    </div>
</div>

<br>
<br>


{{< /rawhtml >}}

## HTML Code
```html
<div class="container">
    <div class="cube">
        <img src="https://assets.lummi.ai/assets/QmW239ythzhEUCVHTDxSzCVaB8wkA16E4hiF6MmNwgRSin?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmQHKeemS2YCLkdTBgQxyFbgwE2RHFr1F51AVhQFFcKCAy?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmS3Y6cMYsRAbXF9t5zmRWwqNttpX65Ev9DvykuHsBCFb6?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmSRo6VjDToFt3xUhNZV2qWBDDq4UPSEsbaq8Es2B5aP1i?auto=format&w=1500">
    </div>
</div>
```

## CSS Code
```css
img {
    position: absolute;
    width: 240px;
    height: 240px;
    backface-visibility: hidden;
}

.container {
    width: 240px;
    height: 240px;
    perspective: 800px;
}

.container:before {
    content: '';
    width: 100%;
    height: 100%;
    box-shadow: 
    0   0   75px 20px #0000001a,
    inset 0 0 350px 350px #0000001a;
    position: absolute;
    top: 90px;
    left: 0px;
    transform: rotateX(95deg) translateZ(-80px);
    animation: rotateShadow 16s infinite;
}

@keyframes rotateShadow {
    0% {
        transform: rotateX(95deg) translateZ(-80px) rotateZ(360deg);
    }

    25% {
        transform: rotateX(95deg) translateZ(-80px) rotateZ(270deg);
    }

    50% {
        transform: rotateX(95deg) translateZ(-80px) rotateZ(180deg);
    }

    75% {
        transform: rotateX(95deg) translateZ(-80px) rotateZ(90deg);
    }
    
    100% {
        transform: rotateX(95deg) translateZ(-80px) rotateZ(0deg);
    }
}

.cube {
    height: 100%;
    width: 100%;
    position: relative;
    transform-style: preserve-3d;
    transform: all 0.8 ease-in-out;
    animation: rotate 16s infinite;
}

@keyframes rotate {
    0% {
        transform: rotateY(0deg);
    }

    25% {
        transform: rotateY(90deg);
    }

    50% {
        transform: rotateY(180deg);
    }

    75% {
        transform: rotateY(270deg);
    }

    110% {
        transform: rotateY(3600deg);
    }
}


img:nth-child(1) {
    transform: rotateY(0deg) translateZ(120px);
}

img:nth-child(2) {
    transform: rotateY(90deg) translateZ(120px);
}

img:nth-child(3) {
    transform: rotateY(-90deg) translateZ(120px);
}

img:nth-child(4) {
    transform: rotateY(180deg) translateZ(120px);
}


```



## CSS Code Explanation

1. **Global `img` Styling**
    ```css
    img {
        position: absolute;
        width: 240px;
        height: 240px;
        backface-visibility: hidden;
    }
    ```
    - This block sets the position, size, and backface visibility of all `img` elements. The `backface-visibility` property hides the back side of the images.

2. **Container Styling**
    ```css
    .container {
        width: 240px;
        height: 240px;
        perspective: 800px;
    }
    ```
    - The `.container` class defines the dimensions and perspective for the 3D effect. The `perspective` property gives a 3D space view to the child elements.

3. **Container Shadow Effect**
    ```css
    .container:before {
        content: '';
        width: 100%;
        height: 100%;
        box-shadow: 0 0 75px 20px #0000001a, inset 0 0 350px 350px #0000001a;
        position: absolute;
        top: 90px;
        left: 0px;
        transform: rotateX(95deg) translateZ(-80px);
        animation: rotateShadow 16s infinite;
    }
    ```
    - Adds a shadow effect to the container using a pseudo-element. The shadow rotates with the animation defined in `@keyframes rotateShadow`.

4. **Rotate Shadow Animation**
    ```css
    @keyframes rotateShadow {
        0% { transform: rotateX(95deg) translateZ(-80px) rotateZ(360deg); }
        25% { transform: rotateX(95deg) translateZ(-80px) rotateZ(270deg); }
        50% { transform: rotateX(95deg) translateZ(-80px) rotateZ(180deg); }
        75% { transform: rotateX(95deg) translateZ(-80px) rotateZ(90deg); }
        100% { transform: rotateX(95deg) translateZ(-80px) rotateZ(0deg); }
    }
    ```
    - Defines the animation for rotating the shadow effect around the Z-axis.

5. **Cube Styling**
    ```css
    .cube {
        height: 100%;
        width: 100%;
        position: relative;
        transform-style: preserve-3d;
        transform: all 0.8s ease-in-out;
        animation: rotate 16s infinite;
    }
    ```
    - Sets the 3D transformation for the `.cube` class. The `preserve-3d` property maintains the 3D position of the children elements. The `rotate` animation is applied to this element.

6. **Rotate Cube Animation**
    ```css
    @keyframes rotate {
        0% { transform: rotateY(0deg); }
        25% { transform: rotateY(90deg); }
        50% { transform: rotateY(180deg); }
        75% { transform: rotateY(270deg); }
        100% { transform: rotateY(360deg); }
    }
    ```
    - Defines the keyframes for the rotation animation of the cube around the Y-axis.

7. **Individual Image Positioning**
    ```css
    img:nth-child(1) { transform: rotateY(0deg) translateZ(120px); }
    img:nth-child(2) { transform: rotateY(90deg) translateZ(120px); }
    img:nth-child(3) { transform: rotateY(-90deg) translateZ(120px); }
    img:nth-child(4) { transform: rotateY(180deg) translateZ(120px); }
    ```
    - Positions each image at the sides of the cube using the `nth-child` selector. The images are placed at 90-degree intervals around the Y-axis, with each image translated 120px along the Z-axis to create the cube faces.

## HTML Structure

```html
<br>
<div class="container">
    <div class="cube">
        <img src="https://assets.lummi.ai/assets/QmW239ythzhEUCVHTDxSzCVaB8wkA16E4hiF6MmNwgRSin?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmQHKeemS2YCLkdTBgQxyFbgwE2RHFr1F51AVhQFFcKCAy?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmS3Y6cMYsRAbXF9t5zmRWwqNttpX65Ev9DvykuHsBCFb6?auto=format&w=1500">
        <img src="https://assets.lummi.ai/assets/QmSRo6VjDToFt3xUhNZV2qWBDDq4UPSEsbaq8Es2B5aP1i?auto=format&w=1500">
    </div>
</div>

```

The HTML creates a container div that holds the rotating cube. Inside the cube div, there are four images, each representing a side of the cube. The CSS handles the 3D rotation and positioning of these images to create a cube effect.