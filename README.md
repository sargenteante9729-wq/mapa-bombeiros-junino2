# 🚒 Mapa Interativo - Festejos Juninos em Sergipe

Aplicação web interativa que mapeia municípios atendidos pelo Corpo de Bombeiros de Sergipe durante os festejos juninos, com integração dinâmica a dados do Google Sheets.

## 📋 Características

✅ **Mapa Interativo** - Visualização em tempo real dos municípios usando Leaflet.js  
✅ **Google Sheets Integration** - Dados dinâmicos via CSV  
✅ **Menu Lateral** - Lista navegável de municipios  
✅ **Popups Informativos** - Dados operacionais (ABTs, efetivo, risco, eventos)  
✅ **Responsividade** - Funciona em desktop e mobile  
✅ **Fallback Local** - Dados offline se a planilha não carregar  

## 🎯 Funcionalidades

### Visualização no Mapa
- 🚒 Marcadores interativos para cada município
- 📍 Animação ao clicar na lista lateral
- 📱 PopUps com informações detalhadas

### Dados Exibidos por Município
- **ABTs** - Ambulâncias de Transporte Básico
- **UR** - Unidades de Resgate
- **Efetivo** - Número de bombeiros destacados
- **Risco** - Nível de risco do município
- **Coordenação** - Responsável pela coordenação
- **Público Estimado** - Número esperado de pessoas
- **Eventos Programados** - Festas e celebrações
- **Eventos Complementares** - Atividades extras

## 🔧 Configuração

### Alterar Planilha Google Sheets

1. Abra sua planilha no Google Sheets
2. Clique em **Arquivo > Compartilhar > Publicar na Web**
3. Escolha **CSV** como formato
4. Copie o URL gerado
5. No arquivo `index.html`, atualize a constante:

```javascript
const URL_PLANILHA_CSV = 'SEU_URL_AQUI';
```

### Estrutura da Planilha

Crie as seguintes colunas no Google Sheets:

| Coluna | Descrição |
|--------|----------|
| `nome` | Nome do município |
| `lat` | Latitude |
| `lon` | Longitude |
| `abts` | Quantidade de ABTs |
| `ur` | Quantidade de Unidades de Resgate |
| `efetivo` | Número de bombeiros |
| `risco` | Nível de risco (Baixo/Médio/Alto) |
| `coordenacao` | Responsável pela coordenação |
| `publico` | Público estimado |
| `eventos_programados` | Eventos principais (use quebras de linha) |
| `eventos_complementares` | Eventos extras (use quebras de linha) |

## 📱 Responsividade

- **Desktop**: Menu lateral (320px) + Mapa (60% largura)
- **Mobile**: Menu inferior (40% altura) + Mapa (60% altura)

## 🗺️ Bibliotecas Utilizadas

- **Leaflet.js** - Renderização do mapa
- **OpenStreetMap** - Camada de mapa base
- **PapaParse** - Parsing de CSV
- **Google Sheets** - Armazenamento de dados

## 🚀 Como Usar

1. Clone o repositório
2. Abra `index.html` em um navegador
3. O mapa carregará automaticamente com os dados da planilha

## 📝 Notas

- Os dados são carregados automaticamente da planilha Google Sheets
- Se a planilha não carregar, a aplicação usa dados de fallback locais
- Os popups possuem suporte a quebras de linha (`\n`)
- A navegação é intuitiva: clique em um município na lista para voar até ele no mapa

## 👨‍💻 Desenvolvido Para

Corpo de Bombeiros - Sergipe 🇧🇷

---

**Última atualização**: 2026-05-28