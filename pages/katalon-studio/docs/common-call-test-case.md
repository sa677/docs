---
title: "[Common] Call Test Case" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/common-call-test-case.html 
redirect_from: "/display/KD/%5BCommon%5D+Call+Test+Case" 
description: 
---
Description  
-------------

Call another test case and execute it separately.

Parameters  
------------

<table><thead><tr><th>Param</th><th>Param Type</th><th>Mandatory</th><th>Description</th></tr></thead><tbody><tr><td><span>arg0</span></td><td><span>TestCase</span></td><td><span>Required</span></td><td><span>Represent the called test case's path.</span></td></tr><tr><td><span>arg1</span></td><td><span>Map&lt;String,Object&gt;</span></td><td><span>Required</span></td><td><span>Represent the list of parameters will be used in the called test case.</span></td></tr><tr><td><span>flowControl</span></td><td><span>FailureHandling</span></td><td><span>Optional</span></td><td><span>Spec</span><span>ify </span><a>failure handling</a><span> schema to determine whether the execution should be allowed to continue or stop.</span></td></tr></tbody></table>

Returns
-------

<table><thead><tr><th>Param Type</th><th>Description</th></tr></thead><tbody><tr><td><span>Object</span></td><td><p><span>Value of called test case if any.</span></p></td></tr></tbody></table>

Example 
--------

You want to verify if the returned message after logging in successfully does not match the expected message.

*   Manual view    
    ![](../../images/katalon-studio/docs/common-call-test-case/image2017-3-3 17_49_2.png)
*   Script view 
    
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
    'Use WebUI keyword'
    WebUI.callTestCase(findTestCase('DDR_NavigateToPageThenVerifyPageTitle'), ['p_Protocol' : null, 'p_DomainName' : null, 'p_Path' : null
            , 'p_WindowTitle' : null])
    
    'Use Mobile keyword'
    Mobile.callTestCase(findTestCase('DDR_NavigateToPageThenVerifyPageTitle'), ['p_Protocol' : null, 'p_DomainName' : null, 'p_Path' : null
            , 'p_WindowTitle' : null])
    
    'Use WS keyword'
    WS.callTestCase(findTestCase('DDR_NavigateToPageThenVerifyPageTitle'), ['p_Protocol' : null, 'p_DomainName' : null, 'p_Path' : null
            , 'p_WindowTitle' : null])
    
    
    
    ```