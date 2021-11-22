# Using a Mantil API

After deploying a Mantil API it will be accessible through its API gateway endpoints.

## REST

Using the REST API is simple, use:
```
mantil invoke <api_name>
```
to invoke the default method, or:
```
mantil invoke <api_name>/<method_name>
```
to invoke a specific method.

You can also get the endpoint using `mantil env -u` and invoke it directly, for example:
```
curl -X POST $(mantil env -u)/<api_name>/<method_name>
```

## WebSocket

Each API can be accessed via WebSocket which is useful for applications that need to update in real time. The WebSocket API can be used in two ways:
1. Publish/Subscribe - An API can publish messages to a subject. Clients can subscribe to this subject to receive new messages.
2. Request/Response - This is used for synchronous communication and is equivalent to calling the regular REST endpoint for the API.

For client-side use we provide a [JavaScript SDK](https://github.com/mantil-io/mantil.js).

A complete example on how to use the WebSocket API can be found in the [chat](https://github.com/mantil-io/template-chat) template.
