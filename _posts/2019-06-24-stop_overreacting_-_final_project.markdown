---
layout: post
title:      "Stop OverReacting - Final Project"
date:       2019-06-24 15:40:52 -0400
permalink:  stop_overreacting_-_final_project
---


React, Redux and Rails - the tripple threat? 

Well, they certainly were the tripple threat to my sanity for a hot minute as first I dipped my toes in to test the water. 

As I began building out my project, one of my main hurdles I encountered was how to update my state in Redux for a nested array. So I wanted to recap here what went wrong and how I resolved the issued to hopefully help out anyone else who may get stuck along the way. 

In the lessions, we covered how to add items to the store and manage state with Redux, which is pretty straight forward. However, updating a specific nested array without losing the rest of my state, this one sent me for a loop. 

I was trying to updated a nested object. I had a list of events at the top, I needed to drop into the first event (or whichever event was updated), retain the rest of the state for that event, then drop one level lower to update the transonders array. 

After many attempts I eventually was able to successfully update my state, however when you update your state with ...state, you're turning it into an object. I was using map to display a list of all of my transponders, so once my list of transponders became an object instead of an array, we ran into some trouble. 

The magic code that finally set me free? 
```
function updateObjectInArray(array, action) {
  return array.map((item, index) => {
    if (index !== action.index) {
      // This isn't the item we care about - keep it as-is
      return item
    }

    // Otherwise, this is the one we want - return an updated value
    return {
      ...item,
      ...action.item
    }
  })
}

```

This can be found in the [redux docs ](https://redux.js.org/recipes/structuring-reducers/immutable-update-patterns) and it talks about how to write a function to update your array. The return value of the function, is an array that you then can use to update your state with redux. 

I spend 2 days hung up on this issue. So I hope this can help unblock someone else who may encounter a similar issue in the future. 

This was a fun and challenging project and I'm glad I encountered this issue as I learned alot about Redux and React along the way that I had not encountered through the lessions yet. 

So overall, we'll call it a win with the moral of the story being, when in doubt - always check the docs. 
