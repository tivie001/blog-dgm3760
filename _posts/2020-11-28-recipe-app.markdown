---
layout: post
title:  "Final Project Post #4 - Recipe App"
---
![Recipe App Screenshots](/assets/recipe-app-header.png)

## Recipe App

--------------------------------------------------------------------------------

#### What have you done this week?

What I did this week: 
* I'VE FINALLY FIGURED OUT HOW TO SAVE PICTURES FOR THE RECIPES IN THE DATABASE! I decided to use an image API, Unsplash, to host all the 
images and I just store the urls in my database. How it works is when a user toggles the modal to add a new
recipe one of the options is to search for the dish they are making or something related to it. Then when the user clicks
search it sends a request to Unsplashes API which then returns 20 images based of the users query. From there a user can
click on an image and select which one they want to use for the recipe. Finally, when a user saves the recipe it will store
the selected images URL in the database. (See screenshot & code snippet below for more details).
* I also implemented the functionality for a user to delete a recipe.
    
![Add New Recipe (with image functionality) Screenshot](/assets/image-select.png)

```javascript
function searchImages(){
    const searchTerm = document.querySelector('#imgSearch').value;
    const imageContainer = document.getElementById("imageContainer");
    let newImg;
    fetch(imageURL + `search/photos?client_id=${API_KEY}&query=${searchTerm}&orientation=landscape&per_page=20`, {
        headers: {
            "Accept-Version": "v1"
        }
    })
        .then((res => res.json()))
        .then(function(res) {
            res.results.forEach((img) => {
                images.push(img);
                if (img || img !== undefined)
                    newImg = `<img src=${img.urls.regular} alt="${img.alt_description}" id="${img.id}" width="200" height="175" class="search-images" onclick="imageSelect(this.id)"/>`
                    imageContainer.insertAdjacentHTML( 'beforeend', newImg);
            })
        }).catch(function(err) {
        console.log(err);
    })
}
```
***This is the function that queries for and returns 20 images at a time when a user searches for an item.***

#### What do you plan on doing next week?
 
* Finalize a few CRUD operations for the lists (i.e. delete a list, add a todo item).

#### What roadblocks did you encounter and what did you do to overcome them?

* I didn't run into huge roadblocks this week. It was mainly just my own stupid bugs that I created.