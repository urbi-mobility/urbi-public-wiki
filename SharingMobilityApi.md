# SharingMobilityApi

All URIs are relative to *https://apigw.urbi.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getCurrent**](SharingMobilityApi.md#getCurrent) | **GET** /api/sm/current | Get user current rentals.
[**getMapItemDetailStation**](SharingMobilityApi.md#getMapItemDetailStation) | **GET** /api/sm/providers/{providerId}/stations/{stationId}/detail | Gets station by provider id and station id
[**getMapItemDetailVehicle**](SharingMobilityApi.md#getMapItemDetailVehicle) | **GET** /api/sm/providers/{providerId}/vehicles/{vehicleId}/detail | Gets vehicle by provider id and vehicle id
[**getStatus**](SharingMobilityApi.md#getStatus) | **GET** /api/sm/rentals/{rentalId}/status | Get rental status from provider.
[**getUnlockCode**](SharingMobilityApi.md#getUnlockCode) | **GET** /api/sm/rentals/{rentalId}/unlockCode | Get rental vehicle&#39;s unlock code.
[**postCancelReservedRental**](SharingMobilityApi.md#postCancelReservedRental) | **POST** /api/sm/rentals/{rentalId}/cancel | Cancel a specific reserved rental.
[**postEndRental**](SharingMobilityApi.md#postEndRental) | **POST** /api/sm/rentals/{rentalId}/end | End a specific rental.
[**postFindClosest**](SharingMobilityApi.md#postFindClosest) | **POST** /api/sm/items/closest | Search nearby map items.
[**postFindVehicle**](SharingMobilityApi.md#postFindVehicle) | **POST** /api/sm/vehicles/find | Find vehicle by code.
[**postMapItemsSearch**](SharingMobilityApi.md#postMapItemsSearch) | **POST** /api/sm/mapItems/search | Search map items by providers and area; filters like fuel amount, number of seats, engine type and transmission type can be also applied.
[**postOpenReservedRental**](SharingMobilityApi.md#postOpenReservedRental) | **POST** /api/sm/rentals/{rentalId}/open | Open a specific reserved rental.
[**postOpenSeat**](SharingMobilityApi.md#postOpenSeat) | **POST** /api/sm/rentals/{rentalId}/openSeat | Open a container on the vehicle.
[**postOpenVehicle**](SharingMobilityApi.md#postOpenVehicle) | **POST** /api/sm/rentals/open | Open a specific vehicle.
[**postParkRental**](SharingMobilityApi.md#postParkRental) | **POST** /api/sm/rentals/{rentalId}/park | Park a running vehicle.
[**postReserveVehicle**](SharingMobilityApi.md#postReserveVehicle) | **POST** /api/sm/rentals/reserve | Reserve a specific vehicle.
[**postUnparkRental**](SharingMobilityApi.md#postUnparkRental) | **POST** /api/sm/rentals/{rentalId}/unpark | Unpark a parked vehicle.


<a name="getCurrent"></a>
# **getCurrent**
> SMCurrentResponse getCurrent()

Get user current rentals.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
try {
    val result : SMCurrentResponse = apiInstance.getCurrent()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#getCurrent")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#getCurrent")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**SMCurrentResponse**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getMapItemDetailStation"></a>
# **getMapItemDetailStation**
> SMMapItemDetailStation getMapItemDetailStation(providerId, stationId)

Gets station by provider id and station id

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val providerId : kotlin.String = providerId_example // kotlin.String | Provider Id.
val stationId : kotlin.String = stationId_example // kotlin.String | Provider station Id.
try {
    val result : SMMapItemDetailStation = apiInstance.getMapItemDetailStation(providerId, stationId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#getMapItemDetailStation")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#getMapItemDetailStation")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **providerId** | **kotlin.String**| Provider Id. |
 **stationId** | **kotlin.String**| Provider station Id. |

### Return type

**SMMapItemDetailStation**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getMapItemDetailVehicle"></a>
# **getMapItemDetailVehicle**
> SMMapItemDetailVehicle getMapItemDetailVehicle(providerId, vehicleId)

Gets vehicle by provider id and vehicle id

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val providerId : kotlin.String = providerId_example // kotlin.String | Provider Id.
val vehicleId : kotlin.String = vehicleId_example // kotlin.String | Provider vehicle Id.
try {
    val result : SMMapItemDetailVehicle = apiInstance.getMapItemDetailVehicle(providerId, vehicleId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#getMapItemDetailVehicle")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#getMapItemDetailVehicle")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **providerId** | **kotlin.String**| Provider Id. |
 **vehicleId** | **kotlin.String**| Provider vehicle Id. |

### Return type

**SMMapItemDetailVehicle**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getStatus"></a>
# **getStatus**
> SMRental getStatus(rentalId)

Get rental status from provider.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
try {
    val result : SMRental = apiInstance.getStatus(rentalId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#getStatus")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#getStatus")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getUnlockCode"></a>
# **getUnlockCode**
> CommCode getUnlockCode(rentalId)

Get rental vehicle&#39;s unlock code.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
try {
    val result : CommCode = apiInstance.getUnlockCode(rentalId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#getUnlockCode")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#getUnlockCode")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |

### Return type

**CommCode**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="postCancelReservedRental"></a>
# **postCancelReservedRental**
> SMRental postCancelReservedRental(rentalId, smCancelReservedRentalRequest)

Cancel a specific reserved rental.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
val smCancelReservedRentalRequest : SMCancelReservedRentalRequest =  // SMCancelReservedRentalRequest | 
try {
    val result : SMRental = apiInstance.postCancelReservedRental(rentalId, smCancelReservedRentalRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postCancelReservedRental")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postCancelReservedRental")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |
 **smCancelReservedRentalRequest** | **SMCancelReservedRentalRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postEndRental"></a>
# **postEndRental**
> SMRental postEndRental(rentalId, smEndRentalRequest)

End a specific rental.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
val smEndRentalRequest : SMEndRentalRequest =  // SMEndRentalRequest | 
try {
    val result : SMRental = apiInstance.postEndRental(rentalId, smEndRentalRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postEndRental")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postEndRental")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |
 **smEndRentalRequest** | **SMEndRentalRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postFindClosest"></a>
# **postFindClosest**
> SMClosestResponse postFindClosest(smClosestRequest)

Search nearby map items.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smClosestRequest : SMClosestRequest =  // SMClosestRequest | 
try {
    val result : SMClosestResponse = apiInstance.postFindClosest(smClosestRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postFindClosest")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postFindClosest")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smClosestRequest** | **SMClosestRequest**|  |

### Return type

**SMClosestResponse**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postFindVehicle"></a>
# **postFindVehicle**
> SMFindVehicleResponse postFindVehicle(smFindVehicleRequest)

Find vehicle by code.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smFindVehicleRequest : SMFindVehicleRequest =  // SMFindVehicleRequest | 
try {
    val result : SMFindVehicleResponse = apiInstance.postFindVehicle(smFindVehicleRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postFindVehicle")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postFindVehicle")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smFindVehicleRequest** | **SMFindVehicleRequest**|  |

### Return type

**SMFindVehicleResponse**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postMapItemsSearch"></a>
# **postMapItemsSearch**
> SMMapItemResponse postMapItemsSearch(smSearchMapItemsRequest)

Search map items by providers and area; filters like fuel amount, number of seats, engine type and transmission type can be also applied.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smSearchMapItemsRequest : SMSearchMapItemsRequest =  // SMSearchMapItemsRequest | 
try {
    val result : SMMapItemResponse = apiInstance.postMapItemsSearch(smSearchMapItemsRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postMapItemsSearch")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postMapItemsSearch")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smSearchMapItemsRequest** | **SMSearchMapItemsRequest**|  |

### Return type

**SMMapItemResponse**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postOpenReservedRental"></a>
# **postOpenReservedRental**
> SMRental postOpenReservedRental(rentalId, smOpenReservedRentalRequest)

Open a specific reserved rental.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
val smOpenReservedRentalRequest : SMOpenReservedRentalRequest =  // SMOpenReservedRentalRequest | 
try {
    val result : SMRental = apiInstance.postOpenReservedRental(rentalId, smOpenReservedRentalRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postOpenReservedRental")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postOpenReservedRental")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |
 **smOpenReservedRentalRequest** | **SMOpenReservedRentalRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postOpenSeat"></a>
# **postOpenSeat**
> postOpenSeat(rentalId)

Open a container on the vehicle.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val rentalId : kotlin.Int = 56 // kotlin.Int | Urbi generated rental Id.
try {
    apiInstance.postOpenSeat(rentalId)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postOpenSeat")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postOpenSeat")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rentalId** | **kotlin.Int**| Urbi generated rental Id. |

### Return type

null (empty response body)

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="postOpenVehicle"></a>
# **postOpenVehicle**
> SMRental postOpenVehicle(smOpenVehicleRequest)

Open a specific vehicle.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smOpenVehicleRequest : SMOpenVehicleRequest =  // SMOpenVehicleRequest | 
try {
    val result : SMRental = apiInstance.postOpenVehicle(smOpenVehicleRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postOpenVehicle")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postOpenVehicle")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smOpenVehicleRequest** | **SMOpenVehicleRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postParkRental"></a>
# **postParkRental**
> SMRental postParkRental(smParkRentalRequest)

Park a running vehicle.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smParkRentalRequest : SMParkRentalRequest =  // SMParkRentalRequest | 
try {
    val result : SMRental = apiInstance.postParkRental(smParkRentalRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postParkRental")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postParkRental")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smParkRentalRequest** | **SMParkRentalRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postReserveVehicle"></a>
# **postReserveVehicle**
> SMRental postReserveVehicle(smReserveVehicleRequest)

Reserve a specific vehicle.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smReserveVehicleRequest : SMReserveVehicleRequest =  // SMReserveVehicleRequest | 
try {
    val result : SMRental = apiInstance.postReserveVehicle(smReserveVehicleRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postReserveVehicle")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postReserveVehicle")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smReserveVehicleRequest** | **SMReserveVehicleRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="postUnparkRental"></a>
# **postUnparkRental**
> SMRental postUnparkRental(smUnparkRentalRequest)

Unpark a parked vehicle.

### Example
```kotlin
// Import classes:
//import org.openapitools.client.infrastructure.*
//import co.urbi.openapi.model.*

val apiInstance = SharingMobilityApi()
val smUnparkRentalRequest : SMUnparkRentalRequest =  // SMUnparkRentalRequest | 
try {
    val result : SMRental = apiInstance.postUnparkRental(smUnparkRentalRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling SharingMobilityApi#postUnparkRental")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling SharingMobilityApi#postUnparkRental")
    e.printStackTrace()
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smUnparkRentalRequest** | **SMUnparkRentalRequest**|  |

### Return type

**SMRental**

### Authorization


Configure bearerAuth:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

