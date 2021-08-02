# .editorconfig not working with VSCode

open `Class1.cs` and `Ctrl + .` on `myField`

You should see the option for `Create and assign field for myField` 

Expected outcome with the current editorconfig file would be

```c#
 public class Class1
    {
        private readonly string _myfield;

        public Class1(string myfield) {
            _myfield = myfield;
        }
    }
```

actual output

```c#
    public class Class1
    {
        private readonly string myfield;

        public Class1(string myfield) {
            this.myfield = myfield;
        }
    }
```

