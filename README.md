# automationtestwithsubmodules - 's Go SDK

SDKs (no submodules) to test automation workflows.


## Installation

Add to your project:

```shell
go get github.com/konfig-dev/automation-test-submodule-go
```

## Getting Started

```golang
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

## Documentation for API Endpoints

All URIs are relative to *http://google.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*GreetingsApi* | [**Hello**](docs/GreetingsApi.md#hello) | **Get** /hello | Get a simple greeting!!!


## Documentation For Models

 - [HelloResponse](docs/HelloResponse.md)
