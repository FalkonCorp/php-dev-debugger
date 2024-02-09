# F4LK0N
(PHP Composer Source Repository)
Useful functions to debug server behavior, and provide a formated and structurated response.

## VDD
F4lk0n VarDump functions to help visualize variable contents.
Useful when, for some reason you don't have XDebug installed on the server and
need to perform a quick analisys of the variables contents.

### Content

#### Features:
- Indicate variables types;
- Indicate file and line of the caller; (When available at the server);
- HTML formated output;
- Stylized output;
- Short name for easy typing while developing;

#### To Do (Future):
- Avoid circular reference;
- Customize output style;

### Install
With compose add it to the required depencies:
```json
  "require": {
    "f4lk0n/vdd": "*"
  },
```
Manually, require all files or just the desired ones from the `src/` folder:
```php
<?php
  require "src/VDD.php";
```

### Usage
Call the VD function passing the desired var, to print and continue;
Call the VDD function, if you wanna print and stop execution.
```php
<?php
  VD($someVarA);  //VarDump contents;
  VD($someVarB);  //VarDump contents;
  VD($someVarC);  //VarDump contents;
  VDD($someVarD); //VarDump contents and die;
  someFunction(); //Not called;
```
