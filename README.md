
## Basic Requirements

* [Node](https://nodejs.org/en): version 6+
* [Yarn](https://yarnpkg.com/lang/en/): Manager package

</br></br>

## Conventions
Conventions and best practices using react.

* [Nomenclatures](#nomenclatures)
* [Folder](#folder)
* [Files](#files)
* [Files js. jsx](#filesjs)
* [Functions](#functions)
* [Autobinding](#autobinding)
* [Constants](#constants)
* [Comparator](#comparator)

</br></br>

### Nomenclatures
Definition of the nomenclatures of packages, classes, variables, constants, methods and others. As a general rule, no accent or special characters are allowed in names of any kind.
</br></br>
**_Use English for name definition, except for situations where there is no word in the language._**

</br></br>

### Folder
The folders must be created with lowercase letters and with camelCase. The words should be in the singular, according to the model below:

| Folder                        | Example                      |
|-------------------------------|------------------------------|
| menu with submenu list (Menu) | menu                         |
| submenu                       | menuSubmenu                  |
| list submenu                  | listSubmenu                  |


</br></br>

### Files

_Name:_
It should be simple and descriptive, allowing its easy association with context, except for files with restrictive names.
</br>
_Location:_
Must be located next to files of the same type, except in specific cases.

</br></br>

### FilesJs

_Name:_
Must follow Name + Type rule

</br>

| Component                     | Examples                     |
|-------------------------------|------------------------------|
| a modal component             | ModalComponent.js            |
| a edit container              | EditContainer.js             |


</br>

_Location:_
Must be located next to files of the same type.

</br></br>

### Functions

_Name:_
Must be simple and descriptive, follow Camel-case pattern.

</br></br>

### Autobinding

:warning: Use arrow functions instead of bind. 

:heavy_check_mark: correct:

```
class Comp extends Component {

    method = () => {
      console.log ('-')
    }
    
}
```
</br>

 :x: Incorrect:
 
```
class Comp extends Component {

    constructor (props) {
        super (props)   
        this.method = this.method.bind(this)
    }

    method () {
        console.log ('-')
    }
}
```

</br></br>

### Constants

Do not use comparison directly with numbers or strings use constant files for this.

Example:

> Constants.js

```
export default NUMBER_ONE = 1
```
</br>

> Component.js

```
import constants from 'folder/Constants'

class Comp extends Component {

    method = (value) => {
        if(value === constants.NUMBER_ONE){
            ...
        }
    }
}

```
</br></br>

### Comparator

:warning: When comparing use === (identical) and not == (equality).

</br>
[More...](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Equality_comparisons_and_sameness)

</br></br>
