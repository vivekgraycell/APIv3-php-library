# SendinBlue\Client\ResellerApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addCredits**](ResellerApi.md#addCredits) | **POST** /reseller/children/{childId}/credits/add | Add Email and/or SMS credits to a specific child account
[**associateIpToChild**](ResellerApi.md#associateIpToChild) | **POST** /reseller/children/{childId}/ips/associate | Associate a dedicated IP to the child
[**createResellerChild**](ResellerApi.md#createResellerChild) | **POST** /reseller/children | Creates a reseller child
[**deleteResellerChild**](ResellerApi.md#deleteResellerChild) | **DELETE** /reseller/children/{childId} | Deletes a single reseller child based on the childId supplied
[**dissociateIpFromChild**](ResellerApi.md#dissociateIpFromChild) | **POST** /reseller/children/{childId}/ips/dissociate | Dissociate a dedicated IP to the child
[**getChildInfo**](ResellerApi.md#getChildInfo) | **GET** /reseller/children/{childId} | Gets the info about a specific child account
[**getResellerChilds**](ResellerApi.md#getResellerChilds) | **GET** /reseller/children | Gets the list of all reseller&#39;s children accounts
[**removeCredits**](ResellerApi.md#removeCredits) | **POST** /reseller/children/{childId}/credits/remove | Remove Email and/or SMS credits from a specific child account
[**updateResellerChild**](ResellerApi.md#updateResellerChild) | **PUT** /reseller/children/{childId} | Updates infos of reseller&#39;s child based on the childId supplied


# **addCredits**
> \SendinBlue\Client\Model\RemainingCreditModel addCredits($childId, $addCredits)

Add Email and/or SMS credits to a specific child account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child
$addCredits = new \SendinBlue\Client\Model\AddCredits(); // \SendinBlue\Client\Model\AddCredits | Values to post to add credit to a specific child account

try {
    $result = $api_instance->addCredits($childId, $addCredits);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->addCredits: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |
 **addCredits** | [**\SendinBlue\Client\Model\AddCredits**](../Model/AddCredits.md)| Values to post to add credit to a specific child account |

### Return type

[**\SendinBlue\Client\Model\RemainingCreditModel**](../Model/RemainingCreditModel.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **associateIpToChild**
> associateIpToChild($childId, $ipId)

Associate a dedicated IP to the child

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child
$ipId = new \SendinBlue\Client\Model\ManageIp(); // \SendinBlue\Client\Model\ManageIp | IP's id

try {
    $api_instance->associateIpToChild($childId, $ipId);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->associateIpToChild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |
 **ipId** | [**\SendinBlue\Client\Model\ManageIp**](../Model/ManageIp.md)| IP&#39;s id |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createResellerChild**
> \SendinBlue\Client\Model\CreateModel createResellerChild($resellerChild)

Creates a reseller child

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$resellerChild = new \SendinBlue\Client\Model\CreateChild(); // \SendinBlue\Client\Model\CreateChild | reseller child to add

try {
    $result = $api_instance->createResellerChild($resellerChild);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->createResellerChild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resellerChild** | [**\SendinBlue\Client\Model\CreateChild**](../Model/CreateChild.md)| reseller child to add | [optional]

### Return type

[**\SendinBlue\Client\Model\CreateModel**](../Model/CreateModel.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteResellerChild**
> deleteResellerChild($childId)

Deletes a single reseller child based on the childId supplied

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child

try {
    $api_instance->deleteResellerChild($childId);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->deleteResellerChild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dissociateIpFromChild**
> dissociateIpFromChild($childId, $ipId)

Dissociate a dedicated IP to the child

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child
$ipId = new \SendinBlue\Client\Model\ManageIp(); // \SendinBlue\Client\Model\ManageIp | IP's id

try {
    $api_instance->dissociateIpFromChild($childId, $ipId);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->dissociateIpFromChild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |
 **ipId** | [**\SendinBlue\Client\Model\ManageIp**](../Model/ManageIp.md)| IP&#39;s id |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChildInfo**
> \SendinBlue\Client\Model\GetChildInfo getChildInfo($childId)

Gets the info about a specific child account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child

try {
    $result = $api_instance->getChildInfo($childId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->getChildInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |

### Return type

[**\SendinBlue\Client\Model\GetChildInfo**](../Model/GetChildInfo.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getResellerChilds**
> \SendinBlue\Client\Model\GetChildrenList getResellerChilds()

Gets the list of all reseller's children accounts

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();

try {
    $result = $api_instance->getResellerChilds();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->getResellerChilds: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\SendinBlue\Client\Model\GetChildrenList**](../Model/GetChildrenList.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeCredits**
> \SendinBlue\Client\Model\RemainingCreditModel removeCredits($childId, $removeCredits)

Remove Email and/or SMS credits from a specific child account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child
$removeCredits = new \SendinBlue\Client\Model\RemoveCredits(); // \SendinBlue\Client\Model\RemoveCredits | Values to post to remove email or SMS credits from a specific child account

try {
    $result = $api_instance->removeCredits($childId, $removeCredits);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->removeCredits: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |
 **removeCredits** | [**\SendinBlue\Client\Model\RemoveCredits**](../Model/RemoveCredits.md)| Values to post to remove email or SMS credits from a specific child account |

### Return type

[**\SendinBlue\Client\Model\RemainingCreditModel**](../Model/RemainingCreditModel.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateResellerChild**
> updateResellerChild($childId, $resellerChild)

Updates infos of reseller's child based on the childId supplied

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\ResellerApi();
$childId = 789; // int | id of reseller's child
$resellerChild = new \SendinBlue\Client\Model\UpdateChild(); // \SendinBlue\Client\Model\UpdateChild | values to update in child profile

try {
    $api_instance->updateResellerChild($childId, $resellerChild);
} catch (Exception $e) {
    echo 'Exception when calling ResellerApi->updateResellerChild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **childId** | **int**| id of reseller&#39;s child |
 **resellerChild** | [**\SendinBlue\Client\Model\UpdateChild**](../Model/UpdateChild.md)| values to update in child profile |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

