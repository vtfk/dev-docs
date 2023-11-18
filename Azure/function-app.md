# Function app
## Authentication
### Keys
If you are using keys as authentication type or "authType": "function", you need to create a host key to be able to access your functions. Navigate to the Function app in the Azure portal, and create a new host key.

![image](https://github.com/vtfk/dev-docs/assets/25528003/8ac5aa9a-e975-45b3-803d-c1d9b675365e)

A host key should only be used ONE single place - for easy rotation management of the key. If you need to access the function from something - create a new key.

To access a function with the key, it is reccommended to pass the key in the header "x-functions-key" (` Headers: { "x-functions-key": <your-key> }`) . If you have to use url query params, you pass it as `?code={key]` in the url.