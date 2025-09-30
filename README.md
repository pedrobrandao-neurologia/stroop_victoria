# Teste de Stroop - Versão Victoria

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

Uma implementação digital fiel do Teste de Stroop na **Versão Victoria (Perret, 1974)**, desenvolvida em HTML5, JavaScript puro e CSS. Ferramenta profissional para avaliação neuropsicológica de atenção seletiva, controle inibitório e flexibilidade mental.

## 📋 Índice

- [Sobre o Teste](#sobre-o-teste)
- [Versão Victoria](#versão-victoria)
- [Características](#características)
- [Demo](#demo)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Interpretação dos Resultados](#interpretação-dos-resultados)
- [Dados Normativos](#dados-normativos)
- [Estrutura de Dados](#estrutura-de-dados)
- [Exportação de Resultados](#exportação-de-resultados)
- [Compatibilidade](#compatibilidade)
- [Uso Clínico](#uso-clínico)
- [Contribuindo](#contribuindo)
- [Licença](#licença)
- [Citação](#citação)

## 🧠 Sobre o Teste

O Teste de Stroop é uma das ferramentas mais consolidadas em neuropsicologia para avaliação de funções executivas, especificamente:

### Funções Avaliadas

- **Atenção Seletiva**: Capacidade de focar em informações relevantes ignorando distratores
- **Controle Inibitório**: Habilidade de suprimir respostas automáticas inadequadas  
- **Flexibilidade Mental**: Adaptação a demandas cognitivas conflitantes
- **Velocidade de Processamento**: Eficiência do processamento cognitivo
- **Sustentação Atencional**: Manutenção do foco ao longo da tarefa

### Sensibilidade Clínica

O teste é sensível a:
- Disfunções executivas frontais
- Declínio cognitivo em idosos
- TDAH e distúrbios atencionais
- Lesões cerebrais
- Demências e comprometimento cognitivo leve

## 📚 Versão Victoria

Esta implementação segue fielmente a **Versão Victoria** padronizada por Perret (1974), amplamente utilizada na prática clínica brasileira e internacional.

### Estrutura do Teste

O teste consiste em **3 cartões** apresentados sequencialmente:

#### Cartão 1 - Retângulos (D)
- **24 retângulos coloridos** (6 linhas × 4 colunas)
- Tarefa: Nomear as cores dos retângulos
- Objetivo: Linha de base de velocidade de nomeação
- Cores: Verde, Azul, Rosa, Marrom

#### Cartão 2 - Palavras Neutras (W)
- **24 palavras neutras** coloridas
- Palavras: CADA, NUNCA, HOJE, TUDO
- Tarefa: Nomear as cores (ignorar as palavras)
- Objetivo: Avaliar interferência semântica básica

#### Cartão 3 - Cores (C)
- **24 nomes de cores** impressos em cores diferentes
- Palavras: VERDE, AZUL, ROSA, MARROM
- Tarefa: Nomear as cores (ignorar o significado)
- Objetivo: Máxima interferência (Efeito Stroop)

### Administração

- **Duração**: Aproximadamente 5 minutos
- **População**: Adolescentes, adultos e idosos (17+ anos)
- **Instrução**: Nomear cores em sequência, linha por linha, esquerda para direita, o mais rápido possível

## ✨ Características

### Interface Profissional
- Interface fiel ao formato físico do teste
- Layout de 6×4 itens conforme protocolo original
- Cores padronizadas (Verde #00FF00, Azul #0000FF, Rosa #FFC0CB, Marrom #8B4513)
- Timer com precisão de centésimos de segundo
- Design responsivo para diferentes dispositivos

### Funcionalidades Clínicas
- Registro automático de tempo por cartão
- Contagem de erros por cartão
- Cálculo automático da razão C/D (efeito interferência)
- Comparação com dados normativos por faixa etária
- Cálculo de Z-scores
- Feedback visual de progresso

### Coleta de Dados
- Registro completo de cada resposta
- Timestamps precisos
- Identificação de erros por item
- Metadados do participante (nome, idade, escolaridade)
- Exportação em múltiplos formatos

## 🎮 Demo

[🔗 Experimente online](seu-link-github-pages)

![Stroop Victoria Demo](screenshot.png)

## 📥 Instalação

### Opção 1: Download Direto
```bash
git clone https://github.com/seu-usuario/stroop-victoria.git
cd stroop-victoria
# Abra index.html no navegador
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
2. Settings → Pages → Source: main branch
3. Acesse: `https://seu-usuario.github.io/stroop-victoria`

## 🚀 Como Usar

### Aplicação do Teste

1. **Configuração Inicial**
   - Nome completo do participante
   - Idade (para comparação normativa)
   - Nível de escolaridade
   - Clique em "Iniciar Teste"

2. **Cartão 1 - Retângulos**
   - Instrua: "Nomeie as CORES dos retângulos"
   - Clique em qualquer cor para iniciar o cronômetro
   - Clique nas cores conforme o participante nomeia
   - Continue até completar os 24 itens

3. **Cartão 2 - Palavras Neutras**
   - Instrua: "Nomeie as CORES das palavras, ignore o que está escrito"
   - Repita o processo

4. **Cartão 3 - Cores (Interferência)**
   - Instrua: "Nomeie as CORES, ignore os nomes das cores escritos"
   - Complete os 24 itens
   - Teste finaliza automaticamente

5. **Visualização e Exportação**
   - Revise os resultados imediatamente
   - Exporte em CSV, JSON ou PDF
   - Reinicie para novo participante

### Orientações para Avaliadores

**Antes de Iniciar:**
- Verifique se o participante entendeu as instruções
- Teste de visão de cores adequada
- Ambiente tranquilo e sem distrações
- Posicionamento confortável

**Durante a Aplicação:**
- Não interrompa durante a execução de um cartão
- Registre todos os erros (auto-correções contam)
- Mantenha ritmo constante
- Encorajamento neutro se necessário

**Após Conclusão:**
- Verifique se houve dificuldades técnicas
- Documente observações qualitativas
- Exporte dados imediatamente

## 📊 Interpretação dos Resultados

### Métricas Principais

#### 1. Tempo por Cartão (segundos)
- **Cartão D**: Linha de base de velocidade
- **Cartão W**: Interferência semântica
- **Cartão C**: Interferência máxima (Efeito Stroop)

#### 2. Erros
- Contagem total por cartão
- Maior relevância clínica no Cartão C

#### 3. Razão C/D
```
C/D = Tempo Cartão C ÷ Tempo Cartão D
```
- **Interpretação**: Magnitude do efeito de interferência
- Valores típicos: 1.8 - 3.0
- Valores > 3.0: Sugerem dificuldade significativa

#### 4. Z-Score
```
Z = (Tempo Observado - Média Normativa) ÷ Desvio Padrão
```
- **|Z| ≤ 1.0**: Dentro do esperado
- **Z > 1.0**: Abaixo do esperado (tempo aumentado)
- **Z < -1.0**: Acima do esperado (tempo diminuído)

### Interpretação Clínica

#### Desempenho Normal
- Tempos dentro de ±1 DP da média normativa
- Poucos erros (0-2) nos cartões
- Razão C/D dentro da faixa esperada
- Aumento progressivo: D < W < C

#### Sinais de Alerta
- **Tempo elevado no Cartão C**: Dificuldade de inibição
- **Muitos erros**: Desatenção ou impulsividade
- **C/D > 3.0**: Interferência excessiva
- **Tempo D já elevado**: Lentidão processual geral

#### Perfis Clínicos

**TDAH:**
- Erros elevados em todos os cartões
- Variabilidade de desempenho
- Impulsividade nas respostas

**Declínio Cognitivo:**
- Tempo aumentado progressivamente
- Dificuldade especial no Cartão C
- Mais proeminente em idosos

**Lesão Frontal:**
- Razão C/D muito elevada
- Perseverações
- Dificuldade de autocorreção

## 📈 Dados Normativos

### Tabela Normativa (Versão Victoria)

| Faixa Etária | D (seg) | W (seg) | C (seg) | C/D |
|--------------|---------|---------|---------|-----|
| 17-29 anos   | 11.79 ± 2.79 | 13.46 ± 3.11 | 21.28 ± 5.37 | 1.85 |
| 30-39 anos   | 11.14 ± 1.68 | 13.81 ± 2.66 | 25.08 ± 9.52 | 2.25 |
| 40-49 anos   | 12.16 ± 1.96 | 14.82 ± 2.46 | 27.20 ± 5.15 | 2.28 |
| 50-59 anos   | 12.84 ± 2.43 | 15.96 ± 2.93 | 28.48 ± 8.07 | 2.28 |
| 60-69 anos   | 12.56 ± 1.89 | 16.16 ± 3.46 | 31.32 ± 8.22 | 2.55 |
| 70-79 anos   | 14.96 ± 5.10 | 19.11 ± 5.13 | 39.56 ± 13.26 | 2.81 |
| 80+ anos     | 19.31 ± 4.91 | 23.91 ± 5.30 | 56.98 ± 23.70 | 2.95 |

**Fonte**: Victoria - Perret (1974), validação brasileira

### Considerações Normativas

- Dados baseados em população brasileira
- Variação normal aumenta com a idade
- Escolaridade pode influenciar desempenho
- Considerar contexto cultural e linguístico

## 📁 Estrutura de Dados

### Formato de Exportação

```json
{
  "participante": {
    "nome": "João Silva",
    "idade": 45,
    "escolaridade": "superior",
    "dataAvaliacao": "30/09/2025, 14:30:00"
  },
  "resultados": {
    "cartaoD_Retangulos": {
      "tempo_segundos": "12.45",
      "erros": 0
    },
    "cartaoW_PalavrasNeutras": {
      "tempo_segundos": "15.23",
      "erros": 1
    },
    "cartaoC_Cores": {
      "tempo_segundos": "28.67",
      "erros": 2
    },
    "razao_C_sobre_D": "2.30"
  },
  "detalhamento": [
    {
      "cartao": "D",
      "tipo": "rectangles",
      "tentativas": [
        {
          "itemIndex": 0,
          "correctColor": "verde",
          "userResponse": "verde",
          "isCorrect": true,
          "timestamp": 1727712600123
        }
      ]
    }
  ]
}
```

## 📤 Exportação de Resultados

### Formatos Disponíveis

#### 1. CSV (Excel, SPSS, R)
- Formato tabular para análise estatística
- UTF-8 com BOM para caracteres especiais
- Estrutura hierárquica: dados do participante + resultados

**Exemplo:**
```csv
TESTE DE STROOP - VERSAO VICTORIA

DADOS DO PARTICIPANTE
Campo,Valor
Nome,"João Silva"
Idade,45
Escolaridade,"superior"

RESULTADOS
Cartao,Tempo(s),Erros
D - Retangulos,12.45,0
W - Palavras Neutras,15.23,1
C - Cores,28.67,2
Razao C/D,2.30,
```

#### 2. JSON (Análise Programática)
- Estrutura completa com metadados
- Ideal para bancos de dados
- Fácil integração com Python, R, MATLAB

#### 3. PDF (Relatório Clínico)
- Documento formatado profissional
- Tabela de resultados
- Pronto para prontuário

### Uso dos Dados Exportados

**Para Análise Estatística (R):**
```r
# Importar dados
dados <- read.csv("Stroop_Victoria_Participante_2025.csv", 
                  skip = 7, header = TRUE)

# Análise descritiva
summary(dados$Tempo.s.)
```

**Para Análise com Python:**
```python
import json
import pandas as pd

# Carregar JSON
with open('stroop_data.json', 'r') as f:
    data = json.load(f)

# Converter para DataFrame
df = pd.DataFrame([data['resultados']])
```

## 🌐 Compatibilidade

### Navegadores

| Navegador | Desktop | Mobile | Testado |
|-----------|---------|--------|---------|
| Chrome    | ✅ 90+  | ✅     | Sim     |
| Firefox   | ✅ 88+  | ✅     | Sim     |
| Safari    | ✅ 14+  | ✅     | Sim     |
| Edge      | ✅ 90+  | ✅     | Sim     |

### Dispositivos Recomendados

**Ideal:**
- Desktop ou laptop (tela ≥ 13")
- Mouse para seleção precisa
- Ambiente controlado

**Aceitável:**
- Tablet (≥ 10")
- Touch screen responsivo

**Não Recomendado:**
- Smartphones (tela muito pequena)
- Ambientes com distrações

## 🏥 Uso Clínico

### Indicações

- Avaliação neuropsicológica completa
- Rastreio de disfunções executivas
- Monitoramento de declínio cognitivo
- Avaliação pré/pós intervenção
- Perícia médica e jurídica

### Limitações

- Requer alfabetização
- Sensível a daltonismo
- Pode ser afetado por fadiga
- Não é diagnóstico isolado

### Boas Práticas

1. **Padronização**: Siga sempre as mesmas instruções
2. **Ambiente**: Local silencioso e iluminado
3. **Rapport**: Estabeleça boa relação com o participante
4. **Observação**: Registre comportamentos qualitativos
5. **Contexto**: Considere o quadro clínico completo

### Aspectos Éticos

- Consentimento informado obrigatório
- Sigilo dos dados (LGPD)
- Uso apenas por profissionais habilitados
- Devolução de resultados apropriada

## 🤝 Contribuindo

Contribuições são bem-vindas, especialmente de neuropsicólogos e pesquisadores.

### Como Contribuir

1. Fork do projeto
2. Crie branch para feature (`git checkout -b feature/Melhoria`)
3. Commit das mudanças (`git commit -m 'Adiciona Melhoria'`)
4. Push para branch (`git push origin feature/Melhoria`)
5. Abra Pull Request

### Áreas Prioritárias

- [ ] Validação com mais dados normativos brasileiros
- [ ] Suporte a outras versões do Stroop (Golden, Comalli)
- [ ] Integração com sistemas de prontuário eletrônico
- [ ] Análise estatística automatizada
- [ ] Modo de treinamento/demonstração

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja [LICENSE](LICENSE) para detalhes.

```
MIT License - Uso livre para fins clínicos, educacionais e de pesquisa.
```

## 📚 Citação

### Para Uso do Software

```bibtex
@software{stroop_victoria_2025,
  title = {Teste de Stroop - Versão Victoria: Implementação Digital},
  author = {[Seu Nome]},
  year = {2025},
  url = {https://github.com/seu-usuario/stroop-victoria},
  version = {1.0.0}
}
```

### Referências do Teste

**Versão Original:**
```bibtex
@article{stroop1935,
  author = {Stroop, J. Ridley},
  title = {Studies of interference in serial verbal reactions},
  journal = {Journal of Experimental Psychology},
  volume = {18},
  pages = {643--662},
  year = {1935}
}
```

**Versão Victoria:**
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

**Dados Normativos Brasileiros:**
```bibtex
@article{campanholo2014,
  author = {Campanholo, K. R. and others},
  title = {Performance of an adult Brazilian sample on the Trail Making Test and Stroop Test},
  journal = {Dementia \& Neuropsychologia},
  volume = {8},
  number = {1},
  pages = {26--31},
  year = {2014}
}
```


## 🙏 Agradecimentos

- Baseado no protocolo Victoria (Perret, 1974)
- Dados normativos de estudos brasileiros de validação
- Comunidade de neuropsicologia clínica
- Feedback de profissionais da área

## 📞 Contato

**Para questões clínicas:**
- Consulte profissional de neuropsicologia habilitado
- Este software não substitui avaliação profissional

---

**⚕️ Uso Profissional**: Este teste deve ser aplicado e interpretado apenas por profissionais qualificados (psicólogos, neuropsicólogos, médicos).

**📊 Para Pesquisa**: Cite adequadamente em publicações científicas.

[![Star on GitHub](https://img.shields.io/github/stars/seu-usuario/stroop-victoria?style=social)](https://github.com/seu-usuario/stroop-victoria)
