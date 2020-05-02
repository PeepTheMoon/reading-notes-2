In class notes from 5/1/20

header and footer can go in the app.js file because it's going to be on every page.  

children talk to parents with a callback

parents talk to children with props

component heirarchy-- there's a top level (parent) and a bottom level.  You have to go against the flow of data to get bottom componenets to "talk" to the top level componenet.

stateful v presentational componenets:

presentational only take in props.

Stateful componenets maintain state.

Starting at the top level when building is usually better, starting at the place where you're going to put everything.  

If two things need the same state or data, put it in the parent of those two componenets.

break things down into verifiable steps because then you can easily debug and make sure each each single problem is solved and working.  Too may things at once means it's harder to find out which thing isn't working.

The magic thing to make something render in react is to change the state and check to see if it updated in the browser

To deploy:

npm install gh-pages --save-dev to deploy your pages. type in terminal.

"homepage": "http://alchemycodelab.github.io/rick-and-morty-1"

use the above in package.json.  change gitname on line to your github and the last part to the name of your repo.

at the bottom on the scripts object in package.json, add:
"predeploy": "npm run build", "deploy": "gh-pages -d build"

afterwards in your terminal type nmp run deploy
it will then build the page and deploy it.

sometimes when you copy quotation marks it doesn't work.  If this is the case, delete and retype them.

//////////////////////////////////

When linking pages in react, you need to update app.js with routers.
1. home page needs to go to the list page
1. id link needs to go to the details page
1. on details page file, use compenentDidMount and fetch pokemon items.  We can console.log(fetchedData) to be sure it's receiving the info.
1. render the pokemon item

///////////////////////////////////////////

To include pagination in the app:

## Next Button
*We want to *implement a next buttom when we notice that the pages in the object in the api are greater than 1.

*if pages > 1, show the next/prev button
results console.log(next url) to make sure its working.

*on clicking the next button, we want to fetch the next 
console.log(results)


*we want to *set results in state

*tech debt: hide prev button on first page



## Prev Button
*if pages > 1, show the next/prev button
results console.log(next url) to make sure its working.

*on clicking the next button, we want to fetch the next 
console.log(results)

*we want to *set results in state

*tech debt: hide next button on last page

## Sync input to URL
*put the search query in the url on change
*if I paste a url with a searchQuery in it, I want that to go in the input and the the initial fetch includes that searchQuery.

## Sync page to URL
*put the pagination in the url on change
*if I paste a url with a page in it, I want that to go in the input and the the initial fetch includes that pagination.

