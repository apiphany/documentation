![APIphany Logo Blue](http://i.imgur.com/fG9dSvD.png)

#Technical Notes: How to add an API on the developer portal

##Summary:

This document is a step by step "*How To*" guide to prepare a user to install and configure an API unto the tenant dashboard.

The following instructions uses the New York Times Article Search API as the guide and exhibit. This guide will show you how easy our platform is to configure and deploy. Please reach out to our sales team or on boarding person for technical assistance.


Version 1.0 - April 1, 2013 Presented by: Carlos Davila

© Apiphany, LLC - 3246 Prospect St. NW Washington, D.C 20007 Phone 202-295-3015 • Fax 202-295-3001


#API
###1. Adding and API

a. Locate your API base URI (ex. http://api.nytimes.com/svc/search/v1/article "article search")

b. Once you have located your API base URI, proceed to adding an API

c. Select **APIs** under **Apiphany**

D. ![](http://i.imgur.com/G5XOgjN.png)

e.	Click on ***add API***, a new screen will pop up allowing you to enter the following information

f.	   **Web API title**

g.	   **Web Serice URL**

h.	   **Web API URL suffix**

I.	![](http://i.imgur.com/p6GG8v1.png)


j.	In the **web API title** text box, you can add any *descriptive* API title you like to define your API (ex. **The Article Search API**).

k.	Each API entry requires being unique.
 
l.	The only field that can be repetitive is the ***web services URL***

m.	**Web API title** requires to be unique, defines your API

n.	**Web API URL suffix** requires to be unique this is the public facing side of your API

o.	If a *non-unique* entry is made an **error message** will prompt you to which field has caused the invalid entry

p.![](http://i.imgur.com/LPztR0h.png)

q.	Once you have successfully made all your entries your API will be added as the first entry or as an additional API

r.![](http://i.imgur.com/ZMdKCJn.png)

s.	Select your API to continue the configuration process; click on the **API name** or on the **configure** link. Either or will take you to the summary window

t.![](http://i.imgur.com/xLwMBNm.png)

u.	The **summary** window shows your calls and bandwidth usage. Your API and link

v.	Click on **Settings** now you can verify the settings you just completed inputting. You can make any changes while in the screen.

![](http://i.imgur.com/1hte6gj.png)

#OPERATIONS:
###1. Signature

a.	Click on **Operations** to add your http method, URI and developers documentation

b. ![](http://i.imgur.com/0HdV690.png)

###2.	When you click *add operation*, the following screen appears, *New Operation*.

a. ![](http://i.imgur.com/35crNLA.png)


###3.	Select *signature* then *HTTP method* a drop down appears which allows you to select from multiple request such as (GET, POST and Delete)

a. ![](http://i.imgur.com/dJIigT3.png)


###4.	Select “GET” enter your “URI Query” in the URI template box, an example is provided (*ex. /article?query={query}&api-key={apikey}*)

a. ![](http://i.imgur.com/v3RjqKR.png)

b.	You can use the **Rewrite URI template*** to rewrite the query method, see example below. **This is an optional field**.

c. ![](http://i.imgur.com/YOzk8kz.png)


###5.	Content in Display name will be entered automatically based on the URI template. The Display name field can be renamed. See below.

a. ![](http://i.imgur.com/OpbGcJR.png)

###6.  The content in Description could be plain text or HTML 5. You will need to structure your HTML 5 so you will have the look and feel you desire.

a. ![](http://i.imgur.com/jc4geEd.png)

###7.  OPERATIONS: Caching Needs defining?????

a. ![](http://i.imgur.com/MQcy8EX.png)

b.	Caching is an optional to enable caching select the enable box you can declare what parameters are going to be cache in the **Vary by query string parameters** text box

c.	Vary by headers ?

d.	Duration ?

e.	Click on **Save** when done

###8.	OPERATIONS: Parameters

a.	Click on **Parameters** the following window opens

b.	![](http://i.imgur.com/gEf6iCc.png)

c.	To add a new query parameter, click on **add query parameter** a new window opens with the options to add the following

	i.		Name: parameter name
	ii.		Description: description of the parameter
	iii.	Type: string, text, date etc… this is a drop down option
	iv.		Values: enter the value that correspond to the specified parameter
	v.		Required: select to make the optional parameter mandatory

d.	**Path Parameters** are entered automatically from the URI string in the URI template

e.	**Query Parameters** are your optional parameter

f.	![](http://i.imgur.com/hSn4Dmj.png)

###9.	OPERATIONS: Code 200

a.	Click on **Code 200**, in the **Description** box you can enter text that corresponds to your code 200 response

b.	![](http://i.imgur.com/V5ENeos.png)

c.	The *code 200* hundred section has two parts **Description** and **add representation.** 

d.	Click on **add representation**, a content box appears, type the letter **(a)** and a list in alphabetical order will appear, you now can make a selection.

e. ![](http://i.imgur.com/oSRyudC.png)

f.	We’ve chosen **application/json** and entered how the representation would look.

g.	![](http://i.imgur.com/DTKQoY0.png)

h.	Click **Save**; your next step is to publish your API product. Do this by selecting **products**

#PRODUCTS:

a.	Click on **products** then select **add product**, a pop up window will appear

b.	![](http://i.imgur.com/zJwB8bl.png)

c.	Enter a **name** for the product and a **description**, click on **save** after you’re done.

d.	A new entry will be entered in the products section, with the name of the product you gave and a description. Default Roles will automatically be part of the **product** such as the **administrator** and **developer.**

e.	![](http://i.imgur.com/BFi8wnk.png)

f.	Click on the **product name** or on **configure** to proceed

###1.	PRODUCTS: Summary

a.	**Products** contains three categories **[Summary, Description and visibility]**

b.	**Summary** allows the action to *publish* or *unpublished* your API. Select *publish* so your API will be visible on your page.

i. ![](http://i.imgur.com/H1Pyvxi.png)

c.	Add the API you created to make a product. Do this by selecting **Add API to the product**. A pop up window will appear and you can select one or more API to your product.

i.	![](http://i.imgur.com/TDBooIV.png)

ii.	![](http://i.imgur.com/s8jRo2h.png)

iii.	***If you click on the API you will be taken back to the API tab in dashboard***

###2.	PRODUCTS: Description

a.	Now select **Description** you will add a **Name** for the product and define the environment. Be aware this section can be written in plain text or HTML 5 code. 

b.	![](http://i.imgur.com/nyMRdPW.png)

###3.	PRODUCTS: visibility

a.	Select **Visibility** this section gives you the ability to add a user group to your API product. Self-explanatory

b.	![](http://i.imgur.com/RdZcuBK.png)

c.	By selecting **manage roles** you will have the option of creating a role for a user group and give it permissions in the portal. ***This feature set is not currently available***. 

d.	Link to the [DEMO PRODUCT](https://carlos-demo.apiphany.com/docs/services/295 "DEMO")























