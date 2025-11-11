# 🚀 Node-RED + BrazilAPI  
### Teste Técnico — Desenvolvido por **Luan Henrique Guimarães Januário de Oliveira**

Este projeto foi desenvolvido como parte de um teste técnico.  
A aplicação utiliza **Node-RED** integrado com a **BrazilAPI**, permitindo:

✅ Listar corretoras registradas na CVM  
✅ Buscar informações de endereço a partir de um CEP  
✅ Salvar o histórico de buscas em banco SQLite  
✅ Página inicial feita em **React** dentro do Node-RED

---

## 🛠 Tecnologias Utilizadas

| Tecnologia | Uso no projeto |
|------------|----------------|
| **Node-RED** | Criação dos fluxos e das APIs (HTTP) |
| **BrazilAPI** | Fonte de dados para CEP e corretoras |
| **React (CDN)** | Interface da página Home |
| **SQLite** | Armazenamento do histórico de CEP |
| **HTML/CSS** | Páginas estilizadas (sem frameworks externos no fluxo principal) |

---

## 🌐 Endpoints disponíveis

| Funcionalidade | URL | Método |
|----------------|-----|--------|
| Página inicial (React) | `http://localhost:1880/home` | GET |
| Catálogo de Corretoras (BrazilAPI) | `http://localhost:1880/corretoras` | GET |
| Buscador de CEP (via input) | `http://localhost:1880/cep` | GET |
| Busca de CEP via rota (`:cep`) | `http://localhost:1880/busca-cep/30130010` | GET |
| Histórico dos CEP pesquisados (SQLite) | `http://localhost:1880/historico` | GET |

---

## 📸 Screenshots

> Imagens armazenadas na pasta `/screenshots` do repositório.

| Página | Print |
|--------|-------|
| Home com React | `/screenshots/home.png` |
| Catálogo de Corretoras | `/screenshots/corretoras.png` |
| Busca CEP | `/screenshots/busca-cep.png` |
| Histórico (SQLite) | `/screenshots/historico.png` |

---

## 💾 Estrutura do Projeto

📦 **node-red-brazilapi**  
├── 📁 **screenshots**  
│   ├── 🏠 *home.png* — Tela inicial  
│   ├── 📈 *corretoras.png* — Catálogo de corretoras  
│   ├── 📍 *busca-cep.png* — Buscador de CEP  
│   └── 🗂️ *historico.png* — Histórico de consultas de CEP  
├── 🗂️ **flows.json** — Fluxo exportado do Node-RED  
└── 📄 **README.md** — Documentação do projeto  


---

## 🖼️ Screenshots

| 🏠 Home | 📈 Corretoras |
|--------|-------------|
| <img src="screenshots/home.png" width="430"/> | <img src="screenshots/corretoras.png" width="430"/> |

| 📍 Busca CEP | 🗂️ Histórico |
|-------------|--------------|
| <img src="screenshots/busca-cep.png" width="430"/> | <img src="screenshots/historico.png" width="430"/> |



---

## ▶️ Como executar o projeto

1️⃣ Instalar Node-RED  
```bash
npm install -g node-red

2️⃣ Iniciar o Node-RED
node-red

3️⃣ Acessar no navegador:

➡️ http://localhost:1880

4️⃣ Importar o fluxo:

No Node-RED, clique em Menu > Import > Select a file
Selecione o arquivo flows.json deste repositório
Banco SQLite é criado automaticamente na primeira busca de CEP.

