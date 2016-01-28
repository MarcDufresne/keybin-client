# Keybin Client library

See [Keybin](https://github.com/MarcDufresne/keybin) for the API code and documentation.

## Configuration

Import the library and call the init function to configure the client
    
    import keybin_client
    
    # host: hostname of your Keybin installation (without the trailing '/')
    # username: your Keybin username
    # password: your Keybin password
    # client_id (Optional): the client_id to use for your token. 
                            defaults to 'default' if none is specified
    keybin_client.init(host, username, password, client_id)
        
## Methods

Use these methods to interact with the Keybin API

All methods except the `get_token` can receive a token as an argument, 
but will generate one if no token is specified.

### Get Token

Use this to generate a token from the API. This method can receive an optional `client_id`, they will use 
the `client_id` from `keybin.init()` if none is specified.

    keybin_client.get_token(client_id=None)
    
### List Keys

Lists all the keys for a user

    keybin_client.list_keys(token=None)

### Get Value

Returns the stored value for the specified key

    keybin_client.get_key_value(key, token=None)

### Store Value

Stores the given value for the specified key

    keybin_client.store_key_value(key, value, token=None)

