# Estudos-de-AngularJs  
**** 
CURSO PROF. RODRIGO BRANAS  
****  

 ### Estudos de AngularJs para atualização de conhecimentos

## 1ª AULA: AngularJS #1 - Introdução e Hello World
### Conceitos básicos  
  
> O **[ ]** indica a injeção, a importação de novos módulos, diretivas, services entre outros:  

~~~angular.js
angular.module("helloWord", []);  
~~~
  
>Aqui criamos um módulo:  

~~~angular.js
angular.module("helloWorld", []);
~~~  

* **AngularJS** trabalha no modelo MVC  
  
* **Scope:** É uma ponte entre **View** e **Controller**, faz a "mediação" entre ambos
   
* Há um **two-way-databinding** entre a **View** e a **Controller**, intermediado pela **Scope**  
  
> Aqui criamos um localizdor de um módulo:

~~~angular.js
angular.module("helloWorld").controller("helloWorldCtrl", function (){ });
~~~  

## 2ª AULA: AngularJS #2 - Usando Diretivas - Parte 1  
### Conceitos    

* __Diretivas:__ Extensões da linguagem HTML que permitem novos comportamentos, sendo implementados sobre uma nova forma declarativa.  
  
> __ngApp__ --> Define as fronteiras da aplicação, buscando todos os comportamentos descritos pelo scripts encontrados no arquivo html. Exemplo:  

~~~angular.js
ng-app="listaTelefonica"
~~~
  
>__ngController__ --> Cria vínculo entre um elemento da View com um elemento da Controller (o sistema de **rotiamento** também permite fazer tal vínculos). Exemplo:  
~~~angular.js
`ng-controller="listaTelefonicaCtrl"`  
~~~  

>__ngBind__ --> Substitui um termo por uma expressão. Exemplo:  

~~~angular.js
ng-bind="app"  
~~~  

>__ngRpeat__ --> Permite iterar sobre os elementos de uma lista, de um array, de uma coleção de objetos.Exemplo:  

~~~angular.js
ng-repeat="contanto in contatos"`  
~~~
  
>Utilizando ng-repeat com CHAVE  E VALOR:  
~~~html
<td ng-repeat="(key, value) in contato">
    {{value}}
</td>
~~~  

>__ngModel__ --> Faz o inverso do **ngBind**, ou seja, ele pega algo da **View** (da "página") e define no **Scope**. Elementos em que se aplica ngModel:  
>* Selects;  
>* Inputs;  
>* Text Areas.  

~~~html
<input class="form-control" type="text" ng-model="nome"/>
~~~  

>__ngClick__ --> Atribui comportamento ao evento. Exemplo:  
> 
~~~angular.js
<button class="btn btn-primary btn-block" ng-click="adicionarContato(contato)">Adicionar Contato</button>
~~~  

Quando estivermos dentro da **controller** será necessário evitar a leitura do **$scope**. Exemplo:  
~~~Js
{nome: $scope.nome, telefone: $scope.telefone}
~~~
