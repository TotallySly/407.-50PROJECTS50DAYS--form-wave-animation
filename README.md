## 408.- 50 Projects 50 Days - Form Wave Animation

### What was the project about?

The project is part of the 50 Projects in 50 Days with Brad Travesy via Udemy. The course is a code-a-long to further cement skills used within HTML, CSS, and Vanilla JavaScript.

This particular project added a very cool animation effect on a generic login page. When the user clicks within the Email or the Password label of the form, each of the respective text moves up with a transition delay. This creates a cool little wave effect animation.

[Form Wave Animation](https://totallysly.github.io/408.-50PROJECTS50DAYS--form-wave-animation/)

#### CSS

As with the other recent projects, the CSS was rather straight forward. It had a lot of emphasis on class specificity.

It introduced [cubic-bezier( )](https://css-tricks.com/advanced-css-animation-using-cubic-bezier/) for the wave animation effect. However, I will read into this, but on the surface it feels like advanced mathematics, and as such I am not sure how in deph I will go into the need of having this within my arsenal.

#### JavaScript

The JavaScript itself was rather minimal, however it introduced new concepts that I have not learnt about, but will need to add into my skillset.

In order to create the wave animation effect, each of the letters within the word **'Email'** and **'Password'** needed to be enclosed within a span which was then styled.

    const  labels = document.querySelectorAll('.form-control label')

    labels.forEach((label) => {
        label.innerHTML = label.innerText
    	    .split('')
    	    .map((letter, index) => `<span style="transition-delay:${index * 75}ms">${letter}</span>`)
    	    .join('')
    })

I have touched (albeit on an absolute basic level) using arrays and the various methods (in this case `.split(' ')` and `.join(' ')` . The idea is that each letter is then split into an array. So the first index will be **'E'**, then **'M'** etc. And then it is joined back into a string with `.join( )`.

Now `.map( )` is a JavaScript method I have not used before. From what I can understand, it is a method in which you can manipulate array into a new array - all without changing the original array.

[MDN - array.map( )](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

[W3Schools - array.map( )](https://www.w3schools.com/jsref/jsref_map.asp)

In this tutorial, we wanted to manipulate each letter within the array by adding a `<span>` and some inline styling around each individual letter within the array.

[![Spans Created with the .map( ) method](https://i.postimg.cc/BQcVZmX9/Screenshot-20230102-161400.png)](https://postimg.cc/Ln5TNBtN)

The above `<span style="transition-delay:Xms>x</span>"` has been added dynamically via JavaScript, using the different string and map methods within JavaScript.

This is something that I have just seen in action for the first time, so I have to learn about this in more depth.
