# APIClient.GreetingsApi

All URIs are relative to *http://google.com*

Method | Path | Description
------------- | ------------- | -------------
[**Hello**](GreetingsApi.md#Hello) | **Get** /hello | Get a simple greeting!!!



## Hello

Get a simple greeting!!!

### Example

```go
package main

import (
    "fmt"
    "os"
    automationtestwithsubmodules "github.com/konfig-dev/automation-test-submodule-go"
)

func main() {
    configuration := automationtestwithsubmodules.NewConfiguration()
    client := automationtestwithsubmodules.NewAPIClient(configuration)

    request := client.GreetingsApi.Hello(
    )
    
    resp, httpRes, err := request.Execute()

    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `GreetingsApi.Hello``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", httpRes)
    }
    // response from `Hello`: HelloResponse
    fmt.Fprintf(os.Stdout, "Response from `GreetingsApi.Hello`: %v\n", resp)
    fmt.Fprintf(os.Stdout, "Response from `HelloResponse.Hello.Message`: %v\n", resp.Message)
}
```

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

