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
```bash
git clone [https://github.com/FabioHenrique-Dev-Br/Elei-o-API.git](https://github.com/FabioHenrique-Dev-Br/Elei-o-API.git)
