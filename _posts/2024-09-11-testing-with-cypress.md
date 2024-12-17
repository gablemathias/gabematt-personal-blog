---
layout: post
title:  "E2E Automated Pizzahut Ordering with Cypress"
date:   2024-11-09 22:31:12 +0000
categories: testing, automation

---

While searching for tools to learn and apply end-to-end (E2E) automated tests, I found Cypress to be quite impressive! My goal was to find a tool that was easy to set up and had a clean user interface (UI) as a plus. 

For me, the best way to learn is by doing. So, I decided to automate an order on the Pizza Hub website, stopping at the point of payment, and having the opportunity, I also made a more complete approach on another website visiting and filling all the necessary fields to their job application process.   

The code can be found below. I ensured it's easy to read and follow along. 
[Github Repo - Ordering on PizzaHut](https://github.com/gablemathias/pizzahut-cypress/blob/main/cypress/e2e/spec.cy.js)
![Cart](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7x12dy0rwfa32mq3bv02.png)

Here's the process automated:

1. Access the website
2. Click on "New Order"
3. Accept the cookies
4. Fill in blank fields (address, etc.)
5. Select the pizza
6. Modify the dough type
7. Add to cart
8. Reach the payment page
9. Check the cart

I tested them both on Chromium (v130) and Firefox (v129).

![Firefox Test](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/b4v1i5e1u6jsw0vv1lri.png)

![Chromium Test](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/eqw247wj06042vxp4f5t.png)

**For the job application process**, I ensured to include all the necessary information on the repository, with images and videos to follow along! 
[Github Repo](https://github.com/gablemathias/init-cypress)

There's also some examples of creating and documenting user stories  using [Jira](https://www.atlassian.com/software/jira) and [Confluence](https://www.atlassian.com/software/confluence).

## Impressions

I've found that the methods `cy.get` and `cy.should` were my best friends. Cypress has amazing [documentation](https://docs.cypress.io/api/table-of-contents) and [courses](https://learn.cypress.io/testing-your-first-application) to get you through everything pretty well and acquire a solid knowledge. I still have a lot to learn!

### Pros
My first two impressions of this tool were the real-time reloading and "time travel" features. Every time I saved the code I changed, the test automatically reloaded, making it incredibly fast to check for any possible errors and move on. I was able to examine every step made by the program and the web-app's state at each point. I can't say how much time this saves and how it allowed me to focus on what really matters: what I wanted to test and whether it was working properly or not.

### Cons

Well, It doesn’t support WebKit Browsers Engine (Safari) and mobile testing natively. It’s mainly suited for JavaScript applications and involves huuuuge DOM manipulation, which can be problematic for some applications that manipulate the DOM after the page loads. 
I also have the feel that certain complex scenarios might slow down the execution speed of the tests. Using more assertions could potentially help with this, but I am not sure since this particular test wasn’t resource-intensive.