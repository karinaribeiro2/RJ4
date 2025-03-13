# 📦 Módulo ReiDoCadastro

Bem-vindo ao **ReiDoCadastro**, um módulo JavaScript desenvolvido em ES6 para gerenciamento de cadastros de empresas e clientes! 🎉

## 🚀 Funcionalidades

- Cadastro de **Clientes** com nome, CPF, endereço e telefones 📇
- Cadastro de **Empresas** com razão social, nome fantasia, CNPJ, endereço e clientes 🏢
- Cadastro de **Endereços** e **Telefones** associados aos clientes e empresas 📍📞
- Métodos para recuperar informações formatadas em **caixa alta** e **caixa baixa** 🔤
- Método para exibir os detalhes da empresa e seus clientes de forma organizada 📜

## 🛠 Estrutura do Projeto

```
📂 models/
   ├── ReiDoCadastro.js  # Definição das classes Cliente, Empresa, Endereço e Telefone
   ├── Telefone.js       # Classe Telefone
   ├── Endereco.js       # Classe Endereco
   ├── Empresa.js        # Classe Empresa
   ├── Cliente.js        # Classe Cliente
📂 tests/
   ├── test.js           # Arquivo de testes
📜 README.md             # Documentação do projeto
```

## 📜 Exemplo de Uso

```javascript
import { Cliente } from "./models/ReiDoCadastro.js";
import { Empresa } from "./models/ReiDoCadastro.js";
import { Telefone } from "./models/ReiDoCadastro.js";
import { Endereco } from "./models/ReiDoCadastro.js";

// Criando um endereço
const enderecoEmpresa = new Endereco("SP", "São Paulo", "Av. Paulista", 123);
const empresa = new Empresa("ABC LTDA", "Mercado Online", "12345678000199", enderecoEmpresa);

// Criando clientes
const enderecoCliente1 = new Endereco("RJ", "Rio de Janeiro", "Rua Copacabana", 456);
const cliente1 = new Cliente("Carlos", "123.456.789-00", enderecoCliente1);
cliente1.telefones.add(new Telefone(21, "777777777"));
cliente1.telefones.add(new Telefone(21, "999999999"));

empresa.clientes.add(cliente1);

console.log(empresa.detalhe());
```

## 🔧 Como Executar

1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/ReiDoCadastro.git
   ```
2. Navegue até a pasta do projeto:
   ```sh
   cd ReiDoCadastro
   ```
3. Execute os testes com Node.js:
   ```sh
   node tests/test.js
   ```

## 💾 Histórico de Commits

- 🎉 Inicialização do repositório
- 🚀 Implementação das classes principais
- 🔥 Adição dos testes
- 📖 Atualização da documentação

## 📜 Licença

Este projeto está licenciado sob a **MIT License**. Sinta-se livre para usar e modificar! 😃

