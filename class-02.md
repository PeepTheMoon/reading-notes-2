# Applying Atomic Design

Breaking down the visialization of a page into componenets helps to break a page into it's ocmpnenets.

Start big and work your way down, first by 
1. visializing the page
1. setting up a template, or skeleton
1. mapping out the organisms: large sections you can easily extract from the page, like header, main content area, divs
1. Identifying the molecules: things that are repeated in several places on the page, like a list of users 
1. Identifying the atoms: include basic html elements like form labels, inputs, buttons, etc that can't be broken down any further without ceasing to be functional.

When you go to build the the page, start building in reverse, from the bottom up. (atoms).

strive for component driven frameworks that are reproduceable and reuseable.  This helps to avoid styling conflicts, especially with older styling.

## https://reactjs.org/docs/thinking-in-react.html

follow the single responsibility principle-- ideally each component should do only ine thing.

 In simpler examples, it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up and write tests as you build.

 ### https://www.thoughtworks.com/insights/blog/ui-components-design

 This article stresses the importanct of designing code in components that are independent and reuseable 

 establishing a common language between design team and engineers is helpful 

 #### https://www.sitepoint.com/callbacks-javascript/

 a callback is function to be executed after another function has finished executing.

 functions are objects in javascript and can take other functions as arguments and can be returned by other functions.  these types of functions are higher order functions, and functions that are passed as an argument and subsequently called by the function that recieves it are callback functions.

 we need callbacks because javascript is an event-driven language an dinstead of waiting for a response before moving on, it will keep executing while listening for other events.

##### classes in javascript

a class is a kind of function

###### object methods
https://javascript.info/object-methods

objects are created to represent objects in the real world and things in the real world can act.  actions are represented in javascript by functions in properties.

A function that is the property of an object is called its method.

It’s common that an object method needs to access the information stored in the object to do its job.

To access the object, a method can use the this keyword.





