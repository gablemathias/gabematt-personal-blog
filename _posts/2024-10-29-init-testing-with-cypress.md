---
layout: post
title:  "E2E Testing including Test Case Process"
date:   2024-10-29 14:11:29 +0000
categories: testing, complete

---
The goal here is to show a proper test case built and how it was tested manually and functionally in a professional manner. 
Using tools such as Jira to design and execute the test cases is awesome.
In a professional environment that uses Jira/Confluence/BitBucket (Atlassian) Tools, learning how to write a proper test case and execute it improves the productivity, and when something goes wrong, you know where to check and do the regression.  

### The overall process:

1. Create user stories with Jira
2. Document with Confluence
3. Verify the process through manual UI test cases
4. E2E Automated tests
5. Report results

**Test Scenario:** Successfully send a Job application through the career page on https://www.init.pt/en/career-init-dcp

**Test Steps:**

    1. The user navigates to init.pt
    2. The user clicls the 'Career' button.
    3. The user scrolldown the page and clicks 'Nothing suitable? Send us an unsolicited application' button.
    4. The user fills the form accordingly.
    5. The user clicks the 'Send application' button.

**Prerequisites:** A curriculum and an ID document to attach.

**Browser:** Chromium v130. Firefox v129

**Test Data:** Personal information, curriculum, check-boxing preferences

**Expected/Intended Results:** Once user fill and checkbox the form, the application will be send correctly.   

**Actual Results:** As Expected

**Test Status – Pass/Fail:** Pass

![image](https://github.com/user-attachments/assets/771cf138-5478-4775-acf4-4481b5eac039)

**Two specs, one for each task (Cypress)**
![Screenshot from 2024-10-29 14-54-14](https://github.com/user-attachments/assets/c8565f1e-36ff-4055-af9e-205679d4e73b)

**The second test passing (Cypress)**

![Screenshot from 2024-10-29 14-57-43](https://github.com/user-attachments/assets/aa27c8ec-ad8d-4a0a-ac30-2cee41929a8e)

**Demo - visiting the career webpage and filling the form (E2E Automated Test)**

[E2E - Filling Form](https://github.com/user-attachments/assets/66a9186f-bb07-408c-a5fc-c32ae7bbb122)

**Demo - visiting and analysing stories in**
[Jira](https://github.com/user-attachments/assets/b0f3a1a1-13f0-4b7f-84ed-a47d19ef3a1d)

**Demo - the documentation created in**
[Confluence](https://github.com/user-attachments/assets/4cbf9a20-7959-4b10-95be-0836cc3df92f)

## Images of the process on Jira and Confluence 
### Jira
![stories-Board](https://github.com/user-attachments/assets/b533d88c-3373-4188-a15a-2028d999ec83)

![moving board](https://github.com/user-attachments/assets/921e6614-5d72-4c33-bc32-bb697fe02f50)

![story details](https://github.com/user-attachments/assets/4ef72ead-f022-4c4b-ab75-81e2fcb1dfc1)

![finishing-one-story](https://github.com/user-attachments/assets/a3423d5f-8d2c-48d5-8789-fd1941adbc17)

![second-story](https://github.com/user-attachments/assets/1849ac77-bdb2-48ee-a1c7-2e8e47f111bc)

![finish-sprint](https://github.com/user-attachments/assets/714fa49d-6797-4358-87c8-74849abc72de)

### Confluence
![1](https://github.com/user-attachments/assets/8b8d407d-f1fe-43cd-8132-eee4cf8c1c53)
![2](https://github.com/user-attachments/assets/64b8bc31-b767-46ee-ad0e-ae1d06b3a0d8)


## Conclusion
Jira gives me excellent control over my tasks and stories. When a story needs to be split into different tasks, it provides the necessary tools
and management features.

Documenting in Confluence allows me to review my past work and helps with future tasks. It's crucial to link everything here and add as
much information as possible for anyone to reference. This includes technical issues, troubleshooting, know-how, and workshops.

Cypress is an outstanding tool for creating End-to-End Automated Tests. It uses the target web application and verifies with its auto-reload
feature every time I save the code.

### There is always room for improvement
Revisiting and refactoring the `do_job_application.cy.js` could be a nice idea. I have used a lot of `wait` function calls to pure purpose of
demonstration.
