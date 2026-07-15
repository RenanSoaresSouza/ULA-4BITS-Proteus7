# Unidade Lógica Aritmética (ALU)

Projeto de uma Unidade Lógica Aritmética (ALU) de 4 bits implementada inteiramente com portas lógicas e circuitos digitais, sem a utilização de microcontroladores ou programação. O desenvolvimento e a simulação foram realizados no **Proteus 7**.

A ALU executa operações aritméticas e lógicas, como soma, subtração, AND, OR, XOR, NOT e deslocamentos de bits. Também implementa as flags **Carry (C)**, **Zero (Z)**, **Negative (N)** e **Overflow (V)**, além de um modo de operação **Signed/Unsigned**, permitindo o tratamento adequado de números com e sem sinal.

# Funcionalidades
> **Código** refere-se às entradas **CBA**, responsáveis pela seleção da operação executada pela ALU.

| Código | Operação    |
| :----: | ----------- |
|  `000` | Soma        |
|  `001` | Subtração   |
|  `010` | OR          |
|  `011` | AND         |
|  `100` | NOT         |
|  `101` | XOR         |
|  `110` | Shift Left  |
|  `111` | Shift Right |

## Flags

| Flag | Descrição |
|:----:|-----------|
| **C/B** | Carry na soma, Borrow na subtração e bit deslocado nas operações de Shift. |
| **Z** | Ativada quando o resultado da operação é igual a zero. |
| **N** | Indica resultado negativo em operações no modo Signed. |
| **V** | Indica overflow em operações aritméticas no modo Signed. |

## Signed/Unsigned

A ALU possui um bit de seleção que permite operar em modo **Signed** ou **Unsigned**.

- **Signed:** utiliza as flags **N**, **Z** e **V** para interpretação dos resultados.
- **Unsigned:** utiliza as flags **C** e **Z**, desconsiderando as flags **N** e **V**.
