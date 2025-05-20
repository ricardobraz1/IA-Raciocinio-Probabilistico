# 🧠 2º Trabalho – Raciocínio Probabilístico

- **Disciplina**: Inteligência Artificial – IEC034 (2025/1)  
- **Curso**: Engenharia da Computação – Turma CO01  
- **Aluno**: Ricardo Mendonça Braz – 22152017

---

## 📌 Descrição

Este projeto consiste na modelagem de uma **Rede Bayesiana** utilizando a linguagem **ProbLog**, com o objetivo de calcular a probabilidade da **voltagem (v)** ser suficiente para acender uma lâmpada, considerando diversos fatores condicionais como o estado do cabo, da lâmpada, da voltagem gerada, entre outros.

---

## 🔧 Variáveis Utilizadas

1. **Lâmpada (`b`)**  
   Probabilidade de estar funcionando corretamente: **0.97**

2. **Cabo (`k`)**  
   Probabilidade de estar em bom estado: **0.90**

3. **Condição da Rua (`str`)**
   - `dry` (seca): **0.85**
   - `wet` (molhada): **0.10**
   - `snow_covered` (coberta de neve): **0.05**

4. **Volante do Dínamo (`flw`)**  
   Probabilidade de estar desgastado: **0.10**

5. **Dínamo Deslizante (`r`)**  
   Probabilidade condicional com base
