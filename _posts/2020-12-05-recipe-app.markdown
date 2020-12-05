---
layout: post
title:  "Final Project Post #5 - Recipe App"
---
![Recipe App Screenshots](/assets/recipe-app-header.png)

## Recipe App

--------------------------------------------------------------------------------

#### What have you done this week?

What I did this week: 
* Couple things that I did this week were:
    * I added some more CRUD operations to my app like deleting a shopping list, & adding a new item to a shopping list.
    * I also implemented a search recipe functionality allowing the user to find a recipe a lot quicker (see code & screenshot below).
    
    
![Search for recipe functionality screenshot](/assets/search.png)

```javascript
$('#searchRecipes').on('keyup change', function (event) {
    let tableRows = [];
    let filteredRecipe = recipes.filter(
        recipe => recipe.title.toLowerCase().includes(event.target.value.toLowerCase())
    );
    filteredRecipe.forEach((recipe) => {
        tableRows += `<tr id="${recipe._id}" onclick="getRecipeDetails(this.id)">
                                <td class="mdl-data-table__cell--non-numeric">${recipe.title}
                                    <br><small class="subtitle-name">${recipe.subTitle}</small>
                                </td>
                              </tr>`
    })
    document.getElementById("recipeNameTable").innerHTML = tableRows;
});
```
***This is the function runs on every keyup change on the search field. It filters through the array of recipe objects 
and returns those that the title matches in the input value.***

#### What do you plan on doing next week?
 
* Test, test, test! Ensure app is working as it should be.
* Fix weird styling bugs.
* Cleanup code.

#### What roadblocks did you encounter and what did you do to overcome them?

* I didn't run into huge roadblocks this week. It was mainly just my own stupid bugs that I created.