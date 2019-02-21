# Building an Andriod Application

After you have a basic understanding of Andriod Studio and have it installed and running on your computer, you can use it to build the UI elements, connect it to the backend code, and test the app on the emulator. The Andriod app takes some input text from the user and outputs the same text onto the screen. The steps for building this Andriod app are as follows:

> ## Contents

**[Building UI in XML Files](#UI)**<br>
**[Connecting UI to Backend Code with Variables and Methods](#Connect)**<br>
**[Implementing Backend Functionality](#Implement)**<br>
**[Testing on Emulator](#Testing)**<br>

<a name="UI"></a>
> ## Building UI in XML Files

You can build the UI using XML text:

1. Open the *activity_main.xml* file
2. The *TextView* element is setup by default 
3. Copy the *EditText*, *Button*, and *TextView* elements from the *activity_main.xml* file
4. Copy the string resources from the *strings* file

<a name="Connect"></a>
> ## Connecting UI to Backend Code with Variables and Methods

An API transaction workflow is as follows:

1. A request is made for a task to be performed
2. A program is run to complete that request
3. The program sends back a response with the results
 
 If the API request and response are sent over the internet, then the API is called a “Web Service API.”
 
 <a name="Implement"></a>
> ## Implementing Backend Functionality

An API transaction workflow is as follows:

1. A request is made for a task to be performed
2. A program is run to complete that request
3. The program sends back a response with the results
 
 If the API request and response are sent over the internet, then the API is called a “Web Service API.”

<a name="Testing"></a>
> ## Testing on Emulator

SOAP is an acronym that stands for Simple Object Access Protocol. It is used to complete a web service using HTTP.

A web service using SOAP has a WSDL (Web Services Description Language). This is an XML file that describes the web service and what you can do with it. 

In SOAP, the HTTP request is created as follows:

1. Start Line: {POST} {WSDL URL} {HTTP version}
   - Method is not used and POST works as a placeholder. 
   - WSDL URL is the WSDL location.

2. Header Line: Content-Type: text/xml
   - SOAP only supports XML as the data format to be used in the body.

3. Body
   - The body constitutes an XML envelope formed using the specific WSDL.

`Example of using a SOAP-based web service`

Web service: HolidayService2 
This web service provides the holidays for a specified country. It is described by this WSDL.

- Method:  POST 
- URL: http://www.holidaywebservice.com/HolidayService_v2/HolidayService2.asmx?WSDL 
- Headers: content-type: test/XML
- Body: 
```
<?xml version="1.0"?>
<soap:Envelope
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:hws="http://www.holidaywebservice.com/HolidayService_v2/"> //WSDL will tell you this namespace.

<soap:Body>
  <hws: GetHolidaysAvailable>
	<hws: countryCode>UnitedStates</hws: countryCode>
  </hws: GetHolidaysAvailable>
</soap:Body>

</soap:Envelope>
```










