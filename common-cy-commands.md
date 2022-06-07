# Useful Cypress Commands & Assertions
>For a full list you can head [here](https://docs.cypress.io/api/table-of-contents), but this is just for the bread and butter commands which you will be finding yourself using a lot if you do any Cypress testing.

## Commands 

### cy.visit(`url`) 
> Tells Cypress to go to the desired url for the tests, this is usually done within a `beforeEach(...)` block so that each test begin with a visit to the url.

### cy.get(`selector`)
> Probably the most common command used in Cypress testing; 'gets' and element from within the DOM using a range of possible 'selectors'. These could be the element's id, its CSS path or as a very last resort its xPath. There's a decent guide within the [Cypress docs](https://docs.cypress.io/guides/references/best-practices#Selecting-Elements) on choosing the best selectors.

### .click()
> After getting an element, e.g. a button, click it.
> 
> There's also the ability to double-click, using the `.dblclick()` command.

### .type(`string of text{enter}`)
> After getting an element, e.g. a text box, type into it. The `{enter}` is optional, but is there in case you would like Cypress to hit the enter key after typing in the text proceeding it.

### cy.check(`selector`)
> This is similar to click() except that it is used for check/tick-boxes

### .contains(`value`)
> Finds the first element in the DOM that matches the given value. You can use this in multiple ways and it is best outlined in the Cypress docs.

## Assertions
Assertions usually follow a pattern of `cy.get(element).assertion(condition[s])`

Cypress bundles [Chai](https://docs.cypress.io/guides/references/bundled-tools#Chai), [Chai-jQuery](https://docs.cypress.io/guides/references/bundled-tools#Chai-jQuery), and [Sinon-Chai](https://docs.cypress.io/guides/references/bundled-tools#Sinon-Chai) to provide built-in assertions. You can see a comprehensive list of them in [the list of assertions reference](https://docs.cypress.io/guides/references/assertions).

### .should(`chainer` , _optional_`String value`)
> Within `.should()` there are many possible assertions you can make, and it's fairly intuitive to use if you're using an IDE. Generally the types of assertions you can make fall under three categories, one of which won't be covered today. These are 
> * `should('chainer', 'value')`
> * `should('assertion')`
> * `should(callbackFunction)` (not covered today)







