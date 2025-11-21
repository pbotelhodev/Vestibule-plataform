# 📚 Vestibule Platform

> Plataforma educacional completa para gestão e aplicação de simulados com controle de acesso hierárquico.

![Status do Projeto](https://img.shields.io/badge/STATUS-CONCLUÍDO-brightgreen?style=for-the-badge)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

---

## 💻 Sobre o Projeto

O **Vestibule** é uma aplicação web **Single Page Application (SPA)** desenvolvida para simular o ambiente de provas escolares. 

O grande diferencial técnico deste projeto é sua **Arquitetura de Renderização Condicional (RBAC)**: o sistema utiliza uma única base de código que adapta dinamicamente a interface, as rotas e as permissões de dados dependendo do nível do usuário logado (**Administrador**, **Professor** ou **Aluno**).

### 🏆 Principais Destaques
- **Gestão de Estado Global:** Controle de sessão e persistência via LocalStorage.
- **Lógica de Notas Dinâmica:** Feedback visual de desempenho (Cores baseadas na nota: Atenção/Bom/Excelente).
- **Onboarding Automatizado:** Geração automática de credenciais e IDs únicos para novos usuários.

---

## 🔐 Acesso de Demonstração (Auto-Seed)

O projeto conta com um sistema de **"Auto-Seed"**. Ao abrir a aplicação pela primeira vez, o banco de dados local é populado automaticamente.

Utilize as credenciais abaixo para acessar o nível máximo (Admin) e criar outros usuários para teste:

| Perfil | ID | Senha |
| :--- | :--- | :--- |
| **Administrador** | `999` | `userPadrao*` |

### 🧪 Roteiro de Teste Recomendado:
1. Faça login como **Admin**.
2. Vá em "Cadastrar" e crie um usuário **Professor** (note a senha gerada automaticamente: `Vestibule` + `ID`).
3. Crie um usuário **Aluno**.
4. Faça logout e entre com as novas contas para ver a interface se transformar.

---

## ⚙️ Funcionalidades Técnicas

### 1. Sistema de Autenticação & Segurança
- Login com validação de credenciais criptografadas (simulação).
- Geração de IDs não-sequenciais aleatórios para segurança.
- Senhas padrão dinâmicas para facilitar o onboarding (`Vestibule` + `ID`).

### 2. Controle de Acesso (RBAC)
- **Admin:** CRUD completo de Usuários, Simulados e Matérias. Visualização de todas as notas.
- **Professor:** Criação de simulados apenas para suas matérias. Visualização de notas filtradas.
- **Aluno:** Acesso "Read-only" aos simulados disponíveis. Histórico de notas próprias.

### 3. Engine de Simulado
- Validação de formulários (limite de caracteres).
- Algoritmo de correção automática (comparação de gabarito).
- Cálculo de média e estilização condicional de tags (Amarelo < 7, Azul < 9, Verde > 9).

---

## 🛠️ Tecnologias Utilizadas

- **Core:** ReactJS + Vite
- **Estilização:** CSS3 Moderno (Variáveis e Flexbox/Grid)
- **Linguagem:** JavaScript (ES6+)
- **Persistência:** LocalStorage API (Simulando Banco de Dados NoSQL)
- **Ícones:** React Icons

---

## 🚀 Como rodar o projeto localmente

```bash
# 1. Clone o repositório
$ git clone [https://github.com/pbotelhodev/vestibule-platform.git](https://github.com/pbotelhodev/vestibule-platform.git)

# 2. Acesse a pasta
$ cd vestibule-platform

# 3. Instale as dependências
$ npm install

# 4. Execute o servidor de desenvolvimento
$ npm run dev

```

📝 Autor
Feito com ❤️ por Pedro Botelho
