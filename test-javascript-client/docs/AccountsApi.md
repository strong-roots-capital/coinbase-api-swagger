# CoinbaseApi.AccountsApi

All URIs are relative to *https://api.sandbox.coinbase.com/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountsAccountIdDelete**](AccountsApi.md#accountsAccountIdDelete) | **DELETE** /accounts/{account_id} | Delete account
[**accountsAccountIdGet**](AccountsApi.md#accountsAccountIdGet) | **GET** /accounts/{account_id} | Show an account
[**accountsAccountIdPrimaryGet**](AccountsApi.md#accountsAccountIdPrimaryGet) | **GET** /accounts/{account_id}/primary | Set account as primary
[**accountsAccountIdPut**](AccountsApi.md#accountsAccountIdPut) | **PUT** /accounts/{account_id} | Update account
[**accountsGet**](AccountsApi.md#accountsGet) | **GET** /accounts | List accounts
[**accountsPost**](AccountsApi.md#accountsPost) | **POST** /accounts | Create account


<a name="accountsAccountIdDelete"></a>
# **accountsAccountIdDelete**
> accountsAccountIdDelete(accountId)

Delete account

Removes user\u2019s account. In order to remove an account it can\u2019t be\n\n- Primary account\n- Account with non-zero balance\n- Fiat account\n- Vault with a pending withdrawal\n

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var accountId = "accountId_example"; // {String} The account id


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.accountsAccountIdDelete(accountId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountId** | **String**| The account id | 

### Return type

null (empty response body)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accountsAccountIdGet"></a>
# **accountsAccountIdGet**
> InlineResponse201 accountsAccountIdGet(accountId)

Show an account

Show current user\u2019s account. To access user\u2019s primary account, primary keyword can be used instead of the account id in the URL.

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var accountId = "accountId_example"; // {String} The account id


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.accountsAccountIdGet(accountId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountId** | **String**| The account id | 

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accountsAccountIdPrimaryGet"></a>
# **accountsAccountIdPrimaryGet**
> InlineResponse201 accountsAccountIdPrimaryGet(accountId)

Set account as primary

Promote an account as primary account.

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var accountId = "accountId_example"; // {String} The account id


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.accountsAccountIdPrimaryGet(accountId, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountId** | **String**| The account id | 

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accountsAccountIdPut"></a>
# **accountsAccountIdPut**
> InlineResponse201 accountsAccountIdPut(accountId, opts)

Update account

Modifies user\u2019s account name.

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var accountId = "accountId_example"; // {String} The account id

var opts = { 
  'accountProperties': new CoinbaseApi.AccountProperties1() // {AccountProperties1} Properties to update
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.accountsAccountIdPut(accountId, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountId** | **String**| The account id | 
 **accountProperties** | [**AccountProperties1**](AccountProperties1.md)| Properties to update | [optional] 

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accountsGet"></a>
# **accountsGet**
> InlineResponse200 accountsGet

List accounts

Lists current user\u2019s accounts to which the authentication method has access to.

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.accountsGet(callback);
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="accountsPost"></a>
# **accountsPost**
> InlineResponse201 accountsPost(opts)

Create account

Creates a new account for user.

### Example
```javascript
var CoinbaseApi = require('coinbase-api');
var defaultClient = CoinbaseApi.ApiClient.default;

// Configure OAuth2 access token for authorization: coinbaseAccessCode
var coinbaseAccessCode = defaultClient.authentications['coinbaseAccessCode'];
coinbaseAccessCode.accessToken = "YOUR ACCESS TOKEN"

var apiInstance = new CoinbaseApi.AccountsApi()

var opts = { 
  'accountProperties': new CoinbaseApi.AccountProperties() // {AccountProperties} Account properties
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.accountsPost(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accountProperties** | [**AccountProperties**](AccountProperties.md)| Account properties | [optional] 

### Return type

[**InlineResponse201**](InlineResponse201.md)

### Authorization

[coinbaseAccessCode](../README.md#coinbaseAccessCode)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

