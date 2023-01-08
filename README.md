# Go API client for openapi

Integrate Neem Wallet APIs into your ecosystem to provide your customer the ability to create wallets, set up a financial PIN, ability to manage their wallets and have on request visibility over their balances.

## Overview
This API client was generated by the [OpenAPI Generator](https://openapi-generator.tech) project.  By using the [OpenAPI-spec](https://www.openapis.org/) from a remote server, you can easily generate an API client.

- API version: 1.0.3
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.GoClientCodegen

## Installation

Install the following dependencies:

```shell
go get github.com/stretchr/testify/assert
go get golang.org/x/oauth2
go get golang.org/x/net/context
```

Put the package under your project folder and add the following in import:

```golang
import openapi "github.com/GIT_USER_ID/GIT_REPO_ID"
```

To use a proxy, set the environment variable `HTTP_PROXY`:

```golang
os.Setenv("HTTP_PROXY", "http://proxy_name:proxy_port")
```

## Configuration of Server URL

Default configuration comes with `Servers` field that contains server objects as defined in the OpenAPI specification.

### Select Server Configuration

For using other server than the one defined on index 0 set context value `sw.ContextServerIndex` of type `int`.

```golang
ctx := context.WithValue(context.Background(), openapi.ContextServerIndex, 1)
```

### Templated Server URL

Templated server URL is formatted using default variables from configuration or from context value `sw.ContextServerVariables` of type `map[string]string`.

```golang
ctx := context.WithValue(context.Background(), openapi.ContextServerVariables, map[string]string{
	"basePath": "v2",
})
```

Note, enum values are always validated and all unused variables are silently ignored.

### URLs Configuration per Operation

Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"{classname}Service.{nickname}"` string.
Similar rules for overriding default operation server index and variables applies by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), openapi.ContextOperationServerIndices, map[string]int{
	"{classname}Service.{nickname}": 2,
})
ctx = context.WithValue(context.Background(), openapi.ContextOperationServerVariables, map[string]map[string]string{
	"{classname}Service.{nickname}": {
		"port": "8443",
	},
})
```

## Documentation for API Endpoints

All URIs are relative to *https://api.dev.neem.io/neem*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DepositWithdrawApi* | [**CashIn**](docs/DepositWithdrawApi.md#cashin) | **Post** /api/v1/wallets/cash-in/{walletId} | Cash In
*DepositWithdrawApi* | [**CashInInquiry**](docs/DepositWithdrawApi.md#cashininquiry) | **Get** /api/v1/wallets/cash-in/inquiry/{walletId} | Cash In Inquiry
*DepositWithdrawApi* | [**CashOut**](docs/DepositWithdrawApi.md#cashout) | **Post** /api/v1/wallets/cash-out/{walletId} | Cash Out
*DepositWithdrawApi* | [**CashOutInquiry**](docs/DepositWithdrawApi.md#cashoutinquiry) | **Get** /api/v1/wallets/cash-out/inquiry/{walletId} | Cash Out Inquiry
*OnboardingApi* | [**CreateAccount**](docs/OnboardingApi.md#createaccount) | **Post** /api/v1/wallets/account | Create Account
*OnboardingApi* | [**CreateMpin**](docs/OnboardingApi.md#creatempin) | **Post** /api/v1/wallets/create-mpin/{walletId} | Create Mpin
*OnboardingApi* | [**Login**](docs/OnboardingApi.md#login) | **Post** /api/v1/wallets/login | Login
*WalletServicesApi* | [**AccountLookup**](docs/WalletServicesApi.md#accountlookup) | **Get** /api/v1/wallets/account/{walletId} | Account Lookup
*WalletServicesApi* | [**AccountUpgrade**](docs/WalletServicesApi.md#accountupgrade) | **Post** /api/v1/wallets/upgrade/{walletId} | Account Upgrade
*WalletServicesApi* | [**ApiV1WalletsValidateOtpPost**](docs/WalletServicesApi.md#apiv1walletsvalidateotppost) | **Post** /api/v1/wallets/validate-otp | Validate OTP
*WalletServicesApi* | [**BalanceInquiry**](docs/WalletServicesApi.md#balanceinquiry) | **Get** /api/v1/wallets/balance/{walletId} | Balance Inquiry
*WalletServicesApi* | [**ChangeMpin**](docs/WalletServicesApi.md#changempin) | **Post** /api/v1/wallets/change-mpin/{walletId} | Change MPIN
*WalletServicesApi* | [**InitiateOtp**](docs/WalletServicesApi.md#initiateotp) | **Post** /api/v1/wallets/initiate-otp | Initiate OTP
*WalletServicesApi* | [**TransactionHistory**](docs/WalletServicesApi.md#transactionhistory) | **Get** /api/v1/wallets/transaction-history/{walletId} | Transaction History


## Documentation For Models



## Documentation For Authorization



### oAuth


- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
 - **email**: Email as scope

Example

```golang
auth := context.WithValue(context.Background(), sw.ContextAccessToken, "ACCESSTOKENSTRING")
r, err := client.Service.Operation(auth, args)
```

Or via OAuth2 module to automatically refresh tokens and perform user authentication.

```golang
import "golang.org/x/oauth2"

/* Perform OAuth2 round trip request and obtain a token */

tokenSource := oauth2cfg.TokenSource(createContext(httpClient), &token)
auth := context.WithValue(oauth2.NoContext, sw.ContextOAuth2, tokenSource)
r, err := client.Service.Operation(auth, args)
```


## Documentation for Utility Methods

Due to the fact that model structure members are all pointers, this package contains
a number of utility functions to easily obtain pointers to values of basic types.
Each of these functions takes a value of the given basic type and returns a pointer to it:

* `PtrBool`
* `PtrInt`
* `PtrInt32`
* `PtrInt64`
* `PtrFloat`
* `PtrFloat32`
* `PtrFloat64`
* `PtrString`
* `PtrTime`

## Author


