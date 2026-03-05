### MatchTheRegex

### Descripción

How about trying to match a regular expressionThe website is running [here](http://saturn.picoctf.net:49217/).
### Solución

### Solucion 1

- Si entramos al codigo fuente de la pagina nos damos cuenta de esto 
|function send_request() {|
|let val = document.getElementById("name").value;|
|// ^p.....F!?|

- lo que quiere decir que tenemos 5 caracteres entre p y la F, cualesquiera y si lo ponemos nos debe de dar la bandera.
- ponemos en value p12345F y le damos enter

picoCTF{succ3ssfully_matchtheregex_c64c9546}
### Notas
- Las expresiones regulares son patrones que se utilizan para hacer coincidir combinaciones de caracteres en cadenas.
### Referencias
- https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Regular_expressions
- https://regexr.com/