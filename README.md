# Projeto QR Code

Projeto desenvolvido no bootcamp da DIO com foco em JavaScript e Node.js. A aplicação funciona como um kit de utilidades para e-commerce, permitindo gerar QR Codes e senhas diretamente pelo terminal.

## Sobre o projeto

A proposta deste projeto é criar uma ferramenta simples, prática e interativa para resolver necessidades comuns do dia a dia: transformar textos ou links em QR Code e gerar senhas configuráveis.

Mesmo sendo uma aplicação de terminal, o projeto trabalha conceitos importantes como organização de arquivos, uso de bibliotecas externas, variáveis de ambiente e separação de responsabilidades no código.

## Funcionalidades

- Gerar QR Code a partir de texto ou link
- Exibir o QR Code no terminal
- Gerar senhas automaticamente
- Configurar tipos de caracteres usados na senha
- Definir tamanho da senha por variável de ambiente
- Escolher a funcionalidade por menu interativo

## Tecnologias utilizadas

- Node.js
- JavaScript (ES Modules)
- prompt
- chalk
- qrcode-terminal

## Estrutura de pastas

```text
projeto-qrcode/
├── .env
├── .gitignore
├── package.json
├── package-lock.json
├── README.md
└── src/
    ├── index.js
    ├── prompts-schema/
    │   ├── prompt-schema-main.js
    │   └── prompt-schema-qrcode.js
    └── services/
        ├── password/
        │   ├── create.js
        │   ├── handle.js
        │   └── utils/
        │       └── permitted-characters.js
        └── qr-code/
            ├── create.js
            └── handle.js
```

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/kevink16-1/PROJETO-QRCODE.git
```

2. Entre na pasta do projeto:

```bash
cd PROJETO-QRCODE
```

3. Instale as dependências:

```bash
npm install
```

4. Crie o arquivo `.env` com base no exemplo:

```bash
cp .env.example .env
```

No Windows PowerShell, use:

```powershell
Copy-Item .env.example .env
```

5. Execute o projeto:

```bash
npm run start
```

## Configuração da senha

O arquivo `.env` controla como a senha será gerada:

```env
UPPERCASE_LETTERS=false
LOWERCASE_LETTERS=false
NUMBERS=true
SPECIAL_CHARACTERS=true
PASSWORD_LENGTH=12
```

Você pode alterar esses valores para permitir letras maiúsculas, letras minúsculas, números, caracteres especiais e definir o tamanho final da senha.

## Aprendizados

Durante o desenvolvimento, foram praticados:

- criação de aplicações CLI com Node.js
- uso de pacotes externos
- leitura de variáveis de ambiente
- organização de código em serviços
- separação entre entrada, processamento e saída
- aplicação de lógica em um cenário real

---

Projeto desenvolvido para fins de estudo no bootcamp da DIO.
