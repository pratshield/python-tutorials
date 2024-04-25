## How does importing in Python work

Assume we have a directory named **dir**, inside which we have the Python script. When we import a module in this Python script, the Python interpreter tries to find the module in this order:

1. It searches among other Python scripts inside the **dir** directory
2. Then it goes over the list of the directories that are set using the **PYTHONPATH** environment variable.
3. Last, it searches through the default directories where Python files were installed. For example. *C:\\Users\\user\\AppData\\Local\\Programs\\Python\\Python312\\Lib*
