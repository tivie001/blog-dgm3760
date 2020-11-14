---
layout: post
title:  "Final Project Post #2 - Recipe App"
---
![Recipe App Screenshots](/assets/recipe-app-header.png)

## Recipe App

--------------------------------------------------------------------------------

#### What have you done this week?

What I did this week: 
* A main feature that I implemented in my app this week was creating a **shopping list**: 
    * A user can create a shopping list and add ingredients to it on creation. It then saves to the database and
can be accessed/displayed throughout the app.
    * A user can check off ingredients and it will cross it off and grey it out for them.
    
![Recipe App Lists Screenshots](/assets/recipe-lists.png)

* In addition to the list functionality, I also added the ability to add ingredients from any 
recipe to a shopping list (see screenshot below).

![Recipe App Lists Screenshots](/assets/add-ingreds.png)
```javascript
app.put('/api/addIngreds/:id', (req, res) => {
    // let newItems;
    List.findById(req.params.id, (err, list) => {
        if (err)
            console.log(handleError(err));
        const newItems = [...list.items, ...req.body]
        list.update({items: newItems}, (err) => {
            if (err)
                console.log(err);
            List.find((err, list) => {
                if (err)
                    console.log(handleError(err));
                res.json(list);
            })
        })
    })
})
```
***I used the spread operator to add the new ingredients (todo items) to the existing ones.***

#### What do you plan on doing next week?
 
* Figure out how to save images to MongoDB and get the finalized relational structure of my database.
* Work on enabling the user to edit recipe details and delete list items.
* Work on linking all the app together with links and a better UI experience.

#### What roadblocks did you encounter and what did you do to overcome them?

* Saving images to MongoDB! I still havent been able to figure it out.
* Working with a CSS framework to get it to behave properly when inserting HTML from JS.