
-----

> **Disciplina:** Linguagem e Técnicas de Programação    
> **Tema:** Manipulação de dados em Entrada e Saída  
> **Professor:** José Carlos Flores  
> **Curso:** Engenharia de Software  
> **Objetivo:** Manipulação de dados em Entrada e Saída(Conversão de tipos em PHP)

### **Lista de Exercícios: Conversão de tipos em PHP**

**Enunciado geral:** Para cada um dos problemas a seguir, analise o código PHP fornecido. Sua tarefa é determinar o **valor final** e o **tipo de dado** da variável `$resultado`. Utilize as funções `var_dump($resultado);` ou `echo gettype($resultado);` e `echo $resultado;` para verificar suas respostas.

-----

**Exercícios:**

1.  **Problema:** Um sistema precisa somar a quantidade inicial de produtos, que é uma string, com a quantidade que acabou de chegar. Qual o resultado da operação?

    ```php
    $quantidade_inicial = "150";
    $chegaram = 50;
    $resultado = $quantidade_inicial + $chegaram;
    ```

2.  **Problema:** É necessário criar um código de produto concatenando um prefixo numérico com um sufixo. Como o PHP se comportará?

    ```php
    $prefixo = 1000;
    $sufixo = "-A";
    $resultado = $prefixo . $sufixo;
    ```

3.  **Problema:** Ao calcular a média de duas notas, uma delas foi inserida como texto. Qual será a média final calculada?

    ```php
    $nota1 = 8;
    $nota2 = "7.5";
    $resultado = ($nota1 + $nota2) / 2;
    ```

4.  **Problema:** Um script precisa verificar se uma variável de texto, que contém um valor numérico, é verdadeira. Qual será o resultado booleano?

    ```php
    $valor_texto = "25";
    $resultado = (bool) $valor_texto;
    ```

5.  **Problema:** Em uma verificação de permissão, um valor `0` (inteiro) é avaliado em um `if`. Qual será o resultado da conversão explícita para booleano?

    ```php
    $permissao_nivel = 0;
    $resultado = (bool) $permissao_nivel;
    ```

6.  **Problema:** Um valor de preço é recebido de uma API como string. Precisamos convertê-lo para inteiro, ignorando os centavos. Qual será o valor final?

    ```php
    $preco_api = "199.99";
    $resultado = (int) $preco_api;
    ```

7.  **Problema:** Uma string contém um número seguido por texto. Como o PHP a converte para um número de ponto flutuante?

    ```php
    $medida = "12.5cm";
    $resultado = (float) $medida;
    ```

8.  **Problema:** Uma string começa com texto, mas contém um número. O que acontece ao tentar somá-la a um inteiro?

    ```php
    $estoque_texto = "Temos 100 unidades";
    $adicao = 25;
    $resultado = $estoque_texto + $adicao;
    ```

9.  **Problema:** Uma variável `null` é usada em um cálculo matemático. Qual valor ela assume ao ser convertida para inteiro?

    ```php
    $valor_desconhecido = null;
    $resultado = (int) $valor_desconhecido;
    ```

10. **Problema:** O booleano `false` é convertido para uma string. Qual será o conteúdo dessa string?

    ```php
    $status_ativo = false;
    $resultado = (string) $status_ativo;
    ```

11. **Problema:** Um array é acidentalmente concatenado com uma string. Qual será o resultado dessa operação?

    ```php
    $dados = [1, 2, 3];
    $resultado = "Os dados são: " . $dados;
    ```

12. **Problema:** O que acontece quando o valor booleano `true` é somado com um número inteiro?

    ```php
    $incremento = true;
    $valor_base = 10;
    $resultado = $valor_base + $incremento;
    ```

13. **Problema:** Uma string contendo apenas "0" é verificada em um contexto booleano. Qual é o resultado?

    ```php
    $input_usuario = "0";
    $resultado = (bool) $input_usuario;
    ```

14. **Problema:** Um número octal (representado por um `0` no início em algumas contextos) em uma string é convertido para inteiro usando `intval`. Qual será o resultado?

    ```php
    $codigo_octal = "077";
    $resultado = intval($codigo_octal);
    ```

