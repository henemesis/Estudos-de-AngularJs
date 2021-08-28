# Estudos-de-AngularJs
 Estudos de AngularJs para atualização de conhecimentos

## 1ª AULA  
### Conceitos básicos

>>angular.module("helloWord", []);  
> O **[ ]** indica a injeção, a importação de novos módulos, diretivas, services entre outros.  

>>Aqui criamos um módulo  
angular.module("helloWorld", []);

* **AngularJS** trabalha no modelo MVC  
  
* **Scope:** É uma ponte entre **View** e **Controller**, faz a "mediação" entre ambos
   
* Há um **two-way-databinding** entre a **View** e a **Controller**, intermediado pela **Scope**  
  
>> Aqui criamos um localizdor de um módulo
>> angular.module("helloWorld").controller("helloWorldCtrl", function (){ });