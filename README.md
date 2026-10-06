# 🗳️ Painel Presidencial - Consulta API REST do TSE

Aplicação web interativa desenvolvida em HTML, Tailwind CSS e JavaScript puro para realizar a consulta e exibição em tempo real dos candidatos à Presidência da República utilizando os endpoints públicos da API do **DivulgaCandContas** do Tribunal Superior Eleitoral (TSE).

---

## 🚀 Funcionalidades

- **Seleção de Pleito Eleitoral:** Alternância dinâmica entre eleições federais (2026, 2022 e 2018).
- **Busca e Filtro Dinâmico:** Pesquisa em tempo real por nome na urna, número do candidato ou sigla do partido.
- **Exibição em Grid:** Apresentação em cards com foto, número, partido, coligação e situação da candidatura (Deferido, etc.).
- **Modal de Detalhes:** Visualização expandida das informações do candidato selecionado.
- **Tratamento de Fallback Visual:** Geração automática de avatares com iniciais do candidato em caso de restrições de mídia no navegador.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Estrutura e marcação semântica.
- **Tailwind CSS (CDN):** Estilização responsiva e moderna.
- **JavaScript (ES6+):** Manipulação do DOM, manipulação de eventos e consumo de APIs via `fetch`.
- **Live Server (VS Code):** Servidor de desenvolvimento local.

---

## ⚙️ Funcionamento da API do TSE

A aplicação realiza chamadas do tipo `GET` diretamente para os serviços REST oficiais do TSE:

- **Listagem de Candidatos:**  
  `https://divulgacandcontas.tse.jus.br/divulga/rest/v1/candidatura/listar/{ANO}/BR/{CODIGO_ELEICAO}/1/candidatos`
- **Fotos Oficiais:**  
  `https://divulgacandcontas.tse.jus.br/divulga/rest/v1/candidatura/buscar/foto/{cand.id}`

---

## 🔓 Como Executar e Resolver Restrições de CORS no Ambiente Local

Os servidores de arquivos e dados do Tribunal Superior Eleitoral possuem regras de segurança (CORS) que bloqueiam requisições diretas feitas por navegadores a partir de origens locais (`http://127.0.0.1:5500`).

Para rodar e testar o projeto no seu computador:

### 1. Clonar o Repositório
```bash git clone [https://github.com/FabioHenrique-Dev-Br/Elei-o-API.git](https://github.com/FabioHenrique-Dev-Br/Elei-o-API.git) ```

2. Abrir no VS Code
Abra a pasta do projeto no VS Code e inicie a execução através da extensão Live Server.

3. Ativar a Extensão de Navegador
Para permitir a passagem das requisições e a exibição dos dados do TSE no ambiente local:

Instale a extensão Allow CORS: Access-Control-Allow-Origin no seu navegador (Chrome ou Edge).

Clique no ícone da extensão no topo do navegador para ativá-la (o botão ficará ON / colorido).

Atualize a página do Live Server (F5).

🌐 Informações e Fontes Oficiais
Para consultar as diretrizes de candidaturas, regras eleitorais e os conjuntos de dados originais disponibilizados pela Justiça Eleitoral:

Para conferir relatórios, prestação de contas e a plataforma oficial de candidaturas, acesse o portal do DivulgaCandContas do TSE.

Para obter conjuntos de dados públicos e estatísticas de pleitos, acesse o Portal de Dados Abertos do TSE.

👨‍💻 Autor
Desenvolvido por Fábio Henrique

GitHub: FabioHenrique-Dev-Br
