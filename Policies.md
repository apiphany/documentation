![APIphany Logo Blue](http://i.imgur.com/fG9dSvD.png)

#Topic: Policy Definitions

## Summary: ##

This document defines each policy, how to use it and where policies can be implemented of the three levels [Operations, API and product]

## Policy Editor ##

**Description:** 

Policy statements MUST be enclosed within either <inbound> or <outbound> elements.- <base /> elements represent policy-in-effect inherited from the outer scopes.
         - <inbound> element contains policies to be applied in the inbound direction (from caller to web service).
         - <outbound> element contains policies to be applied in the outbound direction (from web service to caller).
         - Policies are applied in the order they appear.

To ADD a policy, position cursor in the policy document to specify the insertion point and click on the associated button for a desired policy statement button.
    To REMOVE a policy, delete the corresponding policy statement from the policy document.
    To RE-ORDER a policy, select the corresponding policy statement and cut-and-paste it into a new location within the policy document.

**Policy Statement:** 

" < policies >, < inbound >, <base / >, < outbound >"

**Example:**


>> 	<policies>
>> 	<inbound>
>>         
>>         <base />
>>         
>>     </inbound>
>>     <outbound>
>>         
>>         <base />
>>         
>>     </outbound>
>>     </policies>

**Where it can be applied:** In all area three levels Operation, API, and Product

**When it should be applied:** It should always be applied its the default base policy

**Why it should be applied, why not:** Base policy definition, always applies

><table>
<thead>
<tr>
  <th>Statement</th>
  <th>Description</th>
</tr>
</thead>
<tbody>
<tr>
  <td>policies</td>
  <td>Policy statements MUST be enclosed within either <inbound> or <outbound> elements</td>
</tr>
<tr>
  <td>inbound</td>
  <td>element contains policies to be applied in the inbound direction (from caller to web service)</td>
</tr>
><tr>
  <td>outbound</td>
  <td>element contains policies to be applied in the outbound direction (from web service to caller)</td>
</tr>
><tr>
  <td>base</td>
  <td>elements represent policy-in-effect inherited from the outer scopes</td>
</tr>
</tbody>
</table>

## Policy: Store to Cache ##

**Description:**

**Policy Statement:** 

*<cache-store duration="seconds" caching-mode="cache-on | do-not-cache" />*

**Example:**

>   	<inbound>
>   	<base />
>		</inbound>>	
> 	<outbound>
> 		<base />
> 		<cache-store duration="3600" caching-mode="cache-on" />
> 	</outbound>

**Where it can be applied:**

**When it should be applied:**

**Why it should be applied, why not:**

<table>
<thead>
<tr>
  <th>Statement</th>
  <th>Description</th>
</tr>
</thead>
<tbody>
<tr>
  <td>seconds</td>
  <td>Duration (in seconds, default=3600) for the cached entry</td>
</tr>
<tr>
  <td>cache-on | do-not-cache</td>
  <td>enable caching or disables caching</td>
</tr>
</tbody>
</table>

## Policy: Get from Cache ##

**Description:**

**Policy Statement:** 

<cache-lookup vary-by-developer="true | false" vary-by-developer-groups="true | false" downstream-caching-type="none| private | public">
<vary-by-header>Accept</vary-by-header>
<vary-by-header>Accept-Charset</vary-by-header>
<vary-by-header>header name</vary-by-header>
<vary-by-query-parameter>parameter name</vary-by-query-parameter>
</cache-lookup>

**Example:**

> 	<inbound>
> 		<base />
> 		<cache-lookup vary-by-developer="false" vary-by-developer-groups="false" downstream-caching-type="none">
> 			<vary-by-header>Accept</vary-by-header>
> 			<vary-by-header>Accept-Charset</vary-by-header>
> 		</cache-lookup>
> 	</inbound>
> 	<outbound>
> 		<base /> 		
> 	</outbound>


**Where it can be applied:**

**When it should be applied:**

**Why it should be applied, why not:**

><table>
<thead>
<tr>
  <th>Statement</th>
  <th>Description</th>
</tr>
</thead>
<tbody>
<tr>
  <td>
vary-by-developer="true | false"

vary-by-developer-groups="true | false"

downstream-caching-type="none | private | public"
></td>
  <td>Content Cell</td>
</tr>
<tr>
  <td>Accept</td>
  <td>Content Cell</td>
</tr>
><tr>
  <td>Accept-Charset</td>
  <td>Content Cell</td>
</tr>
><tr>
  <td>header name</td>
  <td>Content Cell</td>
</tr>
><tr>
  <td>parameter name</td>
  <td>Content Cell</td>
</tr>
</tbody>
</table>

## Policy: Authenticate with Basic ##

**Description:**

**Policy Statement:**

*<authentication-basic username="username" password="password" />*

**Example:**

> 	<inbound>
> 		<base />
> 		<authentication-basic username="apiphany" password="vb2345ut!8P" />
> 	</inbound>
> 	<outbound>
> 		<base />
> 	</outbound>


**Where it can be applied:**

**When it should be applied:**

**Why it should be applied, why not:**

><table>
<thead>
<tr>
  <th>Statement</th>
  <th>Description</th>
</tr>
</thead>
<tbody>
<tr>
  <td>username="username" password="password"</td>
  <td>Content Cell</td>
</tr>
</tbody>
</table>

## Policy: Set query string parameters ##

**Description:**

**Policy Statement:**

*<set-query-parameters>
 <parameter name="param name" exists-action="override | skip | append">
 <value>value</value>  </parameter> </set-query-parameters>*

**Example:**


> 	<set-query-parameters>
			<parameter name="api_key" exists-action="skip">
				<value>vwva3789ca6gs23kcvv2c77v</value>
				<!-- for multiple parameters with the same name add additional value elements -->
			</parameter>
		</set-query-parameters>


**Where it can be applied:**

**When it should be applied:**

**Why it should be applied, why not:**

><table>
<thead>
<tr>
  <th>Statement</th>
  <th>Description</th>
</tr>
</thead>
<tbody>
<tr>
  <td>Parameter Name="name"</td>
  <td>Content Cell</td>
</tr>
><tr>
  <td>exists-action="override | skip | append"</td>
  <td>Content Cell</td>
</tr>
><tr>
  <td>Value="value"</td>
  <td>Content Cell</td>
</tr>
</tbody>
</table>
