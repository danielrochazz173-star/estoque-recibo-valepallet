# 📄 Sistema de Geração de Recibos e Vale Pallet

Sistema web para geração automática de recibos e vales pallet para as empresas DICON e Trindade.

## 🚀 Funcionalidades

- ✅ Geração de **Recibos** com valores e informações de pagamento
- ✅ Geração de **Vale Pallet** com múltiplas vias (1 a 4 vias)
- ✅ Suporte para duas empresas: **DICON** e **Trindade**
- ✅ Seleção automática de logo e CNPJ conforme a empresa escolhida
- ✅ Valor padrão de R$ 30,00 para recibos (editável)
- ✅ Campo de data personalizável (usa data atual se não preenchido)
- ✅ Layout otimizado para impressão em folha A4
- ✅ Avisos inteligentes para sábados (DICON) e demais dias (Trindade)
- ✅ Design moderno com tema azul

## 📋 Requisitos

- Navegador web moderno (Chrome, Firefox, Edge, Safari)
- Conexão com internet (apenas para carregar a página inicial)

## 🎯 Como Usar

### Gerar Recibo

1. Selecione **"Recibo"** no campo "Tipo de Documento"
2. Escolha a empresa: **DICON** ou **Trindade**
3. Preencha os campos:
   - Nome do Cliente
   - Quantidade de Paletes
   - Valor por Palete (padrão: R$ 30,00)
   - Forma de Pagamento
   - Número da NF
   - Data (opcional - usa data atual se não preenchido)
4. Clique em **"Gerar Documento"**
5. O sistema gerará 2 vias do recibo automaticamente

### Gerar Vale Pallet

1. Selecione **"Vale Pallet"** no campo "Tipo de Documento"
2. Escolha a empresa: **DICON** ou **Trindade**
3. Preencha os campos:
   - CLIENTE
   - NF
   - QTDE DE PALLETS
   - Data (opcional - usa data atual se não preenchido)
   - Número de Vias (1 a 4)
4. Clique em **"Gerar Documento"**

## 📅 Regras de Negócio

- **Aos sábados**: O procedimento deve ser feito pela **DICON**
- **Demais dias**: Use a empresa **Trindade**
- O sistema exibe avisos automáticos aos sábados

## 🏢 Empresas Configuradas

### DICON
- **CNPJ**: 37.218.268/0001-04
- **Logo**: `dicon_recibo.jpg`

### Trindade
- **CNPJ**: 48.724.616/0001-31
- **Logo**: `trindade_recibo.jpg`

## 📁 Estrutura de Arquivos

```
sistema-vale-pallet/
├── index.html              # Arquivo principal do sistema
├── dicon_recibo.jpg        # Logo da empresa DICON
├── trindade_recibo.jpg     # Logo da empresa Trindade
├── README.md               # Este arquivo
├── GUIA_HOSPEDAGEM.md      # Guia para hospedar online
└── GUIA_CPANEL.md          # Guia para publicar no cPanel
```

## 🌐 Hospedagem

### Opções Gratuitas

1. **GitHub Pages** (Recomendado)
   - Veja o guia completo em `GUIA_HOSPEDAGEM.md`

2. **Netlify**
   - Drag & drop dos arquivos
   - Link automático gerado

3. **Vercel**
   - Upload direto ou via GitHub

### cPanel

Para publicar no cPanel, consulte o arquivo `GUIA_CPANEL.md`

## 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3 (com gradientes modernos)
- JavaScript (Vanilla)
- Canvas API (para conversão de imagens)

## 📝 Notas Importantes

- O arquivo principal deve se chamar `index.html` para funcionar corretamente
- As imagens devem estar na mesma pasta do arquivo HTML
- O sistema funciona 100% no navegador, sem necessidade de servidor
- Compatível com impressão em folha A4

## 👨‍💻 Desenvolvido por

**Daniel Rocha**

## 📄 Licença

Este projeto é de uso interno da empresa.

---

## 🔧 Personalização

Para adicionar novas empresas ou modificar configurações, edite o objeto `empresas` no JavaScript:

```javascript
const empresas = {
    dicon: {
        imagem: 'dicon_recibo.jpg',
        cnpj: '37.218.268/0001-04'
    },
    trindade: {
        imagem: 'trindade_recibo.jpg',
        cnpj: '48.724.616/0001-31'
    }
};
```

---

**Versão**: 1.0  
**Última atualização**: 2024

