# OpenAPIClient PHP

## Documentation for API Endpoints

All URIs are relative to *https://paella.test10.ozean12.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OrderApi* | [**merchantPayment**](docs/Api/OrderApi.md#merchantpayment) | **POST** /order/{order_id}/confirm-payment | Merchant payment confirmation
*OrderApi* | [**orderFullCancellation**](docs/Api/OrderApi.md#orderfullcancellation) | **POST** /order/{order_id}/cancel | Order full cancellation
*OrderApi* | [**orderPost**](docs/Api/OrderApi.md#orderpost) | **POST** /order | Create new order
*OrderApi* | [**orderShip**](docs/Api/OrderApi.md#ordership) | **POST** /order/{order_id}/ship | Create new order
*OrderApi* | [**patchOrder**](docs/Api/OrderApi.md#patchorder) | **PATCH** /order/{order_id} | Update order amount / duration
*OrderApi* | [**retrieveOrder**](docs/Api/OrderApi.md#retrieveorder) | **GET** /order/{order_id} | Create new order


## Documentation For Models

 - [Amount](docs/Model/Amount.md)
 - [BankAccount](docs/Model/BankAccount.md)
 - [CreateNewOrderApi](docs/Model/CreateNewOrderApi.md)
 - [DebtorCompany](docs/Model/DebtorCompany.md)
 - [DebtorCompanyOnOrderCreatedResponse](docs/Model/DebtorCompanyOnOrderCreatedResponse.md)
 - [DebtorPerson](docs/Model/DebtorPerson.md)
 - [DeliveryAddress](docs/Model/DeliveryAddress.md)
 - [ErrorBlock](docs/Model/ErrorBlock.md)
 - [ErrorUnauthorized](docs/Model/ErrorUnauthorized.md)
 - [Invoice](docs/Model/Invoice.md)
 - [MerchantPaymentRequest](docs/Model/MerchantPaymentRequest.md)
 - [Order](docs/Model/Order.md)
 - [PatchOrder](docs/Model/PatchOrder.md)
 - [ShipOrder](docs/Model/ShipOrder.md)


## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: X-Api-Key
- **Location**: HTTP header


## Author

engineering@billie.io
