# TP2 - Raciocínio Probabilístico

- **Disciplina**: Inteligência Artificial IEC034 - 2025/1  
- **Curso**: Engenharia da Computação - Turmas CO01  
- **Aluno**: Antonio Mileysson França Bragança - 21850963  

---

## Descrição

Este trabalho utiliza uma rede bayesiana para modelar a probabilidade de uma lâmpada funcionar corretamente com base em diversas variáveis do sistema elétrico alimentado por dínamo. O modelo considera probabilidades independentes e condicionais entre os componentes, como voltagem, condições da rua e integridade do sistema.

### Variáveis Envolvidas

- **Lâmpada (b)**: Funcionamento da lâmpada.  
  - P(b = true) = 0.97  
- **Cabo (k)**: Estado do cabo de alimentação.  
  - P(k = true) = 0.90  
- **Luz Ligada (li)**: Depende de `v`, `b`, `k`.  
- **Condição da Rua (str)**:  
  - P(dry) = 0.85  
  - P(wet) = 0.10  
  - P(snow_covered) = 0.05  
- **Volante do Dínamo (flw)**: Indica desgaste.  
  - P(flw = true) = 0.10  
- **Dínamo Deslizante (r)**: Condicional ao `str` e `flw`.  
- **Voltagem (v)**: Depende de `r`.

### Probabilidades Condicionais

- **li (Luz Ligada)**:
  - Se `v`, `b`, `k` forem verdadeiros: P(li) = 0.99  
  - Demais combinações possuem valores entre 0.0 e 0.3  

- **r (Dínamo)**:
  - Se `str = snow_covered` e `flw = false`: P(r) = 0.8  
  - Se `str = dry` e `flw = true`: P(r) = 0.1  

- **v (Voltagem)**:
  - Se `r = true`: P(v) = 0.9  
  - Se `r = false`: P(v) = 0.2  

## Evidência Observada

- A rua está coberta de neve:  
  ```prolog
  evidence(str(snow_covered), true).
