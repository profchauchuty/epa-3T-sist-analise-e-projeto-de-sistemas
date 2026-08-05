# Teste de Mesa

## 1. Conceito
- Técnica utilizada para **simular manualmente a execução de um algoritmo**
- Permite acompanhar o comportamento das variáveis passo a passo
- Ajuda a identificar erros de lógica antes da execução do programa
- Consiste em registrar os valores das variáveis em uma tabela durante cada etapa do algoritmo
- É uma das ferramentas mais importantes para aprender programação e depurar códigos

---

## 2. Estrutura Básica
- O teste de mesa é realizado acompanhando a execução linha por linha do algoritmo
- A cada instrução executada, os valores das variáveis devem ser atualizados na tabela

```text
Passo | Instrução Executada | Variável 1 | Variável 2 | Resultado
```

### Exemplo Simples

```portugol
programa
{
    funcao inicio()
    {
        inteiro x
        
        x = 5
        x = x + 3
        
        escreva(x)
    }
}
```

### Teste de Mesa

| Passo | Instrução | x |
|--------|------------|---|
| 1 | Declaração de x | - |
| 2 | x = 5 | 5 |
| 3 | x = x + 3 | 8 |
| 4 | escreva(x) | 8 |

**Saída:** `8`

---

## 3. Acompanhamento de Variáveis

### O que é?
- Processo de observar como os valores armazenados nas variáveis mudam durante a execução do algoritmo
- Cada operação pode alterar um ou mais valores
- O teste de mesa permite visualizar essas alterações de forma organizada

### Exemplo

```portugol
programa
{
    funcao inicio()
    {
        inteiro a, b
        
        a = 10
        b = 4
        
        a = a + b
        
        escreva(a)
    }
}
```

### Teste de Mesa

| Passo | a | b |
|--------|---|---|
| Inicial | - | - |
| a = 10 | 10 | - |
| b = 4 | 10 | 4 |
| a = a + b | 14 | 4 |

**Saída:** `14`

---

## 4. Teste de Mesa com Estrutura de Decisão

### O que é?
- Utilizado para verificar qual caminho será executado dentro de um bloco `se`
- É importante analisar a condição lógica antes de determinar o resultado

### Exemplo

```portugol
programa
{
    funcao inicio()
    {
        inteiro idade
        
        idade = 18
        
        se(idade >= 18){
            escreva("Maior de idade")
        }
        senao{
            escreva("Menor de idade")
        }
    }
}
```

### Teste de Mesa

| Passo | idade | Condição (idade >= 18) |
|--------|--------|----------------------|
| idade = 18 | 18 | - |
| Verificação | 18 | Verdadeiro |

**Saída:** `Maior de idade`

---

## 5. Teste de Mesa com Estrutura de Repetição

### O que é?
- Permite acompanhar cada repetição de um laço
- Muito utilizado para identificar erros em contadores e acumuladores

### Exemplo

```portugol
programa
{
    funcao inicio()
    {
        inteiro soma = 0
        
        para(inteiro i = 1; i <= 3; i++)
        {
            soma = soma + i
        }
        
        escreva(soma)
    }
}
```

### Teste de Mesa

| Iteração | i | soma |
|-----------|---|------|
| Inicial | - | 0 |
| 1ª | 1 | 1 |
| 2ª | 2 | 3 |
| 3ª | 3 | 6 |

**Saída:** `6`

---

## 6. Contadores e Acumuladores

### Contador
- Variável utilizada para contar quantas vezes um evento acontece
- Geralmente aumenta de 1 em 1

```portugol
contador = contador + 1
```

### Acumulador
- Variável utilizada para armazenar somas sucessivas
- Recebe novos valores durante a execução

```portugol
soma = soma + numero
```

### Exemplo

```portugol
programa
{
    funcao inicio()
    {
        inteiro contador = 0
        inteiro soma = 0
        
        para(inteiro i = 1; i <= 4; i++)
        {
            contador++
            soma = soma + i
        }
        
        escreva(contador)
        escreva(soma)
    }
}
```

### Teste de Mesa

| Iteração | i | contador | soma |
|-----------|---|-----------|------|
| Inicial | - | 0 | 0 |
| 1ª | 1 | 1 | 1 |
| 2ª | 2 | 2 | 3 |
| 3ª | 3 | 3 | 6 |
| 4ª | 4 | 4 | 10 |

---

## 7. Exemplo Completo

```portugol
programa
{
    funcao inicio()
    {
        inteiro numero
        inteiro dobro
        
        numero = 5
        dobro = numero * 2
        
        se(dobro > 8)
        {
            escreva("Maior que 8")
        }
        senao
        {
            escreva("Menor ou igual a 8")
        }
    }
}
```

### Teste de Mesa

| Passo | numero | dobro | Condição (dobro > 8) |
|--------|---------|--------|---------------------|
| Inicial | - | - | - |
| numero = 5 | 5 | - | - |
| dobro = numero * 2 | 5 | 10 | - |
| Verificação | 5 | 10 | Verdadeiro |

**Saída:** `Maior que 8`

---

## 8. Vantagens do Teste de Mesa

| Vantagem | Descrição |
|-----------|-----------|
| Identificação de Erros | Permite encontrar erros de lógica antes da execução |
| Aprendizagem | Facilita a compreensão do funcionamento dos algoritmos |
| Depuração | Auxilia na correção de programas |
| Organização | Mostra claramente a evolução das variáveis |
| Economia de Tempo | Evita várias tentativas de execução incorreta |

---

## 9. Boas Práticas
- Registrar todas as variáveis importantes na tabela
- Atualizar os valores após cada instrução executada
- Não pular etapas do algoritmo
- Verificar cuidadosamente condições de decisão (`se`)
- Em laços de repetição, registrar cada iteração separadamente
- Destacar a saída final produzida pelo programa

---

## 10. Exercícios

1. Realize o teste de mesa do algoritmo abaixo:

```portugol
inteiro x

x = 4
x = x + 2

escreva(x)
```

2. Faça o teste de mesa do código abaixo:

```portugol
inteiro a = 3
inteiro b = 7

a = a * b

escreva(a)
```

3. Realize o teste de mesa e informe a saída:

```portugol
inteiro idade = 15

se(idade >= 18){
    escreva("Maior")
}
senao{
    escreva("Menor")
}
```

4. Faça o teste de mesa do laço abaixo:

```portugol
inteiro soma = 0

para(inteiro i = 1; i <= 5; i++){
    soma = soma + i
}

escreva(soma)
```

5. Complete a tabela do teste de mesa para o algoritmo:

```portugol
inteiro contador = 0

para(inteiro i = 0; i < 4; i++){
    contador++
}

escreva(contador)
```
