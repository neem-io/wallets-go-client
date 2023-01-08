# \DepositWithdrawApi

All URIs are relative to *https://api.dev.neem.io/neem*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CashIn**](DepositWithdrawApi.md#CashIn) | **Post** /api/v1/wallets/cash-in/{walletId} | Cash In
[**CashInInquiry**](DepositWithdrawApi.md#CashInInquiry) | **Get** /api/v1/wallets/cash-in/inquiry/{walletId} | Cash In Inquiry
[**CashOut**](DepositWithdrawApi.md#CashOut) | **Post** /api/v1/wallets/cash-out/{walletId} | Cash Out
[**CashOutInquiry**](DepositWithdrawApi.md#CashOutInquiry) | **Get** /api/v1/wallets/cash-out/inquiry/{walletId} | Cash Out Inquiry



## CashIn

> map[string]interface{} CashIn(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).ContentType(contentType).Body(body).Execute()

Cash In

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    xNeemPartnerId := "1234" // string |  (optional)
    xNeemID := "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c" // string |  (optional)
    contentType := "application/json" // string |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.DepositWithdrawApi.CashIn(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DepositWithdrawApi.CashIn``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `CashIn`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `DepositWithdrawApi.CashIn`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCashInRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemPartnerId** | **string** |  | 
 **xNeemID** | **string** |  | 
 **contentType** | **string** |  | 
 **body** | **map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CashInInquiry

> map[string]interface{} CashInInquiry(ctx, walletId).EndToEndIdentification(endToEndIdentification).Amount(amount).Currency(currency).ExtendedProperties(extendedProperties).Execute()

Cash In Inquiry

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    endToEndIdentification := "endToEndIdentification_example" // string | 
    amount := "amount_example" // string | 
    currency := "currency_example" // string |  (optional)
    extendedProperties := []map[string]interface{}{map[string]interface{}(123)} // []map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.DepositWithdrawApi.CashInInquiry(context.Background(), walletId).EndToEndIdentification(endToEndIdentification).Amount(amount).Currency(currency).ExtendedProperties(extendedProperties).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DepositWithdrawApi.CashInInquiry``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `CashInInquiry`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `DepositWithdrawApi.CashInInquiry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCashInInquiryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **endToEndIdentification** | **string** |  | 
 **amount** | **string** |  | 
 **currency** | **string** |  | 
 **extendedProperties** | **[]map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CashOut

> map[string]interface{} CashOut(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemNonce(xNeemNonce).XNeemOTPCode(xNeemOTPCode).ContentType(contentType).Body(body).Execute()

Cash Out

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    xNeemPartnerId := "1234" // string |  (optional)
    xNeemNonce := "1234" // string |  (optional)
    xNeemOTPCode := "erfdcd345=" // string |  (optional)
    contentType := "application/json" // string |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.DepositWithdrawApi.CashOut(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemNonce(xNeemNonce).XNeemOTPCode(xNeemOTPCode).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DepositWithdrawApi.CashOut``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `CashOut`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `DepositWithdrawApi.CashOut`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCashOutRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemPartnerId** | **string** |  | 
 **xNeemNonce** | **string** |  | 
 **xNeemOTPCode** | **string** |  | 
 **contentType** | **string** |  | 
 **body** | **map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CashOutInquiry

> map[string]interface{} CashOutInquiry(ctx, walletId).EndToEndIdentification(endToEndIdentification).Amount(amount).Currency(currency).ExtendedProperties(extendedProperties).Execute()

Cash Out Inquiry

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    walletId := "walletId_example" // string | 
    endToEndIdentification := "endToEndIdentification_example" // string | 
    amount := "amount_example" // string | 
    currency := "currency_example" // string |  (optional)
    extendedProperties := []map[string]interface{}{map[string]interface{}(123)} // []map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.DepositWithdrawApi.CashOutInquiry(context.Background(), walletId).EndToEndIdentification(endToEndIdentification).Amount(amount).Currency(currency).ExtendedProperties(extendedProperties).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `DepositWithdrawApi.CashOutInquiry``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `CashOutInquiry`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `DepositWithdrawApi.CashOutInquiry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCashOutInquiryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **endToEndIdentification** | **string** |  | 
 **amount** | **string** |  | 
 **currency** | **string** |  | 
 **extendedProperties** | **[]map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[oAuth](../README.md#oAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

