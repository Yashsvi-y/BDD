## Selenium-Cucumber-Java

This repository contains a collection of sample projects and libraries that demonstrate how to use `selenium-cucumber-java`, a BDD (Behavior-Driven Development) framework with Cucumber  and Java. The projects showcase automation script development and utilize reporters such as Extent Report.

### Installation & Prerequisites


1. Intellij IDE
2. Required Intellij Plugins:
   - Maven
   - Cucumber


## Framework Setup

To set up the framework, you can either download the zip or clone the repository from https://github.com/Yashsvi-y/BDD.git, or download the ZIP file from email and set it up in your local workspace.

## Application Under Automation: Website used for Test Automation is as below:
https://www.kapruka.com/

### Extent Reports

The framework utilizes the Extent Reports to generate HTML test reports. Use link as a Reference: https://www.extentreports.com/docs/versions/5/java/

## BDD Automation with Cucumber-Java and Page Objects

In this repository, we encourage the use of Behavior-Driven Development (BDD) with Cucumber and Java to develop automation scripts. 

Tests are written in the Cucumber framework using the Gherkin syntax. If you're new to Gherkin and Cucumber, you can find more information at https://cucumber.io/docs. A typical test will have a structure similar to this:

```gherkin
Feature: Search Page Validation

  @Search
  Scenario: Testing Search
    When I login with the website
    Then I should see dashboard
    When I enter text to Search and click on Search button
    Then I should see Results
    When I enter invalid text to Search and click on Search button
    Then I should not see Results
    When I enter text to Search and click on Search button
    Then I should see Results

  @Search
  Scenario: Testing Search Pagination
    When I login with the website
    Then I should see dashboard
    When I enter text to Search and click on Search button
    Then I should see Results
    When I click on Next
    Then I should see Results on Second Page
```

## The Page Object Design Pattern

To better organize your test code and make it more maintainable, we recommend using the Page Object Design Pattern. With this pattern, the UI elements of your web application are modeled as objects within the test code. This approach reduces code duplication and allows easy updates if the UI changes. Writing and maintaining test automation can be challenging, especially when it comes to keeping selectors (classes, IDs, or XPath, etc.) up to date with the latest code changes. The Page Object pattern provides a solution by centralizing these selectors in separate <pagename>.java files, where you can manage them along with the associated methods.
