# 0.4

```marmaid
//sequenceDiagram

participant browser
participant server
participant User
participant JavaScript

//assuming the page is already open and running
User->>browser: write something into the text field (whatever)
User->>browser: clicking the Save button
browser->>JavaScript: list = document.getElementsByTagName('ul')[0]
JavaScript->>server: send the list elements to server
server->>server: processing
browser->>JavaScript: newElement = document.createElement('li')
browser->>JavaScript: newElement.textContent = (whatever)
JavaScript->>browser: list.appendChild(newElement)
// should commit first or changes will disappear if refresh the page
browser->>User: Exibir Lista Atualizada
````


