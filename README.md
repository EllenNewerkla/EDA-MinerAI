# EDA-MinerAI - Trabalho Final de Mineração de Dados (P2)
Este repositório contém o notebook e a documentação referentes ao Trabalho Final da disciplina de Mineração de Dados.  
O objetivo foi realizar EDA (Análise de Dados Exploratória) para compreender o comportamento dos dados e tentar descobrir um padrão que explique e diferencie clientes bons de maus pagadores.

---

## Principais Insights

### 1. **Distribuição do Risco de Inadimplência**
A proporção entre bons e maus pagadores é relativamente equilibrada, tornando o dataset adequado para modelagem sem necessidade imediata de reamostragem.

---

### 2. **Variáveis Demográficas**

**2.1. Sexo**  
- Mulheres e homens têm taxas semelhantes.  
- Inadimplência levemente maior entre homens (~27% vs. ~25%).

**2.2. Estado Civil**  
- Solteiros apresentam maior risco.  
- Casados, divorciados e viúvos: menores taxas, sugerindo estabilidade.  
- Categorias pequenas exigem cautela na interpretação.

**2.3. Número de Dependentes**  
- De 0 a 2 dependentes: comportamento praticamente uniforme.  
- A partir de 3: risco aumenta gradualmente.  
- Valores muito altos são estatisticamente instáveis.

---

### 3. **Escolaridade**
A variável original não possui dados válidos.  
Com o nível educacional do cônjuge como proxy:

- Níveis mais baixos → maior risco.  
- Categorias pequenas distorcem resultados.  
- Indica influência moderada da educação, mas limitada pela baixa qualidade do atributo.

---

### 4. **Localização (Estado Residencial)**
A inadimplência varia entre **18% e 32%**:

- Menor risco: SC, RS, RO  
- Maior risco: SE, DF, AL, AM  

A geografia influencia de forma moderada; estados com poucos registros foram analisados com cuidado.

---

### 5. **Renda e Outliers**
- Maior concentração em renda baixa/média.  
- Muitos outliers distorciam visualizações → limitar o eixo foi útil.  
- Apesar da dispersão elevada, a mediana se mantém estável.

---

### 6. **Tipo de Residência**
Após substituir boxplot por barplot:

- Grupos **2, 4 e 5** exibem maior risco (~29–30%).  
- Grupo **3** apresenta o menor risco (~20%).  

Mesmo sem documentação completa dos códigos, a variável possui forte relação com inadimplência.

---

### 7. **Outras Fontes de Renda**
Com a variável binária `FLAG_OUTRAS_RENDAS`:

- Ter outras fontes reduz levemente o risco.  
- Diferença moderada, porém perceptível.

---

### 8. **Idade**
- Clientes mais jovens → maior inadimplência.  
- Clientes mais velhos → comportamento mais estável.  
- Idade se mostrou um preditor relevante e consistente.

---

## Síntese Final

A inadimplência é influenciada por múltiplos fatores: nenhum atributo isolado explica o risco, mas diversos elementos apresentam efeitos moderados e coerentes — como idade, estado civil, número de dependentes, tipo de residência e nível educacional (proxy).

Mesmo com limitações e ausência de algumas variáveis essenciais, o conjunto de dados permitiu identificar tendências sólidas:  
**fatores ligados à estabilidade financeira e familiar reduzem o risco, enquanto variáveis associadas à vulnerabilidade econômica aumentam a probabilidade de inadimplência.**

A análise oferece uma base consistente para etapas posteriores, como modelagem preditiva, segmentação ou definição de políticas de crédito.
