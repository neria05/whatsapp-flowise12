<html>
<body>
<div><h1>WhatsApp Chatbot com Integração de API usando Flowise - Documentação</h1></div>
<div><p>Este é um exemplo de como criar um chatbot no WhatsApp usando a biblioteca <code>@open-wa/wa-automate</code> e integrá-lo com uma API externa usando chamadas CURL, com o auxílio da biblioteca Flowise. O chatbot receberá mensagens dos usuários, enviará uma pergunta para a API e responderá com a resposta obtida.</p></div>
<div><h2>Pré-requisitos</h2></div>
<div><p>Antes de começar, certifique-se de ter as seguintes dependências instaladas em seu ambiente de desenvolvimento:</p></div>
<div><ul><li>Node.js (versão 14 ou superior)</li><li>npm (gerenciador de pacotes do Node.js)</li></ul></div>
<div><h2>Instalação</h2></div>
<div><p>Siga as etapas abaixo para configurar o projeto:</p></div>
<div><ol><li>Clone o repositório do chatbot WhatsApp com integração Flowise para o seu ambiente de desenvolvimento:</li></ol></div>
<div><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><code class="!whitespace-pre hljs language-bash">git <span class="hljs-built_in">clone</span> https://github.com/Mpiffer/whatsapp-flowise.git
</code></div></div></pre></div>
<div><ol start="2"><li>Acesse o diretório do projeto:</li></ol></div>
<div><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><code class="!whitespace-pre hljs language-bash"><span class="hljs-built_in">cd</span> whatsapp-flowise
</code></div></div></pre></div>
<div><ol start="3"><li>Instale as dependências do projeto usando o npm:</li></ol></div>
<div><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><code class="!whitespace-pre hljs language-bash">npm install
</code></div></div></pre></div>
<div><h2>Configuração</h2></div>
<div><p>Antes de executar o chatbot, você precisa configurar algumas informações:</p></div>
<div><ol><li><p>Abra o arquivo <code>index.js</code> no diretório raiz do projeto.</p></li><li><p>No bloco de código <code>wa.create()</code>, ajuste as configurações de acordo com suas preferências. Aqui estão algumas opções importantes:</p></li></ol></div>
<div><ul><li><code>sessionId</code>: Identificador único para sua sessão do WhatsApp.</li><li><code>multiDevice</code>: Defina como <code>true</code> se desejar suportar vários dispositivos conectados à mesma conta do WhatsApp.</li><li><code>authTimeout</code>: Tempo máximo de espera (em segundos) para se conectar ao dispositivo de conta do WhatsApp.</li><li><code>blockCrashLogs</code>: Define se os logs de falhas devem ser bloqueados ou não.</li><li><code>disableSpins</code>: Define se os spins (círculos de carregamento) devem ser desativados ou não.</li><li><code>headless</code>: Define se o navegador será executado no modo headless (sem interface gráfica).</li><li><code>hostNotificationLang</code>: Define o idioma das notificações do host (exemplo: 'PT_BR' para português do Brasil).</li><li><code>logConsole</code>: Define se os logs do console serão exibidos ou não.</li><li><code>popup</code>: Define se os pop-ups serão exibidos durante a execução.</li><li><code>qrTimeout</code>: Tempo máximo de espera (em segundos) para escanear o código QR. Defina como 0 para esperar indefinidamente.</li></ul></div>
<div><ol start="3"><li><p>No bloco de código <code>client.onMessage()</code>, você pode personalizar as respostas do chatbot com base nas mensagens recebidas. O exemplo atual responde apenas com "👋 Olá!" quando recebe a mensagem "Hi". Você pode adicionar lógica adicional para processar diferentes mensagens e chamar a API conforme necessário.</p></li><li><p>No bloco de código <code>axios.post()</code>, ajuste a URL da API, a pergunta e o cabeçalho de autorização. Substitua <code>http://192.168.15.8:3000/api/v1/prediction/2f3522c3-1e9f-4f2e-a411-f34303e98cd2</code> pela URL correta da sua API. Certifique-se de fornecer a pergunta no formato adequado para a API.</p></li></ol></div>
<div><h2>Execução</h2></div>
<div><p>Após configurar o projeto, você pode executar o chatbot com o seguinte comando:</p></div>
<div><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><code class="!whitespace-pre hljs language-bash">node index.js
</code></div></div></pre></div>
<div><p>Lembre-se de fornecer suas próprias configurações e adaptar o código conforme necessário para atender aos requisitos específicos do seu projeto.</p></div>
</body>
</html>
