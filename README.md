# 🏆 Bolão da Amizade - Copa 2026

Um Web App responsivo (Mobile-First) desenvolvido para gerenciar e visualizar estatísticas, rankings e palpites de um bolão de futebol da Copa do Mundo de 2026. 

Link do projeto modelo: 

https://bolao-da-amizade.netlify.app/

O diferencial deste projeto é a sua arquitetura *Serverless*: ele não possui um backend tradicional. O banco de dados é gerenciado integralmente através do **Google Sheets**, e a aplicação consome esses dados em tempo real utilizando requisições assíncronas (Fetch API).

## ✨ Funcionalidades Principais

*   📊 **Ranking Dinâmico:** Classificação atualizada em tempo real, com divisão em abas independentes para o "Grupo A" e "Grupo B".
*   🔮 **Probabilidade de Vitória (Chance de Ganhar):** Algoritmo matemático integrado que calcula e exibe a chance percentual de cada participante ser campeão, baseando-se na diferença de pontos para o líder e na quantidade de partidas restantes.
*   📱 **Design Mobile-First e Dark Mode:** Interface moderna, fluida e amigável para dispositivos móveis, construída inteiramente com **Tailwind CSS**.
*   🔍 **Histórico de Palpites (Modal):** Ao clicar em um participante, um modal interativo é aberto exibindo o histórico completo de palpites daquela pessoa (Fase de Grupos + Mata-Mata).
*   📈 **Gráficos e Estatísticas:** Dashboard visual contendo média de pontos da rodada, líder atual, progresso das partidas (ex: 72 de 88 finalizadas) e gráficos de barras interativos.
*   🔄 **Destaque Automático:** Identificação automática do usuário dono do aplicativo (variável customizável) para destacá-lo com cores diferentes no meio da tabela de classificação.

## 🛠️ Tecnologias Utilizadas

*   **HTML5**
*   **JavaScript (Vanilla / ES6+):** Lógica assíncrona (`async/await`), manipulação de DOM e tratativas de arrays/objetos.
*   **Tailwind CSS:** (via CDN) Para estilização rápida e design responsivo.
*   **Chart.js:** Biblioteca para a renderização dos gráficos de pontuação.
*   **Google Sheets / Google Visualization API:** Utilizado como banco de dados NoSQL/JSON para leitura da pontuação e gabarito.

## 🚀 Como Executar o Projeto

Como este projeto é um *Single Page Application* (SPA) estático, rodá-lo é extremamente simples. Não é necessário instalar dependências como Node.js ou rodar servidores de banco de dados.

1. **Clone o repositório:**
   ```bash
   git clone (https://github.com/luizfelizardo/bolao-copa-2026.git)

   ⚙️ Configuração do Banco de Dados (Google Sheets)
Para que o aplicativo funcione com suas próprias planilhas, certifique-se de:

Publicar sua planilha na web (Arquivo > Compartilhar > Publicar na web).

Substituir as constantes no início da tag <script> do arquivo index.html com os IDs das suas planilhas:

JavaScript
const ID_ANTIGA = 'ID_DA_SUA_PLANILHA_FASE_DE_GRUPOS';
const ID_NOVA = 'ID_DA_SUA_PLANILHA_MATA_MATA';
const MAX_PONTOS_POR_PARTIDA = 5; // Defina os pontos ganhos por acerto exato
📄 Licença
Este projeto é de uso livre para estudos e entretenimento. Sinta-se à vontade para realizar um fork e adaptar o bolão para o seu grupo de amigos!
