![](https://github.com/apiphany/documentation/blob/master/images/logo.png?raw=true)
#Tech Note 1: How to publish an API

## Summary
This is a step-by-step guide explaining how to register and describe an API, add it to newly created product, and publish it to the Web. Please provide feedback or request assistance by sending an email to [support@apiphany.com](mailto:support@apiphany.com).

## Adding an API
1. Sign in into the administrative console on the developer portal.
	- Navigate to your developer portal.
	- Click **Sign In** button or link in the top menu. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_01_signin.png?raw=true)
	- Depending on how you created your account, click on one of the 3rd party identities or enter your username (not your email address) and password and click **Sign In** button.
	- Click on the **Dashboard** button or link in the top menu. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_02_dashboard.png?raw=true)

2. Select the **APIs** menu option on the left and click on the **add API** button. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_03_addapi.png?raw=true)

3. The **Add new API** popup window will be displayed. 

4. Provide values for the three fields (all required) on the **Add new API** popup window.
	- **Web API title** provides a unique and descriptive name for the API. It is displayed in many places on the developer and administrative portals.
	- **Web service URL** references HTTP service implementing the API. Apiphany platform will forward API requests to this address.
	- **Web API URL suffix** is appended to the base URL. Base URL is common for all APIs hosted on the Apiphany platform by the API publisher. It can be viewed under the last input box. Apiphany platform distinguishes APIs by their suffix and therefore it must be unique for every API for a given publisher. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_04_new_api.png?raw=true)

5. Once you have successfully made all of your entries click **Save**.
 
## Changing API settings

1. The **settings** section allows you to verify and edit the information you just entered. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_06_settings.png?raw=true)

2. You can optionally configure HTTP Basic Authentication for the web service implementing the API by checking **Enable Authentication** checkbox and entering credentials. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_07_authentication.png?raw=true)
 
## Configuring API operations

### <a id="url_template"></a> Operation signature
1. To enter API operations select **operations** link on the API page. Note that you have to click **Save** button to persist the changes. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_08_operations.png?raw=true)

2. To add a new operation click **add operation** button. **New operation** window will be displayed. **Signature** tab will be selected by default. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_09_operation_signature.png?raw=true)

3. Specify HTTP method by placing cursor in the **HTTP method** input and selecting one of HTTP methods from the drop down list. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_10_http_method.png?raw=true)
 
4. Define **URI template** by typing in a URL fragment consisting of one or more URL path segments and zero or more query string parameters. URI template, appended to the base URL of the API, identifies a single HTTP operation and may contain one or more named variable parts that are identified by curly braces. These variable parts are called template parameters and are dynamically assigned values extracted from the request's URL when the request is being processed by the Apiphany platform.![](https://github.com/apiphany/documentation/blob/master/images/tn01_11_uri_template.png?raw=true)

5. Optionally, specify **Rewrite URI template**. Template parameters from the URI template should be used in the rewrite template. URL of the incoming operation request will be converted into a URL that would be forwarded to the web service that implements the API according to the URL - rewrite URL mapping. The following example shows how content type encoded as path segment in the web service can be provided as a query parameter in the API published via APiphany using the URI templates.
	
	URI template:`/orders?format={contentType}`
	
	Rewrite URI template:`/{contentType}/orders`
	
	Request URL `.../orders?format=xml` is mapped to `.../xml/orders`

5. Enter a descriptive name for the operation in the **Display name** text box.

6. Operation description can be specified as plain text or HTML in the **Description** text box.
 
### Operation caching
Response caching reduces latency perceived by the API consumers, lowers bandwidth consumption and decreases the load on the HTTP web service implementing the API. Note that comprehensive caching settings are available via the **Policy** page.
 
1. To easily and quickly enable caching for the operation, select the **Caching** tab and check the **Enable** checkbox. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_12_enable_cache.png?raw=true)

2. In the **Duration** text box, change the time period during which cached responses remain fresh and are served from cache. Default value is 3600 second or 1 hour.

3. Optionally, enter specific query string parameters and/or HTTP headers to be used in computing cache key values in the **Vary by string parameters** and **Vary by headers** text boxes respectively. When none specified, full request URL and the following HTTP header values are used in cache key generattion: `Accept` and `Accept-Charset`. 

### Request parameters
Operation parameters are managed on the **Parameters** tab. Parameters specified in the URL Template on the [**Signature tab**](#url_template) are added automatically and can be changed only by editing the URL template. Additional parameters can be entered manually.

To add a new query parameter, click **add query parameter** and enter the following information:

- **Name** - parameter name.

- **Description** - a brief description of the parameter (optional).

- **Type** - parameter type, selected in the drop down.

- **Values** - values that can be assigned to this parameter. One of the values can be marked as default (optional).

- **Required** - make the parameter mandatory by checking the checkbox. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_13_request_parameters.png?raw=true)

### Request body
If the operation allows (e.g. PUT, POST) and requires a body you may provide an example of it in all of the supported representation formats (e.g. json, XML). 

1. Switch to the **Body** tab.

2. Click **add representation**, start typing desired content type name (e.g. `application/json`) and then select it in the drop down.

3. Paste request body example in the selected format into the text box. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_14_request_body.PNG?raw=true)

4. Add description (optional).

### Responses
It is a good practice to provide examples of responses for all status codes that the operation may produce. Each status code may have more than one response body example, one for each of the supported content types. For instance, to add an example of `200 OK` response perform the following steps:

1. Click on **add response**, start typing desired status code (e.g. `200 OK` in the text box, then select it in the drop down.

2. **Code 200** tab is created and selected.

2. Click **add representation** start typing desired content type name (e.g. `application/json`) and then select it in the drop down. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_15_response_body_content_type.png?raw=true)

3. Paste request body example in the selected format into the text box. ![](https://github.com/apiphany/documentation/blob/master/images/tn01_16_response_body.png?raw=true) 

4. Add description (optional).

Do not forget to click **Save** button to persist the changes.
