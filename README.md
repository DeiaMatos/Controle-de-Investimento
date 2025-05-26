# Controle de Investimento

# 📊 Planilha de Investimentos FIIs por Perfil de Risco

Essa planilha foi criada para auxiliar investidores a simular e planejar seus aportes mensais em Fundos Imobiliários (FIIs), com alocação personalizada de acordo com o perfil de risco (Conservador, Moderado ou Agressivo).

---

## ✅ Objetivos

- Simular o valor acumulado com investimentos mensais ao longo do tempo
- Visualizar o valor estimado de dividendos mensais
- Definir a alocação ideal de ativos com base no perfil de risco
- Acompanhar o crescimento do patrimônio e a distribuição da carteira por tipo de FII
------

### 📈 Aba `ControleDeInvestimento`

#### Seção: Configurações Iniciais
- **Salário**: valor mensal de referência
- **Sugestão de investimento**: 30% do salário (ajustável)
- **Rendimento estimado da carteira**: 0,6% ao mês

#### Seção: Investimento Mensal
- Valor mensal investido (ex: R$ 200,00)
- Duração do investimento em anos (ex: 5 anos)
- Taxa de juros compostos (ex: 1,08% ao mês)
- **Fórmula principal**: `=VF(taxa; períodos; pagamento)`
- Simulação de dividendos mensais: `ValorAcumulado * 0,006`

#### Seção: Alocação por Perfil
- Perfil selecionado (Conservador / Moderado / Agressivo)
- Alocação do valor investido por tipo de FII
- Cálculo automático via `PROCV` (ex: `=PROCV("Conservador-PAPEL", ...)`)
- Gráfico de pizza dinâmico

----------------------------------------------------------------------

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


