Test case 1: login test

// <reference types="cypress" />


it('login test', function () {
    cy.visit('https://www.mytheresa.com/en-de/men.html')

    cy.get('#myaccount').click()

    cy.get('#qa-login-email > #email').type('test1@maildrop.cc')
    cy.get('#qa-login-password > #pass').type('Test@1234')
    cy.get('#qa-login-button > #send2 > :nth-child(1) > span').click()

})


Test case 2: 

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
    cy.get('.large')
    cy.get('#search_mini_form > .form-search > label > .icon',{force: true}).click()






})
