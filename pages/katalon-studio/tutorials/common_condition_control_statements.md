---
title: "Common Condition and Control statements with Katalon Studio"
sidebar: katalon_studio_tutorials_sidebar
permalink: katalon-studio/tutorials/common_condition_control_statements.html
description: "Katalon Studio provides the ability to dictate the flow of execution by supporting control statements which are common concepts in programming language."
---
Katalon Studio provides a capability to dictate the logical flow of execution by supporting **control statements** such as _if/else_, _for/while_ and _try/catch_ which are very common concepts in programming languages. This tutorial will explain in details how to use **control statements** in Katalon Studio along with examples for each case.

The following control statements are supported in Katalon Studio:

*   **[Decision-making statements](https://docs.katalon.com/display/KD/Control+Statements#ControlStatements-Decision-makingstatements)**
*   **[Looping statements](https://docs.katalon.com/display/KD/Control+Statements#ControlStatements-Loopingstatements)**
*   **[Branching statements](https://docs.katalon.com/display/KD/Control+Statements#ControlStatements-Branchingstatements)**
*   **[Exception handling block](https://docs.katalon.com/display/KD/Control+Statements#ControlStatements-Exceptionhandlingblock)**

Note: once a test step is added as any of the control statements, it will not be allowed to change into another keyword.

Decision-making statements
--------------------------

### In the Manual view

Open a test case in the **Manual** view, then navigate to **Decision-making** Statements from command toolbar.

![navigate to Decision-making Statements from command toolbar](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2015%3A16%3A40.png)

Refer to the following table for the usage of each statement:

<table><thead><tr><th>Statement</th><th>Description</th></tr></thead><tbody><tr><td>If</td><td>This statement requires a boolean condition as input value. Katalon Studio will execute all the steps within once the condition&nbsp;is triggered.</td></tr><tr><td>&nbsp;Else If</td><td>Using Else If after If, you can create a combination of conditions where the steps within the <em>first </em>satisfied condition will be executed.</td></tr><tr><td>&nbsp;Else</td><td>&nbsp;This statement serves as the conclusion of the If – Else If – Else structure. The steps within this statement will be executed if all the conditions above it are not triggered.</td></tr></tbody></table>

![you can create a combination of conditions](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2014%3A23%3A17.png)

<table><thead><tr><th>Statement</th><th>Description</th></tr></thead><tbody><tr><td>Switch</td><td>This statement requires an expression, which is often referred to as the control expression (or control variable), as input value.</td></tr><tr><td>Case</td><td>The Cases indicate the assumed value for the control expression, with the corresponding steps to be executed when a match occurs.<br>Each Case will have a Break by default which should be positioned at the end of the Case block to mark the end of it.</td></tr><tr><td>Default</td><td>This statement is included automatically within every Switch statement. In situations where there is no case matched, all the steps under default will be executed.</td></tr></tbody></table>

![Common Condition and Control statements with Katalon Studio](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2014%3A47%3A59.png)

### In the Script view

The Script view of test cases allows you to programmatically define and handle If-ElseIf-Else or Switch-Case structure easily using either Groovy or Java language. Refer to [conditional structure](http://groovy-lang.org/semantics.html#_conditional_structures) in Groovy for more details.

For example:

<table><thead><tr><th>Decision-making statement</th><th>Screenshot</th></tr></thead><tbody><tr><td><strong>If – Else If – Else</strong></td><td><div><p>Here is an example on how to use <strong>if-else if-else </strong>in the Script View where the Click action will be carried out based on the condition</p><p><span><img></span></p></div></td></tr><tr><td><strong>Switch – Case</strong></td><td><div><p>Here is an example on how to use <strong>switch-case </strong>in the Script View where <i><span>varB</span></i>&nbsp;is calculated based on the passing value of&nbsp;<i><span>varA.</span></i></p></div><div><img></div></td></tr></tbody></table>

Looping statements
------------------

### In the Manual view

Open a test case in Manual view, then navigate to **Looping Statements** from the command toolbar.

![Katalon Studio looping statement](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2015%3A29%3A14.png)

Refer to the following table for the usage of each statement:

<table><thead><tr><th><div><strong>Statement</strong></div></th><th><div><strong>Description</strong></div></th></tr></thead><tbody><tr><td><strong>For</strong></td><td>This statement accepts a <em>range</em>,<em> list</em> or <em>array</em> as input value so that Katalon Studio knows how many times to execute all steps within the For structure.</td></tr></tbody></table>

![how many times to execute all steps within the For structure](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2015%3A49%3A5.png)

<table><thead><tr><th><div>Statement</div></th><th><div>Description</div></th></tr></thead><tbody><tr><td><strong>While</strong></td><td>This statement requires a boolean condition as input value so that Katalon Studio will keep executing all steps within until the condition fails.</td></tr></tbody></table>

![ Katalon Studio will keep executing all steps within until the condition fails](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2015%3A53%3A44.png)

### In the Script view

The Script View of test cases allows you to programmatically define and handle For or While structure easily using either Groovy or Java language. Refer to [looping structures](http://groovy-lang.org/semantics.html#_looping_structures) in Groovy for more details.

For example:

<table><thead><tr><th>Looping statement</th><th>Screenshot</th></tr></thead><tbody><tr><td><strong>For</strong></td><td><div><p>Here is an example on how to use <strong>For </strong>in the Script View where the <em>acceptAlert </em>keyword will be executed 10 times</p><p><span><img></span></p></div></td></tr><tr><td><strong>While</strong></td><td><div><p>Here is an example on how to use <strong>For </strong>in the Script View where the value of <strong>varA </strong>is <strong>true</strong></p><p><span><img></span></p></div></td></tr></tbody></table>

Branching statements
--------------------

### In the Manual view

Open a test case in the Manual view, then navigate to **Branching Statements** from the command toolbar.

![Katalon Studio Branching Statements](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2016%3A17%3A13.png)

Refer to the following table for the usage of each statement:

<table><thead><tr><th><div><strong>Statement</strong></div></th><th><div>Description</div></th></tr></thead><tbody><tr><td><strong>Break</strong></td><td>Katalon Studio exits the current code block and continues to the next code block/test step.</td></tr></tbody></table>

![the next code block/test step](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2016%3A36%3A37.png)

<table><thead><tr><th><div>Statement</div></th><th><div>Description</div></th></tr></thead><tbody><tr><td><strong>Continue</strong></td><td>Katalon Studio will skip the remainder of the current loop and continue with the next iteration of the loop.</td></tr></tbody></table>

![ the next iteration of the loop.](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2016%3A42%3A13.png)

<table><thead><tr><th><div><strong>Statement</strong></div></th><th><div><strong>Description</strong></div></th></tr></thead><tbody><tr><td><strong>Return</strong></td><td>Katalon exits from the current method/step, and the flow control is returned to where the method/step <span>is previously invoked</span>.</td></tr></tbody></table>

![the flow control is returned](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2016%3A47%3A44.png)

### In the Script view

The Script view of test cases allows you to programmatically define and handle Break, Continue & Return easily using either Groovy or Java language.

For example:

<table><thead><tr><th>Decision-making statement</th><th>Screenshot</th></tr></thead><tbody><tr><td><strong>Break</strong></td><td><div><p>Here is an example on how to use <strong>Break </strong>in the Scripts View in order to exit current code block and move to next code block.</p></div><div><img></div></td></tr><tr><td><strong>Continue</strong></td><td><div>Here is an example on how to use <strong>Continue </strong>in the Script View in order to skip the remainder of the current loop and continue with the next iteration of the loop.</div><div><img></div></td></tr><tr><td><strong>Return</strong></td><td><div><p>Here is an example on how to use <strong>Return </strong>in the Script View in order to exit from the current method, and the flow control is returned to where the method was invoked.</p></div><div><img></div></td></tr></tbody></table>

Exception handling block
------------------------

### In the Manual view

Open a test case in Manual view, then navigate to **Exception Handling Statements** from the command toolbar.

![Katalon Studio Exception Handling Statements](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-9%2017%3A0%3A13.png)

Refer to the following table for the usage of each statement:

<table><thead><tr><th>Statement</th><th>Description</th></tr></thead><tbody><tr><td><strong>Try</strong></td><td>This statement indicates that all steps within it will be monitored by exception handlers.</td></tr><tr><td><strong>Throw</strong></td><td>Before you can catch an exception, some code must throw it. Regardless of what throws the exception, it’s always involved with the Throw statement.</td></tr><tr><td><strong>Catch</strong></td><td>Katalon Studio executes all steps within <span>the Catch block when there is any issue occurring during execution of the Try block</span>.</td></tr><tr><td><strong>Finally</strong></td><td><span>This is the last part of the Try-Catch-Finally structure and all steps within this block will be executed regardless of what exceptions and whether they are handled in the Catch block.</span></td></tr></tbody></table>

![the usage of each statement](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-28%2011%3A51%3A55.png)

### In the Script view

The Script view of test cases allows you to programmatically define and handle exception easily using either Groovy or Java language. Refer to [this guide](http://groovy-lang.org/semantics.html#_try_catch_finally) for more details about exception handling in Groovy.

For example:

![Katalon Studio Script View](../../images/katalon-studio/tutorials/common_condition_control_statements/image2017-2-28%2013%3A20%3A32.png)