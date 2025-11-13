<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootcamp Helper - Extensão Chrome MV3</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            color: white;
            padding: 60px 20px;
        }

        header h1 {
            font-size: 48px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        header p {
            font-size: 18px;
            opacity: 0.95;
        }

        .main-content {
            background: white;
            border-radius: 12px;
            padding: 40px;
            margin: 40px 0;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
        }

        section {
            margin-bottom: 40px;
        }

        section h2 {
            color: #667eea;
            font-size: 28px;
            margin-bottom: 20px;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
        }

        section h3 {
            color: #764ba2;
            font-size: 20px;
            margin-top: 20px;
            margin-bottom: 10px;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .feature-card {
            background: #f9f9f9;
            border-left: 4px solid #667eea;
            padding: 20px;
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.2);
        }

        .feature-card h4 {
            color: #667eea;
            margin-bottom: 10px;
        }

        .steps {
            background: #f0f0f0;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
        }

        .step {
            display: flex;
            margin-bottom: 15px;
            align-items: flex-start;
        }

        .step-number {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 15px;
            flex-shrink: 0;
        }

        .step-content {
            flex: 1;
        }

        .step-content strong {
            color: #667eea;
        }

        .permissions-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        .permissions-table th,
        .permissions-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }

        .permissions-table th {
            background: #f0f0f0;
            color: #667eea;
            font-weight: 600;
        }

        .permissions-table tr:hover {
            background: #f9f9f9;
        }

        .download-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            border-radius: 12px;
            text-align: center;
            margin: 40px 0;
        }

        .download-section h2 {
            color: white;
            border-bottom-color: white;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            margin: 10px;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .btn-primary {
            background: white;
            color: #667eea;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: #667eea;
        }

        .code-block {
            background: #2d2d2d;
            color: #f8f8f2;
            padding: 15px;
            border-radius: 6px;
            overflow-x: auto;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            font-size: 13px;
        }

        .code-block code {
            display: block;
        }

        footer {
            text-align: center;
            padding: 30px 20px;
            color: white;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            margin-top: 40px;
        }

        footer p {
            margin: 5px 0;
        }

        .badge {
            display: inline-block;
            background: #667eea;
            color: white;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin: 5px 5px 5px 0;
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 32px;
            }

            .main-content {
                padding: 20px;
            }

            section h2 {
                font-size: 22px;
            }

            .feature-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>🚀 Bootcamp Helper</h1>
        <p>Extensão Chrome com Manifest V3 - Projeto Bootcamp II</p>
    </header>

    <div class="container">
        <div class="main-content">
            <!-- Visão Geral -->
            <section>
                <h2>📋 Visão Geral</h2>
                <p>
                    O <strong>Bootcamp Helper</strong> é uma extensão de navegador desenvolvida como projeto educacional para demonstrar as melhores práticas de desenvolvimento de extensões Chrome usando o padrão <strong>Manifest V3</strong>.
                </p>
                <p style="margin-top: 15px;">
                    A extensão implementa funcionalidades essenciais incluindo comunicação entre popup e service worker, armazenamento local de dados, e manipulação do DOM através de content scripts.
                </p>
            </section>

            <!-- Funcionalidades -->
            <section>
                <h2>✨ Funcionalidades Principais</h2>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>💬 Comunicação Bidirecional</h4>
                        <p>Popup envia mensagens PING para o Service Worker e recebe respostas em tempo real com status de atividade.</p>
                    </div>
                    <div class="feature-card">
                        <h4>💾 Armazenamento Local</h4>
                        <p>Registra data de instalação e contagem de PINGs usando chrome.storage.local para persistência de dados.</p>
                    </div>
                    <div class="feature-card">
                        <h4>🎨 Manipulação do DOM</h4>
                        <p>Content Script destaca links e títulos em páginas específicas, injetando um badge de status visual.</p>
                    </div>
                    <div class="feature-card">
                        <h4>🔒 Permissões Mínimas</h4>
                        <p>Segue o princípio do menor privilégio, solicitando apenas permissões estritamente necessárias.</p>
                    </div>
                </div>
            </section>

            <!-- Instalação -->
            <section>
                <h2>🛠️ Instalação Manual</h2>
                <p>Siga os passos abaixo para instalar a extensão em modo desenvolvedor:</p>
                
                <div class="steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-content">
                            <strong>Abra o Chrome</strong> e navegue para <code>chrome://extensions</code>
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-content">
                            <strong>Ative o Modo Desenvolvedor</strong> clicando na chave no canto superior direito
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-content">
                            <strong>Clique em "Carregar sem compactação"</strong> (Load unpacked)
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-content">
                            <strong>Selecione a pasta</strong> da extensão no seu computador
                        </div>
                    </div>
                    <div class="step">
                        <div class="step-number">5</div>
                        <div class="step-content">
                            <strong>Pronto!</strong> O ícone da extensão aparecerá na barra de ferramentas
                        </div>
                    </div>
                </div>
            </section>

            <!-- Estrutura do Projeto -->
            <section>
                <h2>📁 Estrutura do Projeto</h2>
                <div class="code-block"><code>bootcamp2-chrome-ext/
├─ src/
│  ├─ popup/
│  │  ├─ popup.html
│  │  ├─ popup.js
│  │  └─ popup.css
│  ├─ background/
│  │  └─ service-worker.js
│  ├─ content/
│  │  └─ content.js
│  └─ styles/
├─ icons/
│  ├─ icon16.png
│  ├─ icon32.png
│  ├─ icon48.png
│  └─ icon128.png
├─ docs/
│  └─ index.html
├─ manifest.json
├─ README.md
├─ LICENSE
└─ .gitignore</code></div>
            </section>

            <!-- Permissões -->
            <section>
                <h2>🔐 Permissões Utilizadas</h2>
                <p>A extensão segue o princípio do menor privilégio:</p>
                <table class="permissions-table">
                    <thead>
                        <tr>
                            <th>Permissão</th>
                            <th>Propósito</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>storage</code></td>
                            <td>Armazenar data de instalação e contagem de PINGs</td>
                        </tr>
                        <tr>
                            <td><code>tabs</code></td>
                            <td>Interagir com abas do navegador</td>
                        </tr>
                        <tr>
                            <td><code>host_permissions</code></td>
                            <td>Injetar content script em https://developer.chrome.com/*</td>
                        </tr>
                    </tbody>
                </table>
            </section>

            <!-- Compatibilidade -->
            <section>
                <h2>🌐 Compatibilidade</h2>
                <p>
                    A extensão é compatível com:
                </p>
                <div style="margin: 15px 0;">
                    <span class="badge">Chrome 114+</span>
                    <span class="badge">Edge 114+</span>
                    <span class="badge">Brave</span>
                    <span class="badge">Opera</span>
                    <span class="badge">Vivaldi</span>
                </div>
                <p style="margin-top: 15px;">
                    Todos os navegadores baseados em Chromium com suporte a Manifest V3.
                </p>
            </section>

            <!-- Tecnologias -->
            <section>
                <h2>🛠️ Tecnologias Utilizadas</h2>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h4>HTML5</h4>
                        <p>Estrutura semântica para popup e landing page</p>
                    </div>
                    <div class="feature-card">
                        <h4>CSS3</h4>
                        <p>Estilos modernos com gradientes e animações</p>
                    </div>
                    <div class="feature-card">
                        <h4>JavaScript (ES6+)</h4>
                        <p>Lógica assíncrona com async/await</p>
                    </div>
                    <div class="feature-card">
                        <h4>Chrome APIs</h4>
                        <p>runtime, storage, tabs, messaging</p>
                    </div>
                </div>
            </section>

            <!-- Download -->
            <div class="download-section">
                <h2>⬇️ Download e Instalação</h2>
                <p style="margin-bottom: 20px;">
                    Escolha uma das opções abaixo para obter a extensão:
                </p>
                <a href="https://github.com/seu-usuario/bootcamp2-chrome-ext/releases" class="btn btn-primary">
                    📦 Download (ZIP)
                </a>
                <a href="https://github.com/seu-usuario/bootcamp2-chrome-ext" class="btn btn-secondary">
                    🔗 Ver no GitHub
                </a>
            </div>

            <!-- Uso -->
            <section>
                <h2>📖 Como Usar</h2>
                <h3>Abrindo o Popup</h3>
                <p>
                    Clique no ícone da extensão na barra de ferramentas do Chrome para abrir o popup interativo.
                </p>
                
                <h3>Verificar Status</h3>
                <p>
                    Clique no botão "Verificar Background" para enviar um PING ao Service Worker. Você receberá uma resposta com o horário atual.
                </p>
                
                <h3>Ver Estatísticas</h3>
                <p>
                    Clique em "Ver Estatísticas" para visualizar a data de instalação e o total de PINGs enviados.
                </p>
                
                <h3>Content Script</h3>
                <p>
                    Visite <code>https://developer.chrome.com</code> para ver o Content Script em ação. Links serão destacados e um badge aparecerá no canto inferior direito.
                </p>
            </section>

            <!-- Desenvolvimento -->
            <section>
                <h2>👨‍💻 Desenvolvimento</h2>
                <h3>Estrutura de Código</h3>
                <p>
                    Todo o código inclui comentários essenciais explicando a funcionalidade. Os arquivos estão organizados de forma clara e modular.
                </p>
                
                <h3>Commits no Git</h3>
                <p>
                    O repositório contém commits frequentes e com mensagens descritivas, facilitando o acompanhamento do desenvolvimento.
                </p>
                
                <h3>Padrões de Código</h3>
                <ul style="margin-left: 20px; margin-top: 10px;">
                    <li>Sem dependências externas (vanilla JavaScript)</li>
                    <li>Sem uso de eval() ou código dinâmico</li>
                    <li>Content Security Policy (CSP) padrão do MV3</li>
                    <li>Tratamento adequado de erros e exceções</li>
                </ul>
            </section>

            <!-- Licença -->
            <section>
                <h2>📄 Licença</h2>
                <p>
                    Este projeto está licenciado sob a Licença MIT. Você é livre para usar, modificar e distribuir este código, desde que inclua a atribuição original.
                </p>
            </section>

            <!-- Suporte -->
            <section>
                <h2>🤝 Suporte e Contribuições</h2>
                <p>
                    Este é um projeto educacional. Se encontrar problemas ou tiver sugestões, abra uma issue no repositório GitHub.
                </p>
                <p style="margin-top: 15px;">
                    Contribuições são bem-vindas! Faça um fork, crie uma branch com suas mudanças e envie um pull request.
                </p>
            </section>
        </div>

        <footer>
            <p>🚀 Bootcamp Helper - Extensão Chrome (Manifest V3)</p>
            <p>Desenvolvido como projeto educacional do Bootcamp II</p>
            <p>&copy; 2025 Manus AI. Licenciado sob MIT.</p>
        </footer>
    </div>
</body>
</html>
