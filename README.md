# Cosmos input binding error

This repo contains 2 functions using the exact same code but different parameters in the cosmos input binding

## TesBindingDocumentExists

The cosmos input binding point to a existing document 

```
"id": "1",
"partitionKey": "1"
```

as result we have a 200 OK when the function is called

## TesBindingDocumentNotExists

The cosmos input binding point to a NON existing document 

```
"id": "2",
"partitionKey": "2"
```

as result we have a 500 Error when the function is called if we check the connected AI the error message is

```
Value cannot be null. (Parameter 'key')
```

There is already a ISSUE on github for the problem https://github.com/Azure/azure-functions-host/issues/6454
The issue is now closed and the fix is already merged in the main branch but there isn't a new release of the runtime.