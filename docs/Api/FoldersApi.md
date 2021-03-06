# SendinBlue\Client\FoldersApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createFolder**](FoldersApi.md#createFolder) | **POST** /contacts/folders | Create a folder
[**deleteFolder**](FoldersApi.md#deleteFolder) | **DELETE** /contacts/folders/{folderId} | Delete a folder (and all its lists)
[**getFolder**](FoldersApi.md#getFolder) | **GET** /contacts/folders/{folderId} | Returns folder details
[**getFolderLists**](FoldersApi.md#getFolderLists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
[**getFolders**](FoldersApi.md#getFolders) | **GET** /contacts/folders | Get all the folders
[**updateFolder**](FoldersApi.md#updateFolder) | **PUT** /contacts/folders/{folderId} | Update a contact folder


# **createFolder**
> \SendinBlue\Client\Model\CreateModel createFolder($createFolder)

Create a folder

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$createFolder = new \SendinBlue\Client\Model\CreateUpdateFolder(); // \SendinBlue\Client\Model\CreateUpdateFolder | Name of the folder

try {
    $result = $api_instance->createFolder($createFolder);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->createFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createFolder** | [**\SendinBlue\Client\Model\CreateUpdateFolder**](../Model/CreateUpdateFolder.md)| Name of the folder |

### Return type

[**\SendinBlue\Client\Model\CreateModel**](../Model/CreateModel.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteFolder**
> deleteFolder($folderId)

Delete a folder (and all its lists)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$folderId = 789; // int | Id of the folder

try {
    $api_instance->deleteFolder($folderId);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **int**| Id of the folder |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFolder**
> \SendinBlue\Client\Model\GetFolder getFolder($folderId)

Returns folder details

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$folderId = 789; // int | id of the folder

try {
    $result = $api_instance->getFolder($folderId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->getFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **int**| id of the folder |

### Return type

[**\SendinBlue\Client\Model\GetFolder**](../Model/GetFolder.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFolderLists**
> \SendinBlue\Client\Model\GetFolderLists getFolderLists($folderId, $limit, $offset)

Get the lists in a folder

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$folderId = 789; // int | Id of the folder
$limit = 10; // int | Number of documents per page
$offset = 0; // int | Index of the first document of the page

try {
    $result = $api_instance->getFolderLists($folderId, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->getFolderLists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **int**| Id of the folder |
 **limit** | **int**| Number of documents per page | [optional] [default to 10]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**\SendinBlue\Client\Model\GetFolderLists**](../Model/GetFolderLists.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFolders**
> \SendinBlue\Client\Model\GetFolders getFolders($limit, $offset)

Get all the folders

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$limit = 10; // int | Number of documents per page
$offset = 0; // int | Index of the first document of the page

try {
    $result = $api_instance->getFolders($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->getFolders: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of documents per page | [default to 10]
 **offset** | **int**| Index of the first document of the page | [default to 0]

### Return type

[**\SendinBlue\Client\Model\GetFolders**](../Model/GetFolders.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateFolder**
> updateFolder($folderId, $updateFolder)

Update a contact folder

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// SendinBlue\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('api-key', 'Bearer');

$api_instance = new SendinBlue\Client\Api\FoldersApi();
$folderId = 789; // int | Id of the folder
$updateFolder = new \SendinBlue\Client\Model\CreateUpdateFolder(); // \SendinBlue\Client\Model\CreateUpdateFolder | Name of the folder

try {
    $api_instance->updateFolder($folderId, $updateFolder);
} catch (Exception $e) {
    echo 'Exception when calling FoldersApi->updateFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **int**| Id of the folder |
 **updateFolder** | [**\SendinBlue\Client\Model\CreateUpdateFolder**](../Model/CreateUpdateFolder.md)| Name of the folder |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

