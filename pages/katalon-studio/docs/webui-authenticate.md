---
title: "[WebUI] Authenticate" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-authenticate.html 
redirect_from: "/display/KD/%5BWebUI%5D+Authenticate" 
description: 
---
Description
-----------

Navigate to a page that requires authentication. System will enter username and password.

Parameters
----------

<table><thead><tr><th>Param</th><th>Param Type</th><th>Mandatory</th><th>Description</th></tr></thead><tbody><tr><td><span>url</span></td><td>String</td><td>Required</td><td><p><span>URL</span><span>&nbsp;of the page to navigate.</span></p></td></tr><tr><td><span>userName</span></td><td>String</td><td>Required</td><td><span>Username to authenticate.</span></td></tr><tr><td><span>password</span></td><td>String</td><td>Required</td><td><span>Password to authenticate.</span></td></tr><tr><td>timeout</td><td>int</td><td>Required</td><td>Time to wait since navigating to the page until entering&nbsp;username.</td></tr><tr><td><span>flowControl</span></td><td>FailureHandling</td><td>Optional</td><td>Specify <a>failure handling</a> schema to determine whether the execution should be allowed to continue or stop.</td></tr></tbody></table>

Example
-------

You want to verify if 'Make Appointment' button has attribute id with value: 'btnMakeAppointment' 

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import internal.GlobalVariable as GlobalVariable
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS

'Open browser and navigate to demo AUT site.'
WebUI.openBrowser('')

'Input username and password on authentication dialog.'
WebUI.authenticate('http://the-internet.herokuapp.com/basic_auth', 'admin', 'admin', 12)

'Close browser'
WebUI.closeBrowser()
```