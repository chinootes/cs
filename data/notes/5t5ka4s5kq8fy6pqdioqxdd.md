
Static variables are not garbage collected until class is loaded in the memory.

Static variables are referenced by Class objects (❗not class objects) which are referenced by ClassLoaders. So static variables can't be elected for garbage collection while the class is loaded. They can be collected when the respective class loader is itself collected.