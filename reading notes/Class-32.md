# DRF Permissions
## why this topic matters as it relates to what you are studying in this module ?
REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.

<br>

## Django Rest Framework (DRF) provides a powerful and flexible toolkit for building Web APIs in Django. One of the essential features of DRF is its built-in permissions system, which helps in securing APIs by controlling access to resources based on certain rules. The key components and purpose of DRF permissions are as follows:

Permission Classes: DRF defines a set of permission classes that determine whether a user has permission to perform a certain action on a particular resource. These classes are responsible for enforcing authorization rules. The permission classes provided by DRF include:

AllowAny: This class allows unrestricted access to all users, both authenticated and unauthenticated.
IsAuthenticated: Only authenticated users are granted access.
IsAdminUser: Only users with the is_staff flag set to True (typically superusers or staff members) are granted access.
IsAuthenticatedOrReadOnly: Unauthenticated users have read-only access, while authenticated users have full access.
DjangoModelPermissions: Permissions are determined based on the Django model-level permissions (i.e., add, change, delete) granted to the user.
DjangoObjectPermissions: Permissions are determined based on the Django model-level and object-level permissions.
Permission Evaluation: When a request is made to an API view, DRF applies the specified permission classes in a sequential manner. The permissions are evaluated from left to right, and the first permission class that denies access immediately interrupts the evaluation and denies permission. If all permission classes allow access, the permission is granted.

Permission Customization: DRF allows you to create custom permission classes to implement your own authorization logic. You can subclass existing permission classes or create entirely new ones to fit your specific requirements. This customization allows fine-grained control over access to resources based on various conditions, such as user roles, group membership, ownership, or any other custom logic.

By utilizing DRF permissions, you can enforce access control policies and secure your API endpoints. These permissions help in preventing unauthorized access to sensitive data or actions. You can restrict certain actions to authenticated users only, limit access based on user roles, or even implement complex authorization rules using custom permission classes. DRF permissions work hand-in-hand with Django's authentication system to ensure that API resources are accessed only by authorized users, enhancing the security of your application.

<br>

# Review SQL Prework
## In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?
In SQL, the SELECT statement is used to query and retrieve data from a database. Its primary purpose is to specify the columns and records that should be returned as a result of the query.

To retrieve all columns from a table called 'employees' using the SELECT statement, you can use the following query:

    SELECT * FROM employees;

In this query:

SELECT specifies that we want to retrieve data.
is a wildcard symbol that represents all columns in the specified table.
FROM indicates the table from which we want to retrieve data.
employees is the name of the table from which we want to retrieve all columns.
Executing this query will return all the columns from the 'employees' table, including all the records (rows) present in the table. The result will be a result set containing the data from all columns for each row in the 'employees' table.

<br>

## Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?
DRF (Django Rest Framework) provides a set of powerful and reusable views called Generic Views that simplify the process of building RESTful APIs. Generic Views abstract common functionalities and provide pre-implemented behaviors for common operations, reducing the amount of code needed.

The role of DRF Generic Views is to handle common API operations, such as retrieving a list of objects, retrieving a single object, creating an object, updating an object, and deleting an object. They encapsulate common patterns and provide a consistent interface for working with different types of resources.

Here are some examples of DRF Generic Views and their usage in building a RESTful API:

APIView: This is the most basic generic view, providing the foundation for all other generic views. You can subclass APIView to create custom views with custom logic for handling HTTP methods.

    from rest_framework.views import APIView
    from rest_framework.response import Response

    class MyAPIView(APIView):
        def get(self, request, format=None):
            # Custom logic for handling GET request
            data = {'message': 'Hello, World!'}
            return Response(data)

ListAPIView: This view retrieves a list of objects from a model and serializes them for the response.

    from rest_framework.generics import ListAPIView
    from .models import Employee
    from .serializers import EmployeeSerializer

    class EmployeeListView(ListAPIView):
        queryset = Employee.objects.all()
        serializer_class = EmployeeSerializer

RetrieveAPIView: This view retrieves a single object from a model based on its identifier (primary key).

    from rest_framework.generics import RetrieveAPIView
    from .models import Employee
    from .serializers import EmployeeSerializer

    class EmployeeDetailView(RetrieveAPIView):
        queryset = Employee.objects.all()
        serializer_class = EmployeeSerializer

CreateAPIView: This view handles the creation of a new object using POST requests.

    from rest_framework.generics import CreateAPIView
    from .serializers import EmployeeSerializer

    class EmployeeCreateView(CreateAPIView):
        serializer_class = EmployeeSerializer

UpdateAPIView and DestroyAPIView: These views handle updating and deleting objects respectively, using PUT, PATCH, and DELETE requests.

    from rest_framework.generics import UpdateAPIView, DestroyAPIView
    from .models import Employee
    from .serializers import EmployeeSerializer

    class EmployeeUpdateView(UpdateAPIView):
        queryset = Employee.objects.all()
        serializer_class = EmployeeSerializer

    class EmployeeDeleteView(DestroyAPIView):
        queryset = Employee.objects.all()
        serializer_class = EmployeeSerializer

By utilizing DRF Generic Views, you can quickly create API views with pre-implemented behaviors for common operations, reducing the amount of boilerplate code needed. These views promote code reusability and follow RESTful design principles, allowing you to build robust and maintainable APIs efficiently.

<br>

## Things I want to know more about :
Nothing for now .
