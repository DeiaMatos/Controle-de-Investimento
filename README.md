# Controle-de-Investimento
Planilha para controle de investimento.

## 🧩 Funcionalidades

- Definição do perfil de investidor com base em perguntas simples
- Simulação de cenários com estimativas de rendimento mensal
- Sugestões de alocação conforme perfil de risco
- Projeção de patrimônio acumulado ao longo do tempo
- Visualização gráfica e resumo dos dividendos mensais

## 📸 Imagens da Planilha

| Cenários | Sugestão de Alocação |
|----------|-----------------------|
| ![Cenários](images/Form_Cenarios.png) | ![Sugestão](images/Form_Sugestao_Invest.png) |

| Perfil de Investidor | Tabela de Apoio |
|----------------------|-----------------|
| ![Perfil](images/Print_Perfil.png) | ![Tabela](images/Print_Tab_Apoio.png) |

| Projeção de Patrimônio | Dividendos Mensais |
|------------------------|---------------------|
| ![Patrimônio](images/Form_Patrimo_Acumulado.png) | ![Dividendos](images/Form_Dividendos_Mensais.png) |

| Gráfico Final | Cofrinho |
|---------------|----------|
| ![Gráfico](images/Print_Grafico.png) | ![Cofrinho](images/Print_Cofrinho.png) |

## 🧠 Perfil de Risco

A definição do perfil de investidor é baseada em uma abordagem simples e acessível, voltada a iniciantes que desejam clareza sobre seu grau de tolerância a risco.

# 📐 Explicação das Fórmulas Utilizadas

Este arquivo apresenta uma explicação detalhada das principais fórmulas usadas na planilha **FII por Perfil de Investidor**. Cada fórmula contribui para o funcionamento automático das simulações e sugestões de alocação da carteira.

## 📊 Fórmulas e Funções

| Fórmula | Descrição | Finalidade |
|--------|------------|------------|
| `=D14*30%` | Multiplica o valor da célula D14 por 30% | Usado para calcular um aporte parcial proporcional |
| `=VF(D22;D21*12;D20*-1)` | Valor Futuro com taxa, períodos e aporte | Simula o valor futuro acumulado com juros compostos mensais |
| `=D23*$D$15` | Multiplica um valor dinâmico por um valor fixo | Converte quantidade ou índice em valor monetário |
| `=VF($D$22;A$29*12;$D$20*-1)` | Valor Futuro com número de períodos variável | Simula patrimônio futuro em diferentes horizontes de tempo |
| `=C29*$D$15` | Multiplica quantidade por valor unitário fixo | Usado para calcular o valor total de cotas ou investimento |
| `=PROCV($C$35&"-"&B39;Apoio!$A:$D;4;FALSO)` | Procura dados na aba Apoio com chave composta | Retorna recomendações ou alocações com base em FII + Perfil |
| `=C42*$C$36` | Multiplica rendimento esperado por proporção definida | Calcula rendimento proporcional ou valor alocado |
| `=B7&"-"&C7` | Concatena duas células com hífen | Cria uma chave única para uso em buscas (`PROCV`) |

---

✅ Estas fórmulas foram aplicadas para tornar a planilha **inteligente e responsiva**, gerando:
- Simulações automáticas de crescimento patrimonial
- Sugestões dinâmicas baseadas no perfil do investidor
- Distribuições percentuais realistas
- Análises rápidas com base em dados auxiliares


