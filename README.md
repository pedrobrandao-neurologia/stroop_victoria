# Teste de Stroop Victoria - Auto-Aplicado

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

Implementação digital auto-aplicável do **Teste de Stroop - Versão Victoria (Perret, 1974)** para avaliação neuropsicológica de atenção seletiva, controle inibitório e flexibilidade mental. Desenvolvido em HTML5, JavaScript puro e CSS com paradigma psicofísico rigoroso.

## 📋 Índice

- [Sobre o Teste](#sobre-o-teste)
- [Características](#características)
- [Paradigma Auto-Aplicado](#paradigma-auto-aplicado)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Estrutura de Dados](#estrutura-de-dados)
- [Dados Normativos](#dados-normativos)
- [Interpretação](#interpretação)
- [Exportação](#exportação)
- [Validade Clínica](#validade-clínica)
- [Compatibilidade](#compatibilidade)
- [Limitações](#limitações)
- [Contribuindo](#contribuindo)
- [Licença](#licença)
- [Citação](#citação)

## 🧠 Sobre o Teste

O Teste de Stroop é um instrumento neuropsicológico clássico para avaliação de:

- **Atenção Seletiva**: Capacidade de focar em informação relevante
- **Controle Inibitório**: Supressão de respostas automáticas
- **Flexibilidade Mental**: Adaptação a demandas conflitantes
- **Velocidade de Processamento**: Eficiência cognitiva

### Versão Victoria

Esta implementação segue fielmente o protocolo **Victoria (Perret, 1974)**, amplamente validado internacionalmente:

**Estrutura:**
- **Cartão D (Retângulos)**: 24 retângulos coloridos - linha de base de velocidade
- **Cartão W (Palavras Neutras)**: 24 palavras neutras coloridas - interferência semântica
- **Cartão C (Cores)**: 24 nomes de cores em cores diferentes - interferência máxima (Efeito Stroop)

**Cores utilizadas:**
- Verde (#00FF00)
- Rosa (#FFC0CB)
- Azul (#0000FF)
- Marrom (#8B4513)

## ✨ Características

### Interface Auto-Aplicável
- ✅ **Apresentação sequencial**: Um estímulo por vez (paradigma psicofísico)
- ✅ **Feedback imediato**: Visual instantâneo (correto/incorreto)
- ✅ **Progressão automática**: Fluxo contínuo entre itens e cartões
- ✅ **Sem necessidade de avaliador**: Participante responde diretamente
- ✅ **Cronometragem precisa**: Timer de alta resolução (10ms)

### Coleta de Dados Rigorosa
- ✅ **Tempo de reação por item**: Precisão de milissegundos
- ✅ **Registro completo**: Cada resposta com timestamp
- ✅ **Cálculo automático de erros**: Sem intervenção manual
- ✅ **Sequência preservada**: Ordem exata conforme protocolo Victoria

### Análise Automatizada
- ✅ **Razão C/D**: Efeito de interferência
- ✅ **Z-scores**: Comparação com normas brasileiras
- ✅ **Interpretação automática**: Feedback imediato ao participante
- ✅ **Dados normativos integrados**: 7 faixas etárias (17-80+)

## 🎯 Paradigma Auto-Aplicado

Esta implementação utiliza princípios de psicofísica experimental:

### Fluxo de Apresentação

```
[Estímulo 1] → [Resposta] → [Feedback 300ms] → [Pausa 200ms] →
[Estímulo 2] → [Resposta] → [Feedback 300ms] → [Pausa 200ms] →
... (24 itens) →
[Próximo Cartão]
```

### Características Psicofísicas

**Inspirado em protocolos MATLAB clássicos:**
- Apresentação serial (não simultânea)
- Inter-stimulus interval (ISI) controlado
- Feedback imediato para reforço
- Coleta de tempo de reação preciso
- Registro automático de acurácia

**Diferenças do protocolo tradicional:**

| Aspecto | Tradicional (Com Avaliador) | Auto-Aplicado (Digital) |
|---------|----------------------------|-------------------------|
| Apresentação | Grade completa (6×4) | Item por item |
| Resposta | Verbal | Clique em botão |
| Registro | Manual (avaliador) | Automático |
| Feedback | Ausente ou tardio | Imediato |
| Tempo | Cronômetro total | TR individual + total |
| Erros | Contagem manual | Detecção automática |

## 📥 Instalação

### Opção 1: Download Direto
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/stroop-victoria-auto.git

# Navegue até a pasta
cd stroop-victoria-auto

# Abra no navegador
open index.html
```

### Opção 2: Servidor Local
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# Acesse http://localhost:8000
```

### Opção 3: GitHub Pages
1. Fork do repositório
2. Settings → Pages → Source: main
3. Acesse: `https://seu-usuario.github.io/stroop-victoria-auto`

## 🚀 Como Usar

### Para Participantes

1. **Acesse o teste** via navegador
2. **Preencha seus dados**:
   - Nome completo
   - Idade
   - Escolaridade
3. **Leia as instruções** cuidadosamente
4. **Clique "Iniciar Teste"**
5. **Para cada estímulo mostrado**:
   - Identifique a **COR** (não o texto)
   - Clique no botão correspondente
   - Continue até o final
6. **Visualize seus resultados**
7. **Exporte** se necessário

### Para Pesquisadores/Clínicos

**Configuração:**
- Ambiente silencioso e sem distrações
- Tela adequada (mínimo 13")
- Conexão estável (se online)
- Instruções claras ao participante

**Orientações ao participante:**
- "Responda o mais rápido possível"
- "Clique na COR que vê, não no que está escrito"
- "Não se preocupe com erros ocasionais"
- "Mantenha o foco durante todo o teste"

**Após o teste:**
- Exporte dados imediatamente
- Armazene com identificação adequada
- Respeite LGPD/privacidade

## 📊 Estrutura de Dados

### Formato de Exportação (JSON)

```json
{
  "participante": {
    "nome": "João Silva",
    "idade": 35,
    "escolaridade": "superior",
    "dataAvaliacao": "30/09/2025, 14:30:00"
  },
  "resultados": {
    "cartaoD_Retangulos": {
      "tempo_segundos": "12.45",
      "erros": 1,
      "tentativas": 24
    },
    "cartaoW_PalavrasNeutras": {
      "tempo_segundos": "15.23",
      "erros": 2,
      "tentativas": 24
    },
    "cartaoC_Cores": {
      "tempo_segundos": "28.67",
      "erros": 5,
      "tentativas": 24
    },
    "razao_C_sobre_D": "2.30"
  },
  "detalhamento": [
    {
      "cartao": "D",
      "tipo": "rectangles",
      "trials": [
        {
          "itemIndex": 0,
          "correctColor": "V",
          "userResponse": "V",
          "isCorrect": true,
          "reactionTime": 845,
          "timestamp": 1727712600123
        }
      ]
    }
  ]
}
```

### Variáveis Coletadas

**Por Cartão:**
- Tempo total (segundos)
- Número de erros
- Número de tentativas

**Por Item:**
- Índice do item (0-23)
- Cor correta
- Resposta do usuário
- Acerto (booleano)
- Tempo de reação (ms)
- Timestamp absoluto

## 📈 Dados Normativos

Normas brasileiras validadas (Campanholo et al., 2014):

| Faixa Etária | D (seg) ± DP | W (seg) ± DP | C (seg) ± DP | C/D |
|--------------|--------------|--------------|--------------|-----|
| 17-29 anos   | 11.79 ± 2.79 | 13.46 ± 3.11 | 21.28 ± 5.37 | 1.85 |
| 30-39 anos   | 11.14 ± 1.68 | 13.81 ± 2.66 | 25.08 ± 9.52 | 2.25 |
| 40-49 anos   | 12.16 ± 1.96 | 14.82 ± 2.46 | 27.20 ± 5.15 | 2.28 |
| 50-59 anos   | 12.84 ± 2.43 | 15.96 ± 2.93 | 28.48 ± 8.07 | 2.28 |
| 60-69 anos   | 12.56 ± 1.89 | 16.16 ± 3.46 | 31.32 ± 8.22 | 2.55 |
| 70-79 anos   | 14.96 ± 5.10 | 19.11 ± 5.13 | 39.56 ± 13.26 | 2.81 |
| 80+ anos     | 19.31 ± 4.91 | 23.91 ± 5.30 | 56.98 ± 23.70 | 2.95 |

**Fonte:** Campanholo et al. (2014) - Dement Neuropsychol 8(1):26-31

## 📖 Interpretação

### Métricas Principais

**1. Tempo por Cartão**
- Velocidade de processamento
- Comparar com normas da faixa etária

**2. Razão C/D**
```
C/D = Tempo Cartão C ÷ Tempo Cartão D
```
- **Normal**: 1.8 - 3.0
- **Elevado**: > 3.0 (interferência excessiva)

**3. Z-Score**
```
Z = (Tempo Observado - Média) ÷ Desvio Padrão
```
- **|Z| ≤ 1.0**: Normal
- **Z > 1.0**: Lentidão
- **Z < -1.0**: Muito rápido

**4. Taxa de Erros**
- Cartão C mais sensível
- > 8 erros: Atenção comprometida

### Interpretação Clínica

**Desempenho Normal:**
- Tempos dentro de ±1 DP
- Poucos erros (< 3 por cartão)
- C/D entre 1.8-3.0
- Progressão D < W < C

**Sinais de Alerta:**
- Tempo C muito elevado
- C/D > 3.0
- Muitos erros no Cartão C
- Inconsistência (muito rápido com muitos erros)

**Perfis Típicos:**

| Condição | Tempo | Erros | C/D | Observação |
|----------|-------|-------|-----|------------|
| TDAH | Normal/rápido | Muitos | Normal | Impulsividade |
| Declínio Cognitivo | Aumentado | Moderados | Elevado | Lentidão global |
| Lesão Frontal | C elevado | Muitos em C | Muito alto | Desinibição |
| Ansiedade | Variável | Poucos | Normal | Inconsistência |

## 📤 Exportação

### Formatos Disponíveis

**1. CSV (Comma-Separated Values)**
- Compatível: Excel, SPSS, R, Python, MATLAB
- Codificação: UTF-8 com BOM
- Estrutura: Resumo + Detalhamento por item

```csv
TESTE DE STROOP - VERSAO VICTORIA (AUTO-APLICADO)

DADOS DO PARTICIPANTE
Campo,Valor
Nome,"João Silva"
Idade,35

RESULTADOS
Cartao,Tempo(s),Erros,Acertos,Total
D - Retangulos,12.45,1,23,24

DETALHAMENTO POR ITEM
Cartao,Item,CorCorreta,Resposta,Correto,TempoReacao(ms)
D,1,V,V,Sim,845
```

**2. JSON (JavaScript Object Notation)**
- Análise programática
- Estrutura hierárquica completa
- Fácil integração com sistemas

**3. PDF (Portable Document Format)**
- Relatório formatado
- Documentação clínica
- Inclui tabelas e métricas

### Análise Estatística

**Python (Pandas):**
```python
import pandas as pd
import json

# Carregar dados
with open('stroop_data.json', 'r') as f:
    data = json.load(f)

# Análise de tempo de reação
trials = data['detalhamento'][0]['trials']
df = pd.DataFrame(trials)

# Estatísticas descritivas
print(df['reactionTime'].describe())

# Separar corretos vs incorretos
corretos = df[df['isCorrect'] == True]['reactionTime']
incorretos = df[df['isCorrect'] == False]['reactionTime']
```

**R:**
```r
library(jsonlite)
library(dplyr)

# Carregar dados
data <- fromJSON('stroop_data.json')

# Extrair trials
trials <- data$detalhamento[[1]]$trials

# Análise
summary(trials$reactionTime)
t.test(reactionTime ~ isCorrect, data=trials)
```

## ✅ Validade Clínica

### Validação do Formato Auto-Aplicado

**Vantagens:**
- ✅ Padronização absoluta (sem variação de avaliador)
- ✅ Tempo de reação preciso (impossível manualmente)
- ✅ Registro completo (nenhum erro perdido)
- ✅ Acessibilidade (aplicação remota)
- ✅ Custo-efetivo (sem necessidade de avaliador)

**Limitações:**
- ⚠️ Não observa comportamento qualitativo
- ⚠️ Requer alfabetização digital básica
- ⚠️ Modo de resposta diferente (clique vs verbal)
- ⚠️ Não detecta estratégias atípicas

### Quando Usar

**Apropriado para:**
- Triagem em larga escala
- Telepsicologia/teleneuropsicologia
- Pesquisa com muitos participantes
- Autoavaliação em contextos não-clínicos
- Monitoramento longitudinal

**Não recomendado para:**
- Diagnóstico clínico isolado (sempre combinar com outros testes)
- Pacientes com déficits motores severos
- Pacientes com baixa compreensão digital
- Contextos forenses (preferir aplicação presencial)

### Considerações Éticas

- **Consentimento informado**: Obrigatório antes de iniciar
- **Privacidade**: Dados sensíveis (LGPD)
- **Devolução**: Participante deve receber resultados apropriados
- **Limitações**: Explicar que é uma ferramenta de triagem
- **Uso profissional**: Interpretação por profissional qualificado

## 🌐 Compatibilidade

### Navegadores

| Navegador | Desktop | Mobile | Testado |
|-----------|---------|--------|---------|
| Chrome    | ✅ 90+  | ✅     | Sim     |
| Firefox   | ✅ 88+  | ✅     | Sim     |
| Safari    | ✅ 14+  | ✅     | Sim     |
| Edge      | ✅ 90+  | ✅     | Sim     |

### Dispositivos

**Recomendado:**
- Desktop/Laptop (≥ 13")
- Mouse ou touchpad preciso
- Ambiente silencioso

**Aceitável:**
- Tablet (≥ 10")
- Touch screen responsivo

**Não recomendado:**
- Smartphones (tela pequena, toques imprecisos)

## ⚠️ Limitações

### Diferenças do Protocolo Original

1. **Modo de resposta**: Clique vs nomeação verbal
2. **Apresentação**: Sequential vs simultânea (grade)
3. **Feedback**: Imediato vs ausente
4. **Tempo**: Individual + total vs apenas total

### Implicações

**Tempos podem ser diferentes:**
- Clique geralmente mais rápido que verbal
- Feedback pode facilitar (efeito aprendizagem)
- Apresentação serial elimina estratégias de varredura

**Recomendações:**
- Use normas específicas se disponíveis para formato digital
- Compare intra-indivíduo (pré/pós) com cautela
- Não compare diretamente com normas de aplicação tradicional
- Considere como ferramenta complementar

## 🤝 Contribuindo

Contribuições são bem-vindas, especialmente:

- [ ] Validação com dados de formato digital
- [ ] Normas específicas para versão auto-aplicada
- [ ] Tradução para outros idiomas
- [ ] Acessibilidade aprimorada
- [ ] Integração com sistemas de prontuário

### Como Contribuir

1. Fork do projeto
2. Crie branch (`git checkout -b feature/Melhoria`)
3. Commit (`git commit -m 'Adiciona Melhoria'`)
4. Push (`git push origin feature/Melhoria`)
5. Pull Request

## 📄 Licença

MIT License - Uso livre para fins clínicos, educacionais e de pesquisa.

```
Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

## 📚 Citação

### Software

```bibtex
@software{stroop_victoria_auto_2025,
  title = {Teste de Stroop Victoria - Versão Auto-Aplicada Digital},
  author = {[Seu Nome]},
  year = {2025},
  url = {https://github.com/seu-usuario/stroop-victoria-auto},
  version = {1.0.0}
}
```

### Protocolo Original

```bibtex
@article{perret1974,
  author = {Perret, E.},
  title = {The left frontal lobe of man and the suppression of habitual responses in verbal categorical behaviour},
  journal = {Neuropsychologia},
  volume = {12},
  pages = {323--330},
  year = {1974}
}
```

### Normas Brasileiras

```bibtex
@article{campanholo2014,
  author = {Campanholo, K. R. and others},
  title = {Performance of an adult Brazilian sample on the Trail Making Test and Stroop Test},
  journal = {Dementia \& Neuropsychologia},
  volume = {8},
  number = {1},
  pages = {26--31},
  year = {2014},
  doi = {10.1590/S1980-57642014DN81000005}
}
```

## 📞 Suporte

**Issues:** [GitHub Issues](https://github.com/seu-usuario/stroop-victoria-auto/issues)

**Questões Clínicas:** Consulte profissional de neuropsicologia

**Uso em Pesquisa:** Cite adequadamente em publicações

---

**⚕️ Aviso:** Este teste é uma ferramenta de triagem/pesquisa. Não substitui avaliação neuropsicológica completa por profissional qualificado.

**🔬 Para Pesquisa:** Considere validação adicional do formato auto-aplicado antes de uso em estudos clínicos.

**📊 Dados Abertos:** Contribua com dados normativos para versão digital!
