---
sidebar_position: 4
---

# 🌐 Examples of browser automation
Lets see how we can use the power of Playwright MCP Server to automate our browser and do webscrapping

### Using Different Browser Types

Playwright MCP now supports multiple browser engines. You can choose between Chromium (default), Firefox, and WebKit:

```bdd
Given I navigate to website "https://example.com" using the "firefox" browser
And I take a screenshot named "firefox-example"
Then I navigate to website "https://example.com" using the "webkit" browser 
And I take a screenshot named "webkit-example"
```

When you send these commands to Claude, it will open the website in Firefox first, take a screenshot, then switch to WebKit and take another screenshot, allowing you to compare how different browsers render the same website.

### Scenario in BDD Format
```bdd
Given I navigate to website http://eaapp.somee.com and click login link
And I enter username and password as "admin" and "password" respectively and perform login
Then click the Employee List page 
And click "Create New" button and enter realistic employee details to create for Name, Salary, DurationWorked,
Select dropdown for Grade as CLevel and Email.
```

Once I enter the above text in ***Claude Desktop Client*** I should see Claude desktop giving me prompt to perform operation 
by opening real browser like this

![Playwright MCP Server](./img/mcp-execution.png)

And once the entire test operation completes, we will be presented with the entire details of how the automation did happened.

![Playwright MCP Server](./img/mcp-result.png)