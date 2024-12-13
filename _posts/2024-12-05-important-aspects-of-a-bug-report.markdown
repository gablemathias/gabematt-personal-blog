---
layout: post
title:  "Important Aspects of a Bug Report"
date:   2024-12-05 17:11:00 +0000
categories: qa
---

Writing a good, concise, and clear bug report can save you a lot of time explaining and reproducing the bug with your developer friend. That’s why I’m here today: to clarify—or at least refresh—your understanding of how to report that not-so-great issue found in a given application.

**Keep in mind:** Put yourself in the shoes of both the user and the developer. What seems obvious to you might not be clear to them. Sometimes, the best approach is to explain things as if everyone around you were kids. We need to explain things properly (kids always ask “why?”), in a simple way (they’re still learning), and with as few gaps as possible—or ideally none—unless you want them to keep asking “why?” over and over.

## Most important aspects

Title, Steps to Reproduce and Logs.

### Title

**It has to be clear, short and obvious.**
"Product quantity input should only accept positive numbers" 
"Product quantity input should not accept negative numbers"

Both titles clearly convey what is happening. I would say that the first one is more generic, as the problem could involve negative numbers or floating-point numbers. The second one is more specific, and I would personally choose this one.

**Remember:** If you can’t make the title completely clear, provide a concise but informative explanation in the summary section of the description.

**Please don't do that:**
"Product quantity inputted in field X should not accept negative numbers only positive numbers from 1 to 2......."
It is just a title my friend, as I said, create a summary if necessary, the details go after that.  

### Steps to Reproduce

I dare to say that this is the most important one, where you communicate exactly how you reached that issue. Think like holding someone arms showing the way.

1. Enter the link abc.com
2. Go to the field X at the left corner of the page
3. Insert the value -199
4. Click on the button "Add to cart"
5. Product was successfully added to the cart

In this simple example, the issue can be easily reproduced. You talked about where to go, the fields, buttons, where to click and what is expected after the click.

### Logs 

That is where you attach some evidences denoting the place where you found the bug, preferably highlighted. 
Everything that can help and show the problem: screenshots of the webpage, server logs, exceptions.

## What else ?

There are additional elements to include in a bug report, such as the  ID, environment, version, priority, labels, and attributions. These are essential, and I will cover them in greater detail in a separate article about creating a bug report in Jira. For now, I hope this explanation clarifies the core purpose of a bug report and, ideally, saves you from at least one Google/Teams meeting, allowing you to focus on what matters.