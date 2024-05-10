Javascript
=========

Due to our project being a web-app, we are using javascript for the backend functionality.

We have 2 main javascript files: `main.js` and `build.js`.

Main.js
-----------

main.js handles the landing page, PC brand selection and budget selection.

main.js functions
------------------
createCard: This function creates the website elements to select between AMD and Intel.

updateState: Changes the url state.

selectBrand: Displays the cards created with createCard.

switchToBudgetSelection: Creates the slider used to select the budget and changes the test shown based on the current slider level.

Build.js
-----------

build.js handles the selection of parts and the PC config generation. 

build.js functions
-------------------

openCollapsePartsMenu: displays and hides the part selection menu.

loginInit: when the login button is clicked, creates the login and signup displays

openCollapseGenerationMenu: displays and hides the generated configs.

displayAutoGenSettings: If a part is selected specifically, other inputs are hidden to avoid database errors.

displayBudget: Displays the budget and selected brand on the ribbon at the bottom of the screen.

displayPart functions: Each of the displayPart functions gets all of the appropriate parts from the database and displays them in a bar for the cases or in a dropdown menu for the others.

generateConfigsArray: Takes the values from the payload passed to it and passes it to the gatherPartObjects functions to get the auto-generated parts. The function then passes the parts into an array and then loops through to find the wattage and total price

startGeneration: gets the budget from the url and adds it to the payload

gatherUserParameters: gets the PC parameters from the inputs and adds them to the paylaod

getValidPart functions: finds the parts from the database based on the compatability such as a power supply providing enough power for the other parts.

gatherPartObjects: if the user wants a part to be auto-generated then the function will call the appropriate getValidPart function to find the part.

displayConfigurations: Displays the config based on what was generated and selected. Also the displays the stats of the config such as clock speed. Adds a save button to each of the configs to let any user that is logged in to save a config to their account.

calculateNumberOfMoreConfigs: Calculates the number of other configs generated

loadMoreConfigs: Displays 10 more configs if there are any left to display.

config.js
----------
Displays the configs the user has saved to their account

config.js functions
-----------

Anonymous function: that fetches the configs from the database, turns them into a json object and then loops through them to display them all.
