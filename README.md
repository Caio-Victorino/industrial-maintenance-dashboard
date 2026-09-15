# 📊 Dashboard Executivo de Manutenção Industrial & Qualidade

![Python](https://img.shields.io/badge/Python-3873A9?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

---

## 🎯 Contexto de Negócio

Na rotina de fabricação industrial, avaliar apenas custos médios oculta problemas de instabilidade operacional nos turnos da noite. Este projeto foi desenvolvido para fornecer à liderança de manutenção um **painel analítico integrado** que correlaciona a severidade financeira dos reparos com a dispersão de tempo de parada (*downtime*) por equipamento e por turno.

---

## 📌 Indicadores Analisados no Painel

### 1. Custo Médio de Reparo (R$ mil) | Barplot Agrupado
- **Objetivo:** Comparar o impacto financeiro das paradas por máquina (*Torno CNC*, *Robô Solda*, *Prensa 500T*).
- **Segmentação:** Divisão por turno (*Diurno* vs *Noturno*) via parâmetro `hue`.
- **Resultado:** Validação do custo médio padronizado entre as equipes de manutenção.

### 2. Distribuição e Variabilidade de Downtime | Violinplot Fendido
- **Objetivo:** Identificar instabilidade e variabilidade no tempo de reparo (minutos).
- **Técnica Avançada:** Aplicação de `split=True` para isolar a anatomia de densidade dos turnos *Diurno* e *Noturno* na mesma estrutura gráfica.
- **Resultado:** Detecção de assimetria no turno noturno para a *Prensa 500T*, evidenciando maior instabilidade e tempo de resposta prolongado.

---

## 🛠️ Tecnologias e Métodos

- **Linguagem:** Python 3.x
- **Bibliotecas:** `matplotlib.pyplot`, `seaborn`, `numpy`
- **Arquitetura de Layout:** Estrutura multijanela via `plt.subplots(1, 2)` com endereçamento absoluto por eixos (`axes[0]` e `axes[1]`).
- **Padrão de Código:** Indentação estruturada, estilização executiva e uso de grades de leitura no eixo Y.

---

## 📁 Estrutura do Repositório

```text
├── dashboard_manutencao_industrial.ipynb   # Código completo validado no Google Colab
└── README.md                              # Documentação executiva do projeto
