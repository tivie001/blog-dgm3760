---
layout: post
title:  "Final Project Post #3 - Recipe App"
---
![Recipe App Screenshots](/assets/recipe-app-header.png)

## Recipe App

--------------------------------------------------------------------------------

#### What have you done this week?

What I did this week: 
* A main feature that I implemented in my app this week was adding CRUD operations to the front and backend for the recipe and list features:
    * A user can now edit a recipe's details (add more ingredients, directions, delete them, edit details, etc.)
    * A user can now delete a todo item as well.
* I also did some testing and fixed some bugs that were related to the way the data was being parsed and handle to and from the DB.
    
![Edit Recipe Screenshot](/assets/edit-recipe.png)
![Delete List item Screenshot](/assets/edit-list.png)

```javascript
function toggleEditRecipe() {
    const recipeDetails = selectedRecipeDetails[0];
    console.log(recipeDetails);
    document.querySelector( '#editTitle').value = recipeDetails.title;
    document.querySelector( '#editSubTitle').value = recipeDetails.subTitle;
    document.querySelector( '#editTotalHours').value = recipeDetails.totalHours;
    document.querySelector( '#editTotalMin').value = recipeDetails.totalMins;
    document.querySelector( '#editRating').value = recipeDetails.rating;
    document.querySelector( '#editDifficulty').value = recipeDetails.difficulty;
    document.querySelector( '#editPrepHours').value = recipeDetails.prepHours;
    document.querySelector( '#editPrepMins').value = recipeDetails.prepMins;
    document.querySelector( '#editPrepDetails').value = recipeDetails.prepDetails;

    ingredientsContainer = document.getElementById( 'editIngredients');
    recipeDetails.ingredients.forEach((ingred, index) => {
        var str = `<section id="${index}"><div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label editable-inputs">
                             <input class="mdl-textfield__input edit-ingredient" value="${ingred}" id="${index}" type="text" id="editIngredient">
                             <label class="mdl-textfield__label" for="editIngredient">New Ingredient</label>
                         </div> 
                         <button type="button" class="mdl-button mdl-button--icon mdl-js-button mdl-js-ripple-effect trash-icon" id="${index}" onclick="removeIndex(this.id)">
                            <i class="material-icons">delete</i>
                         </button></section>`
        ingredientsContainer.insertAdjacentHTML( 'beforeend', str );
    })
    directionsContainer = document.getElementById( 'editDirections');
    recipeDetails.directions.forEach((direct, index) => {
        var str = `<div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label editable-inputs">
                             <input class="mdl-textfield__input edit-direction" value="${direct}" id="${index}" type="text" id="editDirection">
                             <label class="mdl-textfield__label" for="editDirection">New Step</label>
                         </div>
                         <button type="button" class="mdl-button mdl-button--icon mdl-js-button mdl-js-ripple-effect trash-icon" onclick="removeIndex()">
                            <i class="material-icons">delete</i>
                         </button>
                        `
        directionsContainer.insertAdjacentHTML( 'beforeend', str );
    })

    ingredientsContainer = document.querySelectorAll( '.editable-inputs');
    ingredientsContainer.forEach(input => {
        input.removeAttribute("data-upgraded");
        componentHandler.upgradeDom();
    })
}
```
***This is how I toggled the HTML to be editable inside the edit recipe modal.***

#### What do you plan on doing next week?
 
* Do some research on using an image API or Pexels to save images to MongoDB.
* Finalize a few CRUD operations for the lists (i.e. delete a list, add a todo item).

#### What roadblocks did you encounter and what did you do to overcome them?

* Saving images to MongoDB! I still haven't been able to figure it out.
* Working with a CSS framework to get it to behave properly when inserting HTML from JS.
