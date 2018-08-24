---
title: "[WebUI] Set Masked Text" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/webui-set-masked-text.html 
redirect_from: "/display/KD/%5BWebUI%5D+Set+Masked+Text" 
description: 
---
Description  
-------------

Set the value of an input field, as though you type it in. It also clears the previous value of the input field. The text value will be masked.

Parameters  

<table><thead><tr><th>Param</th><th>Param Type</th><th>Mandatory</th><th>Description</th></tr></thead><tbody><tr><td><span>to&nbsp;</span></td><td><span>TestObject</span></td><td><span>Required</span></td><td><span>Represent a web element.</span></td></tr><tr><td><span>text</span></td><td><span>String</span></td><td><span>Required</span></td><td><span>The text to type in.</span></td></tr><tr><td><span>flowControl</span></td><td><span>FailureHandling</span></td><td><span>Optional</span></td><td><span>Spec</span>ify <a>failure handling</a> schema to determine whether the execution should be allowed to continue or stop.</td></tr></tbody></table>

Example  
---------

You want to set the masked text to **Password** fieldof a login form.

```groovy
import static com.kms.katalon.core.checkpoint.CheckpointFactory.findCheckpoint
import static com.kms.katalon.core.testcase.TestCaseFactory.findTestCase
import static com.kms.katalon.core.testdata.TestDataFactory.findTestData
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.checkpoint.Checkpoint as Checkpoint
import com.kms.katalon.core.checkpoint.CheckpointFactory as CheckpointFactory
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as MobileBuiltInKeywords
import com.kms.katalon.core.mobile.keyword.MobileBuiltInKeywords as Mobile
import com.kms.katalon.core.model.FailureHandling as FailureHandling
import com.kms.katalon.core.testcase.TestCase as TestCase
import com.kms.katalon.core.testcase.TestCaseFactory as TestCaseFactory
import com.kms.katalon.core.testdata.TestData as TestData
import com.kms.katalon.core.testdata.TestDataFactory as TestDataFactory
import com.kms.katalon.core.testobject.ObjectRepository as ObjectRepository
import com.kms.katalon.core.testobject.TestObject as TestObject
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WSBuiltInKeywords
import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUiBuiltInKeywords
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI
import internal.GlobalVariable as GlobalVariable

'Open browser and navigate to AUT'
WebUI.openBrowser(GlobalVariable.G_SiteURL)

'Input username'
WebUI.setText(findTestObject('Page_Login/txt_UserName'), Username)

'Input password'
WebUI.setMaskedText(findTestObject('Page_Login/txt_Password'), Password)

'Click on \'Login\' button'
WebUI.click(findTestObject('Page_Login/btn_Login'))

'Close browser'
WebUI.closeBrowser()
```