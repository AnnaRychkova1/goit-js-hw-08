# goit-js-hw-08

# Task — Gallery of images

Create a gallery with the ability to click on its elements and view in full size
image in a modal window. Watch a demo video of the gallery.

Creating a gallery is a complex task that is best broken down into several
simpler subtasks, performing each of which you will get closer to the final one
goals This process is called problem decomposition.

## 1 - Gallery layout

It is logical to start by creating something where we will add gallery elements.
To do this, add a gallery container tag to the HTML code — an unordered list of
"gallery" class.

```
<ul class="gallery"></ul>
```

## 2 - Array of images

To create gallery elements you will need data. Add this array of objects to your
JavaScript file. Each object represents one gallery element.

- preview — link to a small version of the image for the gallery card
- original — a link to a large version of the image for the modal window
- description — text description of the image, for the alt attribute of the
  small image and the caption of the large image in the modal.

```
const images = [ { preview:
"https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820__480.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820_1280.jpg",
description: "Hokkaido Flower", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/14/22/05/container-4203677_1280.jpg",
description: "Container Haulage Freight", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/16/09/47/beach-4206785_1280.jpg",
description: "Aerial Beach View", }, { preview:
"https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619__340.jpg",
original:
"https://cdn.pixabay.com/photo/2016/11/18/16/19/flowers-1835619_1280.jpg",
description: "Flower Blooms", }, { preview:
"https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334__340.jpg",
original:
"https://cdn.pixabay.com/photo/2018/09/13/10/36/mountains-3674334_1280.jpg",
description: "Alpine Mountains", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/16/23/04/landscape-4208571_1280.jpg",
description: "Mountain Lake Sailing", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/17/09/27/the-alps-4209272_1280.jpg",
description: "Alpine Spring Meadows", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/16/21/10/landscape-4208255_1280.jpg",
description: "Nature Landscape", }, { preview:
"https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843__340.jpg",
original:
"https://cdn.pixabay.com/photo/2019/05/17/04/35/lighthouse-4208843_1280.jpg",
description: "Lighthouse Coast Sea", }, ];
```

## 3 - Layout of gallery elements

You have a container in which you can add elements galleries, and the data by
which they can be created. It's time to fill the gallery marking

Use the images object array and this gallery element HTML template and create in
the JavaScript code of the element markup, then add all the markup inside
ul.gallery. Do not add any HTML tags other than those contained in this
template.

```
<li class="gallery-item">
  <a class="gallery-link" href="large-image.jpg">
    <img
      class="gallery-image"
      src="small-image.jpg"
      data-source="large-image.jpg"
      alt="Image description"
    />
  </a>
</li>
```

- In the src attribute of the `<img>` tag, we specify a link to a small version
  of the image.
- For the alt attribute, we use the description of the image.
- Link to large image must be stored in the data-attribute source on the `<img>`
  element, and pointed to href link.
- Note that the image is surrounded by a link that has the href attribute points
  to the path to the image file. So you can click on it cause the image to be
  downloaded to the user's computer. Ban this one default behavior.

## 4 - Styles

Add styling to the gallery according to the layout.

## 5 - Delegation

It's time to add the functionality of listening for clicks on elements gallery
and getting a link to a large image when clicked. For this use the delegation
technique on ul.gallery. So far when clicking on an element gallery display a
link to a large image in the console.

## 6 - Connecting the library

The basicLightbox library provides a fully functional modal window that is
perfect for our task. Use the jsdelivr CDN service and add a link to the
library's minified (.min) JS and CSS files to the HTML file.

## 7 - Modal window

Add your code so that when you click on the gallery element the modal window of
the connected library opened. In order to find out how initialize a modal window
in your code and how to use it, see with documentation and examples.

## 8 - Large image

Use your code to get a link to the large one image to replace the value of the
src attribute of the `<img>` element in the modal window before opening. Use the
ready markup of a modal window with an image from the examples of the
basicLightbox library.

## 9 - Closing from the keyboard

Add the functionality of closing the modal window after pressing the Escape key.
Make it so that listening to the keyboard is only as long as the modal window is
open. The basicLightbox library contains a method for soft closing of the modal
window.

# What the mentor will pay attention to during the inspection:

- The live page displays a gallery of images from the images array
- The image gallery is stylized according to the layout
- Gallery data is generated dynamically in JS
- When listening to the click event on gallery items used acceptance of
  delegation
- When clicking between gallery elements, nothing happens
- The basicLightbox library is connected
- When you click on an element of the gallery, a connected modal window opens
  library that contains an enlarged version of the clicked image
- Implemented the functionality of closing the modal window after pressing the
  key Escape
- Keyboard event listening happens only as long as it is open modal window
