# \WalletServicesApi

All URIs are relative to *https://api.dev.neem.io/neem*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AccountLookup**](WalletServicesApi.md#AccountLookup) | **Get** /api/v1/wallets/account/{walletId} | Account Lookup
[**AccountUpgrade**](WalletServicesApi.md#AccountUpgrade) | **Post** /api/v1/wallets/upgrade/{walletId} | Account Upgrade
[**ApiV1WalletsValidateOtpPost**](WalletServicesApi.md#ApiV1WalletsValidateOtpPost) | **Post** /api/v1/wallets/validate-otp | Validate OTP
[**BalanceInquiry**](WalletServicesApi.md#BalanceInquiry) | **Get** /api/v1/wallets/balance/{walletId} | Balance Inquiry
[**ChangeMpin**](WalletServicesApi.md#ChangeMpin) | **Post** /api/v1/wallets/change-mpin/{walletId} | Change MPIN
[**InitiateOtp**](WalletServicesApi.md#InitiateOtp) | **Post** /api/v1/wallets/initiate-otp | Initiate OTP
[**TransactionHistory**](WalletServicesApi.md#TransactionHistory) | **Get** /api/v1/wallets/transaction-history/{walletId} | Transaction History



## AccountLookup

> map[string]interface{} AccountLookup(ctx, walletId).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).XNeemCNIC(xNeemCNIC).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Execute()

Account Lookup

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
    schemeName := "schemeName_example" // string | 
    xNeemCNIC := "xNeemCNIC_example" // string | 
    xNeemPartnerId := "1234" // string |  (optional)
    contentType := "application/json" // string |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.AccountLookup(context.Background(), walletId).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).XNeemCNIC(xNeemCNIC).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.AccountLookup``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `AccountLookup`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.AccountLookup`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAccountLookupRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **endToEndIdentification** | **string** |  | 
 **schemeName** | **string** |  | 
 **xNeemCNIC** | **string** |  | 
 **xNeemPartnerId** | **string** |  | 
 **contentType** | **string** |  | 

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


## AccountUpgrade

> map[string]interface{} AccountUpgrade(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).ContentType(contentType).Body(body).Execute()

Account Upgrade

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
    resp, r, err := apiClient.WalletServicesApi.AccountUpgrade(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.AccountUpgrade``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `AccountUpgrade`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.AccountUpgrade`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAccountUpgradeRequest struct via the builder pattern


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


## ApiV1WalletsValidateOtpPost

> map[string]interface{} ApiV1WalletsValidateOtpPost(ctx).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Body(body).Execute()

Validate OTP

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
    xNeemPartnerId := "1234" // string |  (optional)
    contentType := "application/json" // string |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.ApiV1WalletsValidateOtpPost(context.Background()).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.ApiV1WalletsValidateOtpPost``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `ApiV1WalletsValidateOtpPost`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.ApiV1WalletsValidateOtpPost`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiApiV1WalletsValidateOtpPostRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xNeemPartnerId** | **string** |  | 
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


## BalanceInquiry

> map[string]interface{} BalanceInquiry(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).ExtendedProperties(extendedProperties).Execute()

Balance Inquiry

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
    walletId := int32(56) // int32 | 
    xNeemPartnerId := "1234" // string |  (optional)
    xNeemID := "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c" // string |  (optional)
    endToEndIdentification := int32(56) // int32 |  (optional)
    schemeName := "schemeName_example" // string |  (optional)
    extendedProperties := []map[string]interface{}{map[string]interface{}(123)} // []map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.BalanceInquiry(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).ExtendedProperties(extendedProperties).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.BalanceInquiry``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `BalanceInquiry`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.BalanceInquiry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **int32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiBalanceInquiryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemPartnerId** | **string** |  | 
 **xNeemID** | **string** |  | 
 **endToEndIdentification** | **int32** |  | 
 **schemeName** | **string** |  | 
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


## ChangeMpin

> map[string]interface{} ChangeMpin(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).XNeemOTP(xNeemOTP).ContentType(contentType).Body(body).Execute()

Change MPIN

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
    xNeemOTP := "erfdcd345=" // string |  (optional)
    contentType := "application/json" // string |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.ChangeMpin(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).XNeemOTP(xNeemOTP).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.ChangeMpin``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `ChangeMpin`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.ChangeMpin`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiChangeMpinRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemPartnerId** | **string** |  | 
 **xNeemID** | **string** |  | 
 **xNeemOTP** | **string** |  | 
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


## InitiateOtp

> map[string]interface{} InitiateOtp(ctx).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Body(body).Execute()

Initiate OTP

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
    xNeemPartnerId := "1234" // string |  (optional)
    contentType := "application/json" // string |  (optional)
    body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.InitiateOtp(context.Background()).XNeemPartnerId(xNeemPartnerId).ContentType(contentType).Body(body).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.InitiateOtp``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `InitiateOtp`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.InitiateOtp`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiInitiateOtpRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xNeemPartnerId** | **string** |  | 
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


## TransactionHistory

> map[string]interface{} TransactionHistory(ctx, walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).FromDate(fromDate).ToDate(toDate).ExtendedProperties(extendedProperties).Execute()

Transaction History

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
    walletId := int32(56) // int32 | 
    xNeemPartnerId := "1234" // string |  (optional)
    xNeemID := "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c" // string |  (optional)
    endToEndIdentification := int32(56) // int32 |  (optional)
    schemeName := int32(56) // int32 |  (optional)
    fromDate := "fromDate_example" // string |  (optional)
    toDate := "toDate_example" // string |  (optional)
    extendedProperties := []map[string]interface{}{map[string]interface{}(123)} // []map[string]interface{} |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.WalletServicesApi.TransactionHistory(context.Background(), walletId).XNeemPartnerId(xNeemPartnerId).XNeemID(xNeemID).EndToEndIdentification(endToEndIdentification).SchemeName(schemeName).FromDate(fromDate).ToDate(toDate).ExtendedProperties(extendedProperties).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `WalletServicesApi.TransactionHistory``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `TransactionHistory`: map[string]interface{}
    fmt.Fprintf(os.Stdout, "Response from `WalletServicesApi.TransactionHistory`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**walletId** | **int32** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiTransactionHistoryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xNeemPartnerId** | **string** |  | 
 **xNeemID** | **string** |  | 
 **endToEndIdentification** | **int32** |  | 
 **schemeName** | **int32** |  | 
 **fromDate** | **string** |  | 
 **toDate** | **string** |  | 
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

