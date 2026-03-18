# 📱 Desafio POO — Sistema de Celulares

![C#](https://img.shields.io/badge/C%23-239120?style=flat&logo=c-sharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![DIO](https://img.shields.io/badge/DIO-Trilha_.NET-512BD4?style=flat)

Desafio de projeto desenvolvido como parte da **Trilha .NET** da [Digital Innovation One (DIO)](https://www.dio.me/), módulo de **Programação Orientada a Objetos**. O objetivo é modelar um sistema de celulares aplicando os quatro pilares da POO em C#: **abstração, encapsulamento, herança e polimorfismo**.

---

## 🧠 Sobre o Desafio

Você foi designado para modelar um sistema que trabalha com celulares. Para isso, deve criar uma **abstração da classe `Smartphone`** e permitir que diferentes marcas — **Nokia** e **iPhone** — tenham seus próprios comportamentos, promovendo reutilização de código através de herança e polimorfismo.

---

## 🏗️ Arquitetura de Classes

```
Smartphone (classe abstrata)
├── Nokia   (classe concreta — herda de Smartphone)
└── Iphone  (classe concreta — herda de Smartphone)
```

### Classe abstrata `Smartphone`

Contém as propriedades e comportamentos comuns a qualquer celular:

| Membro | Tipo | Descrição |
|---|---|---|
| `Numero` | Propriedade | Número do aparelho |
| `Modelo` | Propriedade | Modelo do celular |
| `IMEI` | Propriedade | Identificador único do aparelho |
| `Memoria` | Propriedade | Capacidade de memória |
| `Ligar()` | Método | Simula uma chamada |
| `ReceberLigacao()` | Método | Simula o recebimento de chamada |
| `InstalarAplicativo()` | Método **abstrato** | Comportamento específico de cada marca |

### Classes derivadas

| Classe | Comportamento de `InstalarAplicativo()` |
|---|---|
| `Nokia` | Instala via sistema Nokia/Windows |
| `Iphone` | Instala via App Store |

---

## 📌 Regras do Desafio

- A classe `Smartphone` **deve ser abstrata** — não pode ser instanciada diretamente
- `Nokia` e `Iphone` devem **obrigatoriamente herdar** de `Smartphone`
- O método `InstalarAplicativo()` deve ser **sobrescrito** em cada classe filha com comportamento distinto

---

## 🗂️ Estrutura do Projeto

```
trilha-net-poo-desafio/
├── Models/
│   ├── Smartphone.cs       # Classe abstrata base
│   ├── Nokia.cs            # Classe derivada Nokia
│   └── Iphone.cs           # Classe derivada Iphone
├── Imagens/                # Prints do resultado esperado
├── Program.cs              # Ponto de entrada — instancia e testa as classes
├── DesafioPOO.csproj
├── trilha-net-poo-desafio.sln
└── README.md
```

---

## 🚀 Como Executar

### Pré-requisitos

- [.NET SDK 6+](https://dotnet.microsoft.com/download)
- Visual Studio 2022 ou VS Code

### Passo a passo

**1. Clone o repositório**
```bash
git clone https://github.com/GuiMRDS/trilha-net-poo-desafio.git
cd trilha-net-poo-desafio
```

**2. Execute**
```bash
dotnet run
```

> Ou abra o arquivo `trilha-net-poo-desafio.sln` no Visual Studio e pressione `F5`.

---

## 🖥️ Exemplo de Saída

```
Ligando para o número 11999999999...
Recebendo ligação...
Instalando o aplicativo no Nokia via sistema Nokia
Instalando o aplicativo no Iphone via App Store
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| C# | Linguagem principal de desenvolvimento |
| .NET | Plataforma de execução |
| Visual Studio | IDE utilizada |
| Git / GitHub | Versionamento de código |

---

## 📚 Conceitos Praticados

| Pilar POO | Aplicação |
|---|---|
| **Abstração** | Classe `Smartphone` abstrata modela o conceito de celular sem instância direta |
| **Encapsulamento** | Propriedades com modificadores de acesso controlados |
| **Herança** | `Nokia` e `Iphone` herdam estrutura e comportamentos de `Smartphone` |
| **Polimorfismo** | `InstalarAplicativo()` tem comportamentos distintos em cada classe filha |

---

## 🎓 Contexto Acadêmico

> Projeto desenvolvido como desafio da **Trilha .NET** da **Digital Innovation One (DIO)**, módulo de Programação Orientada a Objetos.
>
> Fork do repositório original: [digitalinnovationone/trilha-net-poo-desafio](https://github.com/digitalinnovationone/trilha-net-poo-desafio)

---

## 👨‍💻 Autor

**Guilherme Marinho**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-guilherme--marinho04-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/guilherme-marinho04/)
[![GitHub](https://img.shields.io/badge/GitHub-GuiMRDS-black?style=flat&logo=github)](https://github.com/GuiMRDS)
[![Email](https://img.shields.io/badge/Email-guimars22%40gmail.com-red?style=flat&logo=gmail)](mailto:guimars22@gmail.com)

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte de um desafio da DIO.
