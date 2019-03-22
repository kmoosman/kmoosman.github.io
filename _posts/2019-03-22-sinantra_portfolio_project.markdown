---
layout: post
title:      "Sinantra Portfolio Project"
date:       2019-03-22 22:52:27 +0000
permalink:  sinantra_portfolio_project
---


Last month, I sold my house, all of my belongings and hit the road as a digital nomad. This Sinatra Project arrived right on time to help me track my adventures! 

I absolutely loved this project. It felt like it came together so quickly and all of my learnings are finally compounding, so I no longer feel like such an imposter. It's exciting to see how quickly you build with Ruby. 

My biggest challenge with this project was the CSS. Fancy styling wasn't required as part of the specs but it look a little piece of my soul everytime I ran shotgun and was greeted by an unformatted page *cringe*.

It took me far longer than I care to admit to figure out where in the world to put my stylesheet, so here's a quick run down of my findings for anyone else who may find themselves with the same dilemma. 

1. Create a Public folder at the root level of your project (this is where your application looks for the css file) 
2. Add a css file to the public folder (I named mine style.css) 
3. Link to the stylesheet in your layout.erb file 
```
<link rel="stylesheet" type="text/css" href="/style.css">
```

**NOTE** 
If your styles don't apply when you refresh the page, try a hard refresh (cmd + shift + r). I couldn't for the life of me figure out why styles weren't applying and until I uncovered that little secret! 

Overall, I'm pretty satisfied with the project, I had a lot of fun building it and I'm excited to add a few new adventures to my page. 




