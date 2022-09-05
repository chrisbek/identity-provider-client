# identity_provider_rest_client.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_all_roles_roles_get**](DefaultApi.md#get_all_roles_roles_get) | **GET** /roles | Get All Roles
[**get_all_roles_roles_role_name_get**](DefaultApi.md#get_all_roles_roles_role_name_get) | **GET** /roles/{role_name} | Get All Roles
[**get_role_user_external_identifier_roles_get**](DefaultApi.md#get_role_user_external_identifier_roles_get) | **GET** /user/{external_identifier}/roles | Get Role
[**get_roles_roles_role_name_resource_resource_name_get**](DefaultApi.md#get_roles_roles_role_name_resource_resource_name_get) | **GET** /roles/{role_name}/resource/{resource_name} | Get Roles
[**get_user_user_external_identifier_get**](DefaultApi.md#get_user_user_external_identifier_get) | **GET** /user/{external_identifier} | Get User
[**post_user_user_external_identifier_post**](DefaultApi.md#post_user_user_external_identifier_post) | **POST** /user/{external_identifier} | Post User
[**put_role_roles_put**](DefaultApi.md#put_role_roles_put) | **PUT** /roles | Put Role
[**put_user_user_external_identifier_put**](DefaultApi.md#put_user_user_external_identifier_put) | **PUT** /user/{external_identifier} | Put User


# **get_all_roles_roles_get**
> [SimpleRoleDTO] get_all_roles_roles_get()

Get All Roles

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.simple_role_dto import SimpleRoleDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    limit = 10 # int |  (optional) if omitted the server will use the default value of 10

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Get All Roles
        api_response = api_instance.get_all_roles_roles_get(limit=limit)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_all_roles_roles_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**|  | [optional] if omitted the server will use the default value of 10

### Return type

[**[SimpleRoleDTO]**](SimpleRoleDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_all_roles_roles_role_name_get**
> [SimpleRoleDTO] get_all_roles_roles_role_name_get(role_name)

Get All Roles

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.simple_role_dto import SimpleRoleDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    role_name = "role_name_example" # str | 
    limit = 10 # int |  (optional) if omitted the server will use the default value of 10

    # example passing only required values which don't have defaults set
    try:
        # Get All Roles
        api_response = api_instance.get_all_roles_roles_role_name_get(role_name)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_all_roles_roles_role_name_get: %s\n" % e)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Get All Roles
        api_response = api_instance.get_all_roles_roles_role_name_get(role_name, limit=limit)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_all_roles_roles_role_name_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role_name** | **str**|  |
 **limit** | **int**|  | [optional] if omitted the server will use the default value of 10

### Return type

[**[SimpleRoleDTO]**](SimpleRoleDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_role_user_external_identifier_roles_get**
> [SimpleRoleDTO] get_role_user_external_identifier_roles_get(external_identifier)

Get Role

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.simple_role_dto import SimpleRoleDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    external_identifier = "external_identifier_example" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Get Role
        api_response = api_instance.get_role_user_external_identifier_roles_get(external_identifier)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_role_user_external_identifier_roles_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_identifier** | **str**|  |

### Return type

[**[SimpleRoleDTO]**](SimpleRoleDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_roles_roles_role_name_resource_resource_name_get**
> [SimpleRoleDTO] get_roles_roles_role_name_resource_resource_name_get(role_name, resource_name)

Get Roles

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.simple_role_dto import SimpleRoleDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    role_name = "role_name_example" # str | 
    resource_name = "resource_name_example" # str | 
    limit = 10 # int |  (optional) if omitted the server will use the default value of 10

    # example passing only required values which don't have defaults set
    try:
        # Get Roles
        api_response = api_instance.get_roles_roles_role_name_resource_resource_name_get(role_name, resource_name)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_roles_roles_role_name_resource_resource_name_get: %s\n" % e)

    # example passing only required values which don't have defaults set
    # and optional values
    try:
        # Get Roles
        api_response = api_instance.get_roles_roles_role_name_resource_resource_name_get(role_name, resource_name, limit=limit)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_roles_roles_role_name_resource_resource_name_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role_name** | **str**|  |
 **resource_name** | **str**|  |
 **limit** | **int**|  | [optional] if omitted the server will use the default value of 10

### Return type

[**[SimpleRoleDTO]**](SimpleRoleDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_user_external_identifier_get**
> UserOutDTO get_user_user_external_identifier_get(external_identifier)

Get User

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.user_out_dto import UserOutDTO
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    external_identifier = "external_identifier_example" # str | 

    # example passing only required values which don't have defaults set
    try:
        # Get User
        api_response = api_instance.get_user_user_external_identifier_get(external_identifier)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->get_user_user_external_identifier_get: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_identifier** | **str**|  |

### Return type

[**UserOutDTO**](UserOutDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_user_user_external_identifier_post**
> UserOutDTO post_user_user_external_identifier_post(external_identifier, user_in_dto)

Post User

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.user_in_dto import UserInDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.user_out_dto import UserOutDTO
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    external_identifier = "external_identifier_example" # str | 
    user_in_dto = UserInDTO(
        roles=[
            SimpleRoleDTO(
                role="role_example",
            ),
        ],
        email_address="email_address_example",
        first_name="first_name_example",
    ) # UserInDTO | 

    # example passing only required values which don't have defaults set
    try:
        # Post User
        api_response = api_instance.post_user_user_external_identifier_post(external_identifier, user_in_dto)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->post_user_user_external_identifier_post: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_identifier** | **str**|  |
 **user_in_dto** | [**UserInDTO**](UserInDTO.md)|  |

### Return type

[**UserOutDTO**](UserOutDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**409** | Conflict |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_role_roles_put**
> SimpleRoleDTO put_role_roles_put(simple_role_dto)

Put Role

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.simple_role_dto import SimpleRoleDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    simple_role_dto = SimpleRoleDTO(
        role="role_example",
    ) # SimpleRoleDTO | 

    # example passing only required values which don't have defaults set
    try:
        # Put Role
        api_response = api_instance.put_role_roles_put(simple_role_dto)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->put_role_roles_put: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **simple_role_dto** | [**SimpleRoleDTO**](SimpleRoleDTO.md)|  |

### Return type

[**SimpleRoleDTO**](SimpleRoleDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**409** | Conflict |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_user_user_external_identifier_put**
> UserOutDTO put_user_user_external_identifier_put(external_identifier, user_in_dto)

Put User

### Example

```python
import time
import identity_provider_rest_client
from Api import default_api
from identity_provider_rest_client.model.user_in_dto import UserInDTO
from identity_provider_rest_client.model.server_exception_model import ServerExceptionModel
from identity_provider_rest_client.model.user_out_dto import UserOutDTO
from identity_provider_rest_client.model.http_validation_error import HTTPValidationError
from identity_provider_rest_client.model.business_exception_model import BusinessExceptionModel
from pprint import pprint
# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = identity_provider_rest_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with identity_provider_rest_client.ApiClient() as api_client:
    # Create an instance of the API class
    api_instance = default_api.DefaultApi(api_client)
    external_identifier = "external_identifier_example" # str | 
    user_in_dto = UserInDTO(
        roles=[
            SimpleRoleDTO(
                role="role_example",
            ),
        ],
        email_address="email_address_example",
        first_name="first_name_example",
    ) # UserInDTO | 

    # example passing only required values which don't have defaults set
    try:
        # Put User
        api_response = api_instance.put_user_user_external_identifier_put(external_identifier, user_in_dto)
        pprint(api_response)
    except identity_provider_rest_client.ApiException as e:
        print("Exception when calling DefaultApi->put_user_user_external_identifier_put: %s\n" % e)
```


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **external_identifier** | **str**|  |
 **user_in_dto** | [**UserInDTO**](UserInDTO.md)|  |

### Return type

[**UserOutDTO**](UserOutDTO.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**409** | Conflict |  -  |
**404** | Not Found |  -  |
**500** | Internal Server Error |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

