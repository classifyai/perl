# WWW::OpenAPIClient::DefaultApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DefaultApi;
```

All URIs are relative to *https://api.classifyai.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_new_model**](DefaultApi.md#create_new_model) | **PUT** /models | Create New Model
[**delete_model**](DefaultApi.md#delete_model) | **DELETE** /models | Delete Model
[**get_models_list**](DefaultApi.md#get_models_list) | **GET** /models | Get Models List
[**index_by_image_url**](DefaultApi.md#index_by_image_url) | **GET** /index_by_image_url | Index by Using Image URL
[**index_image**](DefaultApi.md#index_image) | **POST** /index_image | Index Local Image
[**tag_image_by_url**](DefaultApi.md#tag_image_by_url) | **GET** /predict_by_image_url | Tag Image by Using Image Url
[**tag_local_image**](DefaultApi.md#tag_local_image) | **POST** /predict | Predict by Image
[**update_model**](DefaultApi.md#update_model) | **POST** /models | Update Model


# **create_new_model**
> create_new_model(model_name => $model_name)

Create New Model

Create a new custom image recognition model

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_name = {"model_name":"\"Test model name\""}; # string | Set a name for your model

eval { 
    $api_instance->create_new_model(model_name => $model_name);
};
if ($@) {
    warn "Exception when calling DefaultApi->create_new_model: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_name** | **string**| Set a name for your model | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_model**
> delete_model(model_id => $model_id)

Delete Model

Delete Model

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_id = "model_id_example"; # string | You can find your model ids from Classify Dashboard.

eval { 
    $api_instance->delete_model(model_id => $model_id);
};
if ($@) {
    warn "Exception when calling DefaultApi->delete_model: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| You can find your model ids from Classify Dashboard. | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_models_list**
> string get_models_list()

Get Models List

Get the list of of models created 

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);


eval { 
    my $result = $api_instance->get_models_list();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DefaultApi->get_models_list: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **index_by_image_url**
> string index_by_image_url(model_id => $model_id, image_url => $image_url)

Index by Using Image URL

Index by Using Image URL

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_id = "model_id_example"; # string | Model ID
my $image_url = "image_url_example"; # string | Image URL

eval { 
    my $result = $api_instance->index_by_image_url(model_id => $model_id, image_url => $image_url);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DefaultApi->index_by_image_url: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| Model ID | 
 **image_url** | **string**| Image URL | 

### Return type

**string**

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **index_image**
> string index_image(model_id => $model_id, file => $file)

Index Local Image

Index Local Image

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_id = "model_id_example"; # string | Model ID
my $file = "/path/to/file"; # string | 

eval { 
    my $result = $api_instance->index_image(model_id => $model_id, file => $file);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DefaultApi->index_image: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| Model ID | 
 **file** | **string****string**|  | [optional] 

### Return type

**string**

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tag_image_by_url**
> tag_image_by_url(model_id => $model_id, image_url => $image_url)

Tag Image by Using Image Url

Predict image tags by providing image url

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_id = "model_id_example"; # string | Type your trained model id to predict. You get your model's id from Classify Dashboard.
my $image_url = "image_url_example"; # string | Provide image url to predict

eval { 
    $api_instance->tag_image_by_url(model_id => $model_id, image_url => $image_url);
};
if ($@) {
    warn "Exception when calling DefaultApi->tag_image_by_url: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **image_url** | **string**| Provide image url to predict | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tag_local_image**
> tag_local_image(model_id => $model_id, file => $file)

Predict by Image

Send a local image to tag

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_id = "model_id_example"; # string | Type your trained model id to predict. You get your model's id from Classify Dashboard.
my $file = "/path/to/file"; # string | 

eval { 
    $api_instance->tag_local_image(model_id => $model_id, file => $file);
};
if ($@) {
    warn "Exception when calling DefaultApi->tag_local_image: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. | 
 **file** | **string****string**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_model**
> update_model(model_name => $model_name, model_id => $model_id)

Update Model

Update Model Name

### Example 
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DefaultApi;
my $api_instance = WWW::OpenAPIClient::DefaultApi->new(

    # Configure API key authorization: x-api-key
    api_key => {'x-api-key' => 'YOUR_API_KEY'},
    # uncomment below to setup prefix (e.g. Bearer) for API key, if needed
    #api_key_prefix => {'x-api-key' => 'Bearer'},
);

my $model_name = "model_name_example"; # string | Model Name
my $model_id = "model_id_example"; # string | Model id to be renamed.

eval { 
    $api_instance->update_model(model_name => $model_name, model_id => $model_id);
};
if ($@) {
    warn "Exception when calling DefaultApi->update_model: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_name** | **string**| Model Name | 
 **model_id** | **string**| Model id to be renamed. | 

### Return type

void (empty response body)

### Authorization

[x-api-key](../README.md#x-api-key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