15. **Problema:** Um número em ponto flutuante é dividido por um inteiro, e o resultado é convertido para inteiro. Qual o valor final?

    ```php
    $total = 10.0;
    $parcelas = 3;
    $resultado = (int) ($total / $parcelas);
    ```

16. **Problema:** Uma string vazia (`""`) é comparada com o inteiro `0` usando o operador de igualdade `==`. A comparação é verdadeira ou falsa?

    ```php
    $string_vazia = "";
    $numero_zero = 0;
    $resultado = ($string_vazia == $numero_zero);
    ```

17. **Problema:** Diferente da anterior, agora compare uma string vazia (`""`) com `null` usando o operador `==`. Qual o resultado?

    ```php
    $string_vazia = "";
    $nulo = null;
    $resultado = ($string_vazia == $nulo);
    ```

18. **Problema:** O que acontece ao somar um array com um número inteiro?

    ```php
    $config = ['timeout' => 100];
    $ajuste = 50;
    $resultado = $config + $ajuste;
    ```

    *(Nota: Esta operação gerará um erro. O exercício visa identificar o erro.)*

19. **Problema:** Use a função `settype` para modificar uma variável de string para float. Qual será o novo valor e tipo da variável?

    ```php
    $distancia = "98.7 km";
    settype($distancia, "float");
    $resultado = $distancia;
    ```

20. **Problema:** Uma string representando um número em notação científica é usada em uma soma. Qual o resultado?

    ```php
    $valor_grande = "2e3"; // 2 * 10^3
    $resultado = $valor_grande + 100;
    ```

21. **Problema:** Converta um número negativo para booleano. Qual será o resultado?

    ```php
    $saldo_devedor = -500;
    $resultado = (bool) $saldo_devedor;
    ```

22. **Problema:** Combine múltiplas conversões: um booleano é somado com um float contido em uma string.

    ```php
    $resultado = true + "9.5";
    ```

23. **Problema:** Um valor `float` muito pequeno é convertido para `int`. Qual o resultado?

    ```php
    $fração = 0.999;
    $resultado = (int) $fração;
    ```

24. **Problema:** A string `"false"` (a palavra em si) é convertida para booleano. Qual o resultado?

    ```php
    $texto_flag = "false";
    $resultado = (bool) $texto_flag;
    ```

25. **Problema:** Use `strval()` para converter um valor nulo. Qual será o resultado?

    ```php
    $sem_valor = null;
    $resultado = strval($sem_valor);
    ```

26. **Problema:** Um número hexadecimal em uma string é convertido para inteiro usando `intval` com a base correta.

    ```php
    $cor_hex = "FF";
    $resultado = intval($cor_hex, 16);
    ```

27. **Problema:** Duas strings que parecem números são comparadas com o operador de igualdade `==`. O resultado é `true` ou `false`?

    ```php
    $str_num1 = "100";
    $str_num2 = "1e2";
    $resultado = ($str_num1 == $str_num2);
    ```

28. **Problema:** Uma variável é definida como uma string vazia e depois seu tipo é alterado para `integer` com `settype`. Qual será seu valor?

    ```php
    $dado = "";
    settype($dado, "integer");
    $resultado = $dado;
    ```

29. **Problema:** Some um inteiro com um valor booleano `false`. Qual será o resultado final?

    ```php
    $pontos = 10;
    $bonus = false;
    $resultado = $pontos + $bonus;
    ```

30. **Problema:** Compare a string `"1"` com o booleano `true` usando o operador de identidade `===`. O resultado é `true` ou `false`?

    ```php
    $texto_um = "1";
    $booleano_verdadeiro = true;
    $resultado = ($texto_um === $booleano_verdadeiro);
    ```

-----
## 👤 GitHub

[![Foto de Perfil](https://github.com/floresjcd.png?size=50)](https://github.com/floresjcd) 
**[@floresjcd](https://github.com/floresjcd)**

-----
