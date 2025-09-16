> **Disciplina:** Linguagem e Técnicas de Programação    
> **Tema:** Conceitos de Variáveis de Entrada e Saída em PHP    
> **Professor:** José Carlos Flores  
> **Curso:** Engenharia de Software  
> **Objetivo:** Análise do Sistema de Login vide: https://github.com/floresjcd/Esoft_2025/tree/b56e9139b5d4e234bb21c373d147b3df7b1c00cf/1oBI/Aula-9/session


# ✅ **GABARITO COMPLETO**

---

## 🟩 **Parte 1: Gabarito Objetivo**

| Questão | Resposta | Explicação |
|--------|---------|-----------|
| 1 | B | `session_start()` inicia ou retoma uma sessão ativa |
| 2 | C | `$_SESSION` armazena dados no servidor |
| 3 | D | `valida.php` processa o login |
| 4 | D | POST é mais seguro para senhas |
| 5 | B | `header('Location')` redireciona o usuário |
| 6 | B | Erro comum: saída antes de `session_start()` |
| 7 | D | `$_SESSION` é a superglobal de sessões |
| 8 | B | Verifica se `$_SESSION['logado']` é true |
| 9 | A | Caminho relativo correto |
| 10 | A | `session_destroy()` apaga todos os dados da sessão |
| 11 | B | Evita injeção de scripts (XSS) |
| 12 | C | `<link rel="stylesheet" href="...">` |
| 13 | B | Método HTTP não permitido (ex: POST em página estática) |
| 14 | B | Apache só serve arquivos em `htdocs` |
| 15 | B | Evita que código posterior seja executado |
| 16 | C | `??` é o operador de coalescência nula |
| 17 | C | Define como `true` após login bem-sucedido |
| 18 | C | `login.html` é HTML puro |
| 19 | B | `session_destroy()` encerra a sessão |
| 20 | E | Porta 443 é a padrão do HTTPS |

---

## 🟩 **Parte 2: Gabarito Discursivo**

**21.**  
`$_SESSION` é mais seguro porque os dados são armazenados no **servidor**, enquanto `$_COOKIE` é armazenado no **navegador do cliente**, podendo ser alterado ou visualizado.

**22.**  
`$_REQUEST` pode misturar dados de `GET`, `POST` e `COOKIE`, o que **compromete a segurança** e pode causar conflitos. É melhor especificar a origem dos dados.

**23.**  
Separação de camadas divide o sistema em:  
- **Estrutura (HTML)**  
- **Estilo (CSS)**  
- **Lógica (PHP)**  
Isso melhora manutenção, legibilidade e reutilização.

**24.**  
`echo` é mais rápido, pode imprimir múltiplos valores com vírgula e não retorna nada. `print` sempre retorna `1` e só imprime um valor por vez.

**25.**  
Organiza os arquivos, facilita a manutenção e permite reutilização em múltiplas páginas. Também segue boas práticas de estrutura de projetos.

**26.**  
Criar um array de usuários e senhas, e verificar se o par informado está presente:
```php
$usuarios = [
    'admin' => '12345',
    'usuario' => 'senha123'
];
if (isset($usuarios[$usuario]) && $usuarios[$usuario] === $senha) { ... }
```

**27.**  
O `header('Location: ...')` redireciona o usuário para outra página após uma ação (login, logout), mantendo o fluxo do sistema.

**28.**  
`session_start()` é necessário para acessar os dados da sessão. Sem ele, `$_SESSION` não estará disponível.

**29.**  
- Uso de `htmlspecialchars()` para evitar XSS  
- Verificação de `$_SESSION['logado']` antes de acessar páginas protegidas

**30.**  
Exemplos de melhorias:  
- Adicionar campo de "nível" (admin/usuario) e exibir conteúdo diferente  
- Validar e-mail no login  
- Mostrar data e hora do último acesso  
- Criar um sistema de tentativas de login

---
