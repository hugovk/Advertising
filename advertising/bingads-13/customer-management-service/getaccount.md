---
title: GetAccount Service Operation - Customer Management
ms.service: bing-ads
ms.subservice: customer-management-api
ms.topic: article
author: jonmeyers
ms.author: jonmeyers
description: Gets the details of an account.
dev_langs: 
- csharp
- java
- php
- python
---
# GetAccount Service Operation - Customer Management
Gets the details of an account.

## <a name="request"></a>Request Elements
The *GetAccountRequest* object defines the [body](#request-body) and [header](#request-header) elements of the service operation request. The elements must be in the same order as shown in the [Request SOAP](#request-soap). 

> [!NOTE]
> Unless otherwise noted below, all request elements are required.

### <a name="request-body"></a>Request Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="accountid"></a>AccountId|The identifier of the account to get.|**long**|
|<a name="returnadditionalfields"></a>ReturnAdditionalFields|The list of additional properties that you want included within each returned account. The additional field values enable you to get the latest features using the current version of Customer Management API, and in the next version the corresponding elements will be included by default.<br/><br/>This request element is optional.|[AccountAdditionalField](accountadditionalfield.md)|

### <a name="request-header"></a>Request Header Elements
[!INCLUDE[request-header](./includes/request-header.md)]

## <a name="response"></a>Response Elements
The *GetAccountResponse* object defines the [body](#response-body) and [header](#response-header) elements of the service operation response. The elements are returned in the same order as shown in the [Response SOAP](#response-soap).

### <a name="response-body"></a>Response Body Elements

|Element|Description|Data Type|
|-----------|---------------|-------------|
|<a name="account"></a>Account|An account object that contains information about the account, such as payment method, account type, and parent customer.|[AdvertiserAccount](advertiseraccount.md)|

### <a name="response-header"></a>Response Header Elements
[!INCLUDE[response-header](./includes/response-header.md)]

## <a name="request-soap"></a>Request SOAP
This template was generated by a tool to show the [order](../guides/services-protocol.md#element-order) of the [body](#request-body) and [header](#request-header) elements for the SOAP request. For supported types that you can use with this service operation, see the [Request Body Elements](#request-body) reference above.

```xml
<s:Envelope xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v13">
    <Action mustUnderstand="1">GetAccount</Action>
    <AuthenticationToken i:nil="false">ValueHere</AuthenticationToken>
    <DeveloperToken i:nil="false">ValueHere</DeveloperToken>
  </s:Header>
  <s:Body>
    <GetAccountRequest xmlns="https://bingads.microsoft.com/Customer/v13">
      <AccountId>ValueHere</AccountId>
      <ReturnAdditionalFields i:nil="false">ValueHere</ReturnAdditionalFields>
    </GetAccountRequest>
  </s:Body>
</s:Envelope>
```

## <a name="response-soap"></a>Response SOAP
This template was generated by a tool to show the order of the [body](#response-body) and [header](#response-header) elements for the SOAP response.

```xml
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header xmlns="https://bingads.microsoft.com/Customer/v13">
    <TrackingId d3p1:nil="false" xmlns:d3p1="http://www.w3.org/2001/XMLSchema-instance">ValueHere</TrackingId>
  </s:Header>
  <s:Body>
    <GetAccountResponse xmlns="https://bingads.microsoft.com/Customer/v13">
      <Account xmlns:e216="https://bingads.microsoft.com/Customer/v13/Entities" d4p1:nil="false" xmlns:d4p1="http://www.w3.org/2001/XMLSchema-instance">
        <e216:BillToCustomerId d4p1:nil="false">ValueHere</e216:BillToCustomerId>
        <e216:CurrencyCode d4p1:nil="false">ValueHere</e216:CurrencyCode>
        <e216:AccountFinancialStatus d4p1:nil="false">ValueHere</e216:AccountFinancialStatus>
        <e216:Id d4p1:nil="false">ValueHere</e216:Id>
        <e216:Language d4p1:nil="false">ValueHere</e216:Language>
        <e216:LastModifiedByUserId d4p1:nil="false">ValueHere</e216:LastModifiedByUserId>
        <e216:LastModifiedTime d4p1:nil="false">ValueHere</e216:LastModifiedTime>
        <e216:Name d4p1:nil="false">ValueHere</e216:Name>
        <e216:Number d4p1:nil="false">ValueHere</e216:Number>
        <e216:ParentCustomerId>ValueHere</e216:ParentCustomerId>
        <e216:PaymentMethodId d4p1:nil="false">ValueHere</e216:PaymentMethodId>
        <e216:PaymentMethodType d4p1:nil="false">ValueHere</e216:PaymentMethodType>
        <e216:PrimaryUserId d4p1:nil="false">ValueHere</e216:PrimaryUserId>
        <e216:AccountLifeCycleStatus d4p1:nil="false">ValueHere</e216:AccountLifeCycleStatus>
        <e216:TimeStamp d4p1:nil="false">ValueHere</e216:TimeStamp>
        <e216:TimeZone d4p1:nil="false">ValueHere</e216:TimeZone>
        <e216:PauseReason d4p1:nil="false">ValueHere</e216:PauseReason>
        <e216:ForwardCompatibilityMap xmlns:e217="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
          <e217:KeyValuePairOfstringstring>
            <e217:key d4p1:nil="false">ValueHere</e217:key>
            <e217:value d4p1:nil="false">ValueHere</e217:value>
          </e217:KeyValuePairOfstringstring>
        </e216:ForwardCompatibilityMap>
        <e216:LinkedAgencies d4p1:nil="false">
          <e216:CustomerInfo>
            <e216:Id d4p1:nil="false">ValueHere</e216:Id>
            <e216:Name d4p1:nil="false">ValueHere</e216:Name>
          </e216:CustomerInfo>
        </e216:LinkedAgencies>
        <e216:SalesHouseCustomerId d4p1:nil="false">ValueHere</e216:SalesHouseCustomerId>
        <e216:TaxInformation xmlns:e218="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
          <e218:KeyValuePairOfstringstring>
            <e218:key d4p1:nil="false">ValueHere</e218:key>
            <e218:value d4p1:nil="false">ValueHere</e218:value>
          </e218:KeyValuePairOfstringstring>
        </e216:TaxInformation>
        <e216:BackUpPaymentInstrumentId d4p1:nil="false">ValueHere</e216:BackUpPaymentInstrumentId>
        <e216:BillingThresholdAmount d4p1:nil="false">ValueHere</e216:BillingThresholdAmount>
        <e216:BusinessAddress d4p1:nil="false">
          <e216:City d4p1:nil="false">ValueHere</e216:City>
          <e216:CountryCode d4p1:nil="false">ValueHere</e216:CountryCode>
          <e216:Id d4p1:nil="false">ValueHere</e216:Id>
          <e216:Line1 d4p1:nil="false">ValueHere</e216:Line1>
          <e216:Line2 d4p1:nil="false">ValueHere</e216:Line2>
          <e216:Line3 d4p1:nil="false">ValueHere</e216:Line3>
          <e216:Line4 d4p1:nil="false">ValueHere</e216:Line4>
          <e216:PostalCode d4p1:nil="false">ValueHere</e216:PostalCode>
          <e216:StateOrProvince d4p1:nil="false">ValueHere</e216:StateOrProvince>
          <e216:TimeStamp d4p1:nil="false">ValueHere</e216:TimeStamp>
          <e216:BusinessName d4p1:nil="false">ValueHere</e216:BusinessName>
        </e216:BusinessAddress>
        <e216:AutoTagType d4p1:nil="false">ValueHere</e216:AutoTagType>
        <e216:SoldToPaymentInstrumentId d4p1:nil="false">ValueHere</e216:SoldToPaymentInstrumentId>
        <e216:TaxCertificate d4p1:nil="false">
          <e216:TaxCertificateBlobContainerName d4p1:nil="false">ValueHere</e216:TaxCertificateBlobContainerName>
          <e216:TaxCertificates xmlns:e219="http://schemas.datacontract.org/2004/07/System.Collections.Generic" d4p1:nil="false">
            <e219:KeyValuePairOfstringbase64Binary>
              <e219:key d4p1:nil="false">ValueHere</e219:key>
              <e219:value d4p1:nil="false">ValueHere</e219:value>
            </e219:KeyValuePairOfstringbase64Binary>
          </e216:TaxCertificates>
          <e216:Status d4p1:nil="false">ValueHere</e216:Status>
        </e216:TaxCertificate>
        <e216:AccountMode d4p1:nil="false">ValueHere</e216:AccountMode>
      </Account>
    </GetAccountResponse>
  </s:Body>
</s:Envelope>
```

## <a name="example"></a>Code Syntax
The example syntax can be used with [Bing Ads SDKs](../guides/client-libraries.md). See [Bing Ads API Code Examples](../guides/code-examples.md) for more examples.
```csharp
public async Task<GetAccountResponse> GetAccountAsync(
	long accountId,
	AccountAdditionalField? returnAdditionalFields)
{
	var request = new GetAccountRequest
	{
		AccountId = accountId,
		ReturnAdditionalFields = returnAdditionalFields
	};

	return (await CustomerManagementService.CallAsync((s, r) => s.GetAccountAsync(r), request));
}
```
```java
static GetAccountResponse getAccount(
	java.lang.Long accountId,
	ArrayList<AccountAdditionalField> returnAdditionalFields) throws RemoteException, Exception
{
	GetAccountRequest request = new GetAccountRequest();

	request.setAccountId(accountId);
	request.setReturnAdditionalFields(returnAdditionalFields);

	return CustomerManagementService.getService().getAccount(request);
}
```
```php
static function GetAccount(
	$accountId,
	$returnAdditionalFields)
{

	$GLOBALS['Proxy'] = $GLOBALS['CustomerManagementProxy'];

	$request = new GetAccountRequest();

	$request->AccountId = $accountId;
	$request->ReturnAdditionalFields = $returnAdditionalFields;

	return $GLOBALS['CustomerManagementProxy']->GetService()->GetAccount($request);
}
```
```python
response=customermanagement_service.GetAccount(
	AccountId=AccountId,
	ReturnAdditionalFields=ReturnAdditionalFields)
```

## Requirements
Service: [CustomerManagementService.svc v13](https://clientcenter.api.bingads.microsoft.com/Api/CustomerManagement/v13/CustomerManagementService.svc)  
Namespace: https\://bingads.microsoft.com/Customer/v13  

