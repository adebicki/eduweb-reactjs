###### Install http server - https://www.npmjs.com/package/http-server

npm install http-server -g

# React DOM

var h3 = React.createElement('h3', {}, 'Header created with React');

To polecenie nie tworzy elementu DOM, tylko element Virtual DOM, który jest znacznie
mniejszy od elementu DOM (mniej właściwości), a więc szybciej się go tworzy.

ReactDOM umożliwia przetworzenie tego obiektu na DOM:

ReactDOM.render(h3, document.getElementById('root'));

###### Utworzenie elementu z wieloma węzłami potomnymi:

var div  = React.createElement('div', {}, React.createElement('h3', {}, 'Header h3'), React.createElement('p', {}, 'paragraf'));

ReactDOM.render(div, document.getElementById('root'));

Jeśli zrobimy to samo jeszcze raz, ale zmienimy coś, to ReactDOM.render sam rozpozna co się
zmieniło i tylko to podmieni w DOM

var div  = React.createElement('div', {}, React.createElement('h3', {}, 'Header h3'), React.createElement('p', {}, 'paragraf v2'));
ReactDOM.render(div, document.getElementById('root'));

###### Dynamiczne style i animacje

style musi być przekazany jako obiekt klucz-wartość

Deklarujemy element raz (React.createElement(..., {}, children...)) uzależniając go od zmiennych, potem zmieniamy tylko
wartości tych zmiennych. Ważne, żeby deklaracja była w funkcji, ( function course() {return React.createElement(...)} ),
żeby można było odświeżać w ogóle po zmianie zmiennych ( ReactDOM.render(course(), document.getElementById('root')); )

###### Dynamiczna treść
Dane możemy mieć skądkolwiek, potem tylko w szablonie dajemy np.
React.createElement('img', {src: data.image}),


next:
https://eduweb.pl/player/reactjs-w-praktyce/dynamiczne-ukrywanie-elementow

