# SAMSUNG REVERSE ENGINEERING
 Detailed Analysis of the Samsung Website 
Objective 
The primary focus was to reverse engineer the autocomplete search functionality on 
the Samsung e-commerce site. 
 Process: 
1. Monitoring Traffic: Using Postman and Burp Suite to capture network traffic 
during the search process. 
2. Identifying API Endpoints: The autocomplete API endpoint was identified: 

 
 
 POST https://sribsrch.ecom.samsung.com/estoresearch
api/v1/scom/in/metrics/autocomplete 


Captured Request Details: 
Headers: 
• Host: sribsrch.ecom.samsung.com 
• Content-Type: application/json 
Request Payload: 
{ 
  "metricsParam": "ea2575b2-c8e9-4f8a-8f16-fe5ca9b5871f", 
  "q": "smarttv", 
  "n": "20", 
  "src": "store" 
} 
Response Payload: 
{ 
  "code": "202 ACCEPTED", 
  "message": "Metrics collected."
 }
 
 
Observations: 
• The request sent metrics data along with the search query, indicating that the 
website collects and processes user search behaviour. 
• The response confirms successful collection of metrics, potentially for analytics 
or personalization purposes.

 
