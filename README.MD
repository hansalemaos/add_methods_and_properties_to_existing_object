# Add methods and properties to an existing object


```python
$pip install add-methods-and-properties-to-existing-object
from add_methods_and_properties_to_existing_object import AddMethodsAndProperties

class NewClass(AddMethodsAndProperties): #inherit from AddMethodsAndProperties to add the method add_methods
    def __init__(self):
        self.bubu = 5

    def _delete_files(self, file): #some random methods 
        print(f"File will be deleted: {file}")

    def delete_files(self, file):
        self._delete_files(file)

    def _copy_files(self, file, dst):
        print(f"File will be copied: {file} Dest: {dst}")

    def copy_files(self, file, dst):
        self._copy_files(file, dst)

    def _create_files(self, file, folder):
        print(f"File will be created: {file} {folder}")

    def create_files(self, file, folder):
        self._create_files(file, folder)

    def method_with_more_kwargs(self, file, folder, one_more):
        print(file, folder, one_more)
        return self


nc = NewClass()
dict_all_files = {
    r"C:\Windows\notepad.exe_delete": {
        "function": "delete_files",
        "args": (),
        "kwargs": {"file": r"C:\Windows\notepad.exe"},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_argsfirst": {
        "function": "delete_files",
        "args": (),
        "kwargs": {"file": r"C:\Windows\notepad.exe"},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_copy": {
        "function": "copy_files",
        "args": (),
        "kwargs": {
            "file": r"C:\Windows\notepad.exe",
            "dst": r"C:\Windows\notepad555.exe",
        },
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_create": {
        "function": "create_files",
        "args": (),
        "kwargs": {"file": r"C:\Windows\notepad.exe", "folder": "c:\\windows95"},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_upper": {
        "function": str.upper,
        "args": (r"C:\Windows\notepad.exe",),
        "kwargs": {},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_method_with_more_kwargs": {
        "function": "method_with_more_kwargs",
        "args": (),
        "kwargs": {"file": r"C:\Windows\notepad.exe", "folder": "c:\\windows95"},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_method_with_more_kwargs_as_args_first": {
        "function": "method_with_more_kwargs",
        "args": (r"C:\Windows\notepad.exe", "c:\\windows95"),
        "kwargs": {},
        "this_args_first": True,
    },
    r"C:\Windows\notepad.exe_method_with_more_kwargs_as_args_last": {
        "function": "method_with_more_kwargs",
        "args": (r"C:\Windows\notepad.exe", "c:\\windows95"),
        "kwargs": {},
        "this_args_first": False,
    },
    "this_is_a_list": [55, 3, 3, 1, 4, 43],
}

nc.add_methods(dict_all_files)


print(nc.C_Windows_notepad_exe_delete)
print(nc.C_Windows_notepad_exe_delete(), end="\n\n")
print(nc.C_Windows_notepad_exe_argsfirst)
print(nc.C_Windows_notepad_exe_argsfirst(), end="\n\n")
print(nc.C_Windows_notepad_exe_copy)
print(nc.C_Windows_notepad_exe_copy(), end="\n\n")
print(nc.C_Windows_notepad_exe_create)
print(nc.C_Windows_notepad_exe_create(), end="\n\n")
print(nc.C_Windows_notepad_exe_upper)
print(nc.C_Windows_notepad_exe_upper(), end="\n\n")
print(nc.C_Windows_notepad_exe_method_with_more_kwargs)
print(
    nc.C_Windows_notepad_exe_method_with_more_kwargs(
        one_more="f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs(
        one_more="f:\\ASJVASDFAS??DFJAS??DJF??ASWFJAS??"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs(
        one_more="f:\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    ),
    end="\n\n",
)
print(nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_first)
print(
    nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_first(
        "f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    ),
    end="\n\n",
)
print(
    nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_first(
        "f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_first(
        "f:\\ASJVASDFAS??DFJAS??DJF??ASWFJAS??"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_first(
        "f:\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    ),
    end="\n\n",
)
print(nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_last)
print(
    nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\ASJVASDFAS??DFJAS??DJF??ASWFJAS??"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    ),
    end="\n\n",
)
print(
    nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\ASJVASDFAS??DFJAS??DJF??ASWFJAS??"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    ),
    end="\n\n",
)
print(nc.this_is_a_list)
checkit = (
    nc.C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\blaaaaaaaaaaaaaaaaaaaaaaaa"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\ASJVASDFAS??DFJAS??DJF??ASWFJAS??"
    )
    .C_Windows_notepad_exe_method_with_more_kwargs_as_args_last(
        "f:\\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    )
)
print(f'nc is checkit? -> {nc is checkit}')


#output:


NewClass.delete_files(self, file='C:\\Windows\\notepad.exe')
File will be deleted: C:\Windows\notepad.exe
None


NewClass.delete_files(self, file='C:\\Windows\\notepad.exe')
File will be deleted: C:\Windows\notepad.exe
None


NewClass.copy_files(self, file='C:\\Windows\\notepad.exe', dst='C:\\Windows\\notepad555.exe')
File will be copied: C:\Windows\notepad.exe Dest: C:\Windows\notepad555.exe
None


NewClass.create_files(self, file='C:\\Windows\\notepad.exe', folder='c:\\windows95')
File will be created: C:\Windows\notepad.exe c:\windows95
None


NewClass.upper(self, 'C:\\Windows\\notepad.exe')
C:\WINDOWS\NOTEPAD.EXE


NewClass.method_with_more_kwargs(self, file='C:\\Windows\\notepad.exe', folder='c:\\windows95')
C:\Windows\notepad.exe c:\windows95 f:\blaaaaaaaaaaaaaaaaaaaaaaaa
C:\Windows\notepad.exe c:\windows95 f:\ASJVASDFAS??DFJAS??DJF??ASWFJAS??
C:\Windows\notepad.exe c:\windows95 f:\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
<__main__.NewClass object at 0x0000000005F199A0>


NewClass.method_with_more_kwargs(self, 'C:\\Windows\\notepad.exe', 'c:\\windows95')
C:\Windows\notepad.exe c:\windows95 f:\blaaaaaaaaaaaaaaaaaaaaaaaa
<__main__.NewClass object at 0x0000000005F199A0>


C:\Windows\notepad.exe c:\windows95 f:\blaaaaaaaaaaaaaaaaaaaaaaaa
C:\Windows\notepad.exe c:\windows95 f:\ASJVASDFAS??DFJAS??DJF??ASWFJAS??
C:\Windows\notepad.exe c:\windows95 f:\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
<__main__.NewClass object at 0x0000000005F199A0>


NewClass.method_with_more_kwargs(self, 'C:\\Windows\\notepad.exe', 'c:\\windows95')
f:\blaaaaaaaaaaaaaaaaaaaaaaaa C:\Windows\notepad.exe c:\windows95
f:\ASJVASDFAS??DFJAS??DJF??ASWFJAS?? C:\Windows\notepad.exe c:\windows95
f:\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX C:\Windows\notepad.exe c:\windows95
<__main__.NewClass object at 0x0000000005F199A0>


f:\blaaaaaaaaaaaaaaaaaaaaaaaa C:\Windows\notepad.exe c:\windows95
f:\ASJVASDFAS??DFJAS??DJF??ASWFJAS?? C:\Windows\notepad.exe c:\windows95
f:\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX C:\Windows\notepad.exe c:\windows95
<__main__.NewClass object at 0x0000000005F199A0>


[55, 3, 3, 1, 4, 43]


f:\blaaaaaaaaaaaaaaaaaaaaaaaa C:\Windows\notepad.exe c:\windows95
f:\ASJVASDFAS??DFJAS??DJF??ASWFJAS?? C:\Windows\notepad.exe c:\windows95
f:\XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX C:\Windows\notepad.exe c:\windows95


nc is checkit? -> True


```