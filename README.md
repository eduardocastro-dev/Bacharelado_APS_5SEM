# 📡 TCPServidor e TCPCliente: Compartilhamento de Arquivos via TCP

Aplicação em **C#** que implementa um servidor e um cliente **TCP** para comunicação em tempo real e compartilhamento de imagens entre múltiplos clientes conectados simultaneamente.

## 📑 Sumário

- [Sobre o projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Arquitetura](#-arquitetura)
- [Tecnologias utilizadas](#-tecnologias-utilizadas)
- [Pré-requisitos](#-pré-requisitos)
- [Como executar](#-como-executar)
- [Observações](#-observações)
- [Contribuindo](#-contribuindo)
- [Licença](#-licença)
- [Autor](#-autor)

## 📖 Sobre o projeto

O projeto implementa um chat cliente-servidor baseado em sockets TCP, permitindo que múltiplos clientes se conectem simultaneamente a um servidor central para trocar mensagens de texto e compartilhar imagens em tempo real.

## ✨ Funcionalidades

### Servidor

- Iniciar e parar a escuta por conexões de clientes.
- Aceitar novas conexões de clientes.
- Gerenciar clientes conectados (armazenar informações como nome, cor de exibição e socket).
- Receber e processar mensagens de texto e arquivos de clientes, reenviando para os demais clientes conectados.
- Enviar mensagens de texto para todos os clientes conectados (broadcast).
- Compartilhar imagens: receber imagens de clientes e replicar para os outros clientes.

### Cliente

- Conectar a um servidor TCP.
- Enviar nome e cor de exibição.
- Enviar mensagens de texto para o servidor.
- Compartilhar imagens com o servidor.
- Receber mensagens de texto do servidor.
- Receber imagens do servidor e salvá-las em uma pasta local.
- Desconectar do servidor.

## 🏗 Arquitetura

- A comunicação TCP é implementada utilizando a biblioteca `System.Net.Sockets`.
- O **servidor** é multithread, permitindo lidar com múltiplos clientes simultaneamente.
- O **cliente** é assíncrono, garantindo uma interface responsiva durante o envio e recebimento de dados.

## 🛠 Tecnologias utilizadas

- [C#](https://learn.microsoft.com/pt-br/dotnet/csharp/)
- [.NET Framework](https://dotnet.microsoft.com/) 4.7.2 ou superior
- `System.Net.Sockets` (comunicação TCP)

## ✅ Pré-requisitos

Antes de começar, você precisa ter instalado:

- [Visual Studio 2019](https://visualstudio.microsoft.com/) ou superior
- [.NET Framework](https://dotnet.microsoft.com/en-us/download/dotnet-framework) 4.7.2 ou superior

## 🚀 Como executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/eduardocastro-dev/Bacharelado_APS_5SEM.git
   ```
2. Abra a solução (`.sln`) no Visual Studio.
3. Compile os projetos do servidor (`TCPServidor`) e do cliente (`TCPCliente`).
4. Execute o projeto **TCPServidor** para iniciar a escuta por conexões.
5. Execute o projeto **TCPCliente** e configure as informações necessárias:
   - Nome de exibição
   - Endereço IP e porta do servidor
   - Pasta local para salvar as imagens recebidas
6. Conecte-se ao servidor pela interface do cliente.
7. Utilize o chat para enviar mensagens de texto e compartilhar imagens com os demais clientes conectados.

> 💡 **Dica:** para testar com múltiplos clientes na mesma máquina, basta executar várias instâncias do projeto **TCPCliente** e conectá-las ao mesmo servidor.

## 📝 Observações

- O projeto inclui tratamento de erros para garantir a robustez das aplicações.
- A documentação detalhada da implementação está disponível nos comentários dos arquivos de código-fonte.
- Este é um projeto **acadêmico**, com fins didáticos sobre comunicação via sockets TCP. Recursos adicionais — como autenticação, criptografia do tráfego e validação mais robusta de entradas — podem ser implementados para atender a requisitos de produção.

## 🤝 Contribuindo

Contribuições para este projeto são bem-vindas! Sinta-se à vontade para:

1. Fazer um fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/minha-feature`)
3. Commitar suas alterações (`git commit -m 'Adiciona minha feature'`)
4. Enviar um pull request

Você também pode abrir uma [issue](https://github.com/eduardocastro-dev/Bacharelado_APS_5SEM/issues) para relatar bugs ou sugerir melhorias.

## 📄 Licença

Este projeto está licenciado sob a licença [MIT](LICENSE).

## 👤 Autor

Desenvolvido por [**Eduardo Castro**](https://github.com/eduardocastro-dev) como parte das atividades do curso de Bacharelado.
