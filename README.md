# 🦊 FoxBet - Calculadora Value Bet Profissional

**Calculadora avançada de Value Bets com Kelly Criterion e Sistema de Unidades**

![FoxBet](https://img.shields.io/badge/FoxBet-Professional-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🎯 O que é FoxBet?

FoxBet é uma calculadora profissional que identifica **Value Bets** (apostas com valor positivo) usando a Pinnacle como referência de mercado e calcula o stake ideal através do **Kelly Criterion**.

### ✨ Características Principais

- ✅ **Cálculo de Expected Value (EV)** preciso
- ✅ **Kelly Criterion** para gestão de banca
- ✅ **Sistema de Unidades** inteligente (0.25u - 1u)
- ✅ **Interface profissional** e responsiva
- ✅ **100% gratuito** e open-source
- ✅ **Funciona offline** após carregamento

## 🚀 Como Usar

### 1. Coleta de Odds

Você precisa de **4 odds**:

- **Odd 1**: Base da Pinnacle (mercado de referência)
- **Odds 2 e 3**: Outras odds da Pinnacle (para calcular margem)
- **Odd 4**: Odd onde você pretende apostar (casa alvo)

**Exemplo:**
```
Jogo: Flamengo vs Palmeiras

Pinnacle:
- Flamengo: 2.00 ← Odd 1
- Empate: 3.50 ← Odd 2  
- Palmeiras: 4.00 ← Odd 3

Bet365:
- Flamengo: 2.20 ← Odd 4 (você vai apostar aqui)

Input: 2.0 3.5 4.0 2.20
```

### 2. Configure sua Banca

- **Banca Total**: R$ 1.000 (exemplo)
- **Valor de 1 Unidade**: R$ 100 (10% da banca)

### 3. Analise o Resultado

FoxBet calcula:
- ✅ **EV (Expected Value)**: +8.5%
- ✅ **Probabilidade Real**: 48.78%
- ✅ **Recomendação**: 0.75u (R$ 75)

## 📊 Sistema de Unidades

FoxBet usa um sistema inteligente que escala suas apostas baseado no tamanho do edge:

| Unidades | Faixa de EV | Descrição | Exemplo (1u = R$ 100) |
|----------|-------------|-----------|------------------------|
| **0.25u** | 0-2% | Edge Pequeno | R$ 25 |
| **0.50u** | 2-5% | Edge Moderado | R$ 50 |
| **0.75u** | 5-8% | Edge Bom | R$ 75 |
| **1.00u** | 8%+ | Edge Excelente | R$ 100 |

### Por que usar unidades?

- 📈 **Escalabilidade**: Apostas maiores em edges maiores
- 🛡️ **Proteção**: Reduz risco em edges pequenos
- 📊 **Consistência**: Padroniza gestão de banca

## 🧮 Como Funciona (Matemática)

### 1. Cálculo da Probabilidade Real

```javascript
// Remove a margem da casa (overround)
prob1 = 1 / odd1
prob2 = 1 / odd2
prob3 = 1 / odd3
totalProb = prob1 + prob2 + prob3

// Probabilidade verdadeira
trueProb = prob1 / totalProb
```

### 2. Expected Value (EV)

```javascript
EV = (odd_alvo * probabilidade_real) - 1

// Exemplo:
// EV = (2.20 * 0.4878) - 1 = +7.3%
```

### 3. Kelly Criterion

```javascript
// Fórmula: (bp - q) / b
// b = odd - 1
// p = probabilidade de ganhar
// q = 1 - p

kellyFraction = ((b * p) - q) / b
stakeIdeal = kellyFraction * banca
```

## 🌐 Deploy no GitHub Pages

### Passo 1: Fork/Clone

```bash
git clone https://github.com/seu-usuario/foxbet.git
cd foxbet
```

### Passo 2: Habilitar GitHub Pages

1. Vá em **Settings** do repositório
2. Clique em **Pages** (menu lateral)
3. Em **Source**, selecione **main** branch
4. Clique **Save**

Sua calculadora estará online em:
```
https://seu-usuario.github.io/foxbet/
```

## 📱 Uso Comercial

FoxBet é **open-source** (MIT License), mas você pode:

✅ Usar gratuitamente
✅ Modificar conforme necessário
✅ Integrar em produtos comerciais
✅ Hospedar sua própria versão

### Ideias de Monetização

1. **Telegram Bot Premium**: Cobrar por acesso ao bot
2. **Comunidade VIP**: Grupo com análises + calculadora
3. **Afiliação**: Indicar casas de apostas
4. **Consultoria**: Ensinar a usar value betting

## 🛠️ Tecnologias

- HTML5
- CSS3 (Gradientes, Animações)
- JavaScript Vanilla (Sem dependências)
- Responsivo (Mobile-first)

## 📄 Licença

MIT License - Você pode usar comercialmente!

## 🦊 Sobre o Projeto

FoxBet foi criado para democratizar o acesso a ferramentas profissionais de apostas esportivas. 

**Raposas são astutas. Seja astuto com suas apostas.** 🦊

---

**⭐ Se este projeto te ajudou, deixe uma estrela no GitHub!**

## 📞 Contato

- GitHub: [@seu-usuario](https://github.com/seu-usuario)
- Issues: [Reportar Bug](https://github.com/seu-usuario/foxbet/issues)

---

**Aposte com responsabilidade. Apostas envolvem risco de perda financeira. +18**
