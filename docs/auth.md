# Authencation system

* Irails integrated the Casbin authencation system,and provides sqlalchemy adapter(default is file adapter)

* The Casbin Docs see [here](https://casbin.org/zh/docs/overview)

## Configure

* file in config/authencation.yaml auth section:

        auth:
            adapter_uri: './configs/casbin-adapter.csv'  ## configure adapter for sqlalchemy uri,default is same the app database 
            auth_model: ./configs/casbin-model.conf      ## configure casbin model file
            adapter_table: 'casbin_rule'                 ## configure for sqlalchemy adapter
            secret_key: '123456'                         ## encryption key for auth server
            casbin_adapter: file                         ## chooses is `file` `sqlalchemy` 
            session_name: user                           ## set cached key for user info in request.session
            type: jwt                                    ## auth type chooses `basic` and `jwt`

