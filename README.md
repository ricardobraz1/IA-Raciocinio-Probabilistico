# 2o Trabalho - Raciocínio Probabilistico

- **Disciplina**: Inteligência Artificial
- **Curso**: Engenharia da Computação

- **Aluno**:  Ricardo Mendonça Braz

### Variáveis

1.  **Lâmpada (b):** A probabilidade da lâmpada estar funcionando corretamente.
    
    -   Probabilidade de `b` (lâmpada ok): **0.97**
        
2.  **Cabo (k):** A probabilidade de o cabo estar em bom estado.
    
    -   Probabilidade de `k` (cabo ok): **0.90**
        
3.  **Luz Ligada (li):** A probabilidade de a luz estar ligada, dada uma série de condições.
    
    -   A luz depende do estado da lâmpada, do cabo e da voltagem gerada.
        
4.  **Condição da Rua (str):** A rua pode ter três condições possíveis:
    
    -   **dry:** Seca com probabilidade **0.85**
        
    -   **wet:** Molhada com probabilidade **0.10**
        
    -   **snow_covered:** Coberta de neve com probabilidade **0.05**
        
5.  **Volante do Dínamo (flw):** Indica se o volante do dínamo está desgastado.
    
    -   Probabilidade de desgaste do volante (`flw`): **0.10**
        
6.  **Dínamo Deslizante R:** O estado do dínamo baseado na condição da rua e no desgaste do volante. Variável condicional.
    
    -   As probabilidades de `r` variam de acordo com o estado da rua (`str`) e o desgaste do volante (`flw`).
        
7.  **Voltagem (V):** A probabilidade de a voltagem ser suficiente para acender a lâmpada, dada a condição do dínamo (`r`).
    

### Probabilidades Condicionais

-   **Luz Ligada (li):**
    
    -   Se a voltagem está disponível e o cabo e a lâmpada estão em boas condições, a luz tem **99%** de chance de estar ligada.
        
    -   Existem várias probabilidades condicionais dependendo de qual combinação de estado da lâmpada (`b`), cabo (`k`), e voltagem (`v`) se aplicam.
        
-   **Dínamo Deslizante (r):**
    
    -   Dependendo da condição da rua e do desgaste do volante, a probabilidade de o dínamo estar funcionando varia. Por exemplo:
        
        -   Se a rua está seca e o volante está desgastado, a probabilidade de o dínamo funcionar é **10%**.
            
        -   Se a rua está coberta de neve e o volante está em bom estado, a probabilidade sobe para **80%**.
            
-   **Voltagem (v):**
    
    -   Se o dínamo está funcionando (`r`), a probabilidade de a voltagem ser adequada para acender a lâmpada é de **80%**.
        
    -   Se o dínamo não está funcionando, a probabilidade de a voltagem ser suficiente é apenas **20%**.
        
