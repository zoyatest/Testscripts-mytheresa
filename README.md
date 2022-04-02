Test case 1: Login test-  As a tester owner, I want to verify I can log in to
https://www.mytheresa.com/ende/men.html.
Hint: you can use https://maildrop.cc/ to create an account on the fly.


// <reference types="cypress" />


it('login test', function () {
    cy.visit('https://www.mytheresa.com/en-de/men.html')

    cy.get('#myaccount').click()

    cy.get('#qa-login-email > #email').type('test1@maildrop.cc')
    cy.get('#qa-login-password > #pass').type('Test@1234')
    cy.get('#qa-login-button > #send2 > :nth-child(1) > span').click()

})


Test case 2:  As a tester, I want to make sure no JavaScript errors when you visit
https://www.mytheresa.com/en-de/men.html
● As a tester, I want to check if a page is returning the expected status code
○ Fetch each link (e.g. <a href=””/> on
https://www.mytheresa.com/en-de/men.html) and visit that link to verify that:
■ the page returns 200 or 30x status codes
■ the page returns no 40x status codes

/// <reference types="cypress" />


it('Link test', function () {
    cy.visit('https://www.mytheresa.com/en-de/men.html')
    cy.get('.nav-primary > :nth-child(10) > .has-children > .item-name').click()
    cy.get('.active > .level0.has-children > .item-name')
    cy.get(':nth-child(12) > .level0.has-children > .item-name').click()
    cy.get(':nth-child(13) > .level0.has-children > .item-name').click()
    cy.get('.nav-primary > :nth-child(14) > .has-children > .item-name').click()
    cy.get(':nth-child(15) > .level0.has-children > .item-name').click()
    cy.get(':nth-child(16) > .level0.has-children > .item-name').click()
    cy.get('.header-minicart > .skip-link > .label').click()
    
    
    

})


Test case 3 : 

As a product owner, I want to see how many open pull requests are there for our
product. You can use https://github.com/appwrite/appwrite/pulls as an example
product
● Output is a list of PR in CSV format with PR name, created date and author


/// <reference types="cypress" />


it('product owner test', function () {
    cy.visit('https://github.com/appwrite/appwrite/pulls')
    cy.get('[data-content="Pull requests"]').click()
    cy.get('.min-width-0 > .head-ref > .no-underline > :nth-child(2)').click()
    cy.get('.btn.ml-2').click()
    cy.get('.navigation-focus').click()
    cy.get('#raw-url').click()
    


})

