![APIphany Logo Blue](http://i.imgur.com/fG9dSvD.png)

#Technical Notes: How to add an API on the developer portal

###Summary:

Step by Step "*How To*" guide to prepare a user to install and configure an API unto the tenant dashboard.

The following instructions uses Playground as the guide and exhibit. This guide will show you how easy our platform is to configure and deploy. Please reach out to our sales team or on boarding person for technical assistance.


#Adding an API

	- Select APIs under Apiphany

![](http://i.imgur.com/TrCjo4W.png)

	-	Click on + add API and a ADD NEW API screen will pop up

![](http://i.imgur.com/p6GG8v1.png)

	- 	API entries must be unique.
	-	The only field that does not need to be UNIQUE is the **web services URL**

	If a *non-unique* entry is made an **error message** will appear indicating which field has caused the invalid entry

![](http://i.imgur.com/uoeubLm.png)

	- Once you have successfully made all your entries, click on "SAVE" you will be taken to the settings page of the API you just created

##APIs: SETTINGS:
![](http://i.imgur.com/xhOuRlY.png)

	- **Settings** allows you to verify and edit the information you just inputted
	- **Enable Authentication** allows Authentication with the web service

![](http://i.imgur.com/jA9tah1.png)


##APIs: OPERATIONS:

	- Select **Operations**

![](http://i.imgur.com/zZp6aS4.png)

	- Select (+ ADD OPERATION), the following screen appears: (New Operation)

![](http://i.imgur.com/35crNLA.png)

	- Select (signature) then (HTTP method) 
	- Drop down appears select one option from multiple choices

![](http://i.imgur.com/dJIigT3.png)

	- Select (HTTP Method), enter your (URI Query) in the (URI template)box

![](http://i.imgur.com/SNftfJc.png)

	- In (Display name) the contents can be renamed.
	- In the (Description) box enter text or html 5 code 
	- Content in (Description) will define the API and its properties

###APIs: OPERATIONS:  Caching

	- Caching is optional, to enable caching select the (enable) button
	- Select (Save) when done

![](http://i.imgur.com/4EcwqaF.png)

###APIs: OPERATIONS:  Request: Parameters

	- Select (Parameters)

![](http://i.imgur.com/cFnXwjE.png)

	*Path Parameters are entered automatically from the information in URI template*
	*Query Parameters** are your optional parameter*
	To add a new query parameter, select (add query parameter) 
		- Name {parameter name}
		- Description {description of the parameter/optional}
		- Type {this is a drop down option}
		- Values: {optional}
		- Required {select to make mandatory}

![](http://i.imgur.com/WuTdHIL.png)

###APIs: OPERATIONS:  Request: Body

	- Select body to enter put request. This option only appears for Put & Delete
	- Optional to enter content

![](http://i.imgur.com/CVXmaUE.png)

###APIs: OPERATIONS: Responses: Code 200

	
	- Select (Code 200), information in the (Description) is optional

![](http://i.imgur.com/V5ENeos.png)

	- Select (add representation) 
	- a content box appears, type the letter (a) 
	- a list in alphabetical order will appear, you can now make a selection.

![](http://i.imgur.com/oSRyudC.png)

	- Example (application/json) entered to show how the representation would look.

![](http://i.imgur.com/rvqKtJp.png)


#PRODUCTS:

	- Click on **products** then select **add product**, a pop up window will appear
	- Enter information as describe

![](http://i.imgur.com/zJwB8bl.png)

	- click save
	- A new product will be entered
	- Default Roles will automatically be part of the **product** 
	- such as the **administrator** and **developer.**

![](http://i.imgur.com/ivg3sbw.png)

	- Select the **product name** or **configure** to proceed

###PRODUCTS: Summary

	- Products contains three categories [Summary, Description and visibility]
	- Within Summary you can set you product to (publish) or (unpublished)
	- Before publishing your product you need to add an API

![](http://i.imgur.com/0YZ6XeM.png)

	- Select (Add API to the product)
	- A window appears select API to use then click on save.

![](http://i.imgur.com/iCgcZC3.png)

###PRODUCTS: Description

	- Select (Description) you can define the environment here
	- This section can be written in plain text or HTML 5 code. 

![](http://i.imgur.com/EsQ1vbh.png)

###PRODUCTS: visibility

	- Select **Visibility** to enable roles

![](http://i.imgur.com/RdZcuBK.png)

	- By selecting **manage roles** you will have the option of creating a role
	- for a user group and give it permissions in the portal
	- ***This feature set is not currently available***























