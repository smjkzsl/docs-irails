# Services

* The design concept of service is mainly to decouple controller and models. Service includes data validation, database addition, deletion, modification, query, etc. The business logic, data processing, etc. in the application can be referenced separately from the controller.

* The service module is always located in the services folder under the app application directory, and will be automatically imported when the application is imported. The namespace is {app name}. services
## Defintion

        from irails.database import Service
        from app.models import User
        class user_service(Service):
            def get(self,id):
                with self.get_session() as session:
                    return session.select(User).query(User.c.id==id)
            def add(self,user:User):
                pass
            def delete(self,user:User):
                pass
            def update(self,user:User):
                pass