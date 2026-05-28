# 📊 Guia: Configurar Google Sheets

## Passo 1: Criar a Planilha

1. Acesse [Google Sheets](https://sheets.google.com)
2. Clique em **+ Criar nova planilha**
3. Dê um nome: "Festejos Juninos - Sergipe"

## Passo 2: Estruturar as Colunas

Na primeira linha, crie as seguintes colunas:

```
A: nome
B: lat
C: lon
D: abts
E: ur
F: efetivo
G: risco
H: coordenacao
I: publico
J: eventos_programados
K: eventos_complementares
```

## Passo 3: Adicionar Dados

### Exemplo - Aracaju:

| nome | lat | lon | abts | ur | efetivo | risco | coordenacao | publico | eventos_programados | eventos_complementares |
|------|-----|-----|------|--|---------|----|-------------|---------|---------------------|----------------------|
| Aracaju | -10.9472 | -37.0731 | 1 | 2 | 30+ | Alto | 1º GBM | 30.000+ | 🎤 Vila do Forró: 01 a 30/06 | 📍 Praça Santos Dumont (12 e 13/06): 🚑 01 viatura |

**Dicas:**
- Use quebras de linha para múltiplos eventos (Ctrl+Enter)
- Copie coordenadas do Google Maps (clique direito > Coordenadas)
- Deixe células vazias para informações indisponíveis

## Passo 4: Publicar como CSV

1. Clique em **Arquivo**
2. Selecione **Compartilhar > Publicar na Web**
3. Na caixa de diálogo:
   - **Link**: Copie o URL gerado
   - **Formato**: Altere para **CSV**
4. Clique em **Publicar**

## Passo 5: Atualizar o index.html

1. Abra o arquivo `index.html`
2. Localize esta linha:

```javascript
const URL_PLANILHA_CSV = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vRRv-CBDj8UMUo32h5_wkViXlTX72qRCoKOOM3gKxvpT3XAcYwd_ZemvShx87VPRUNU1B4PTZZkVn0P/pub?output=csv';
```

3. Substitua pelo URL da sua planilha (que copiou no Passo 4)
4. Salve o arquivo

## ✅ Pronto!

Agora abra `index.html` no navegador e o mapa carregará automaticamente com seus dados!

---

## 🔄 Atualizar Dados

Toda vez que você editar a planilha Google Sheets, o mapa **atualiza automaticamente** ao recarregar a página (com pequeno delay de cache).

## 🆘 Solucionar Problemas

### "A carregar dados operacionais... 📡" não desaparece
- Verifique se a planilha está publicada como CSV
- Verifique o URL da planilha no console do navegador (F12 > Console)

### Dados não aparecem no mapa
- Verifique se as colunas `lat` e `lon` têm valores numéricos
- Certifique-se de que `nome` não está vazio

### PopUps vazios
- Adicione dados nas colunas `abts` ou `efetivo` para ativar o popup completo

---

Para mais ajuda, abra as Ferramentas de Desenvolvedor (F12) e verifique os erros no Console.