<i data-lucide="battery" class="w-4 h-4 text-white rotate-0"></i>
            </div>
        </div>

        <!-- BARRA DE ENDEREÇO SAFARI (Simulação de Navegador Premium iOS) -->
        <div class="bg-[#1C1C1E] border-b border-zinc-800 px-4 py-2 flex items-center justify-between text-zinc-400 text-xs z-40">
            <div class="flex items-center space-x-3">
                <i data-lucide="a-large-small" class="w-4 h-4 cursor-pointer hover:text-white"></i>
            </div>
            <div onclick="openSafariShareSheet()" class="bg-[#2C2C2E] rounded-lg px-3 py-1 flex items-center justify-center space-x-1.5 w-2/3 max-w-[210px] mx-auto text-[11px] cursor-pointer hover:bg-zinc-700 transition">
                <i data-lucide="lock" class="w-3 h-3 text-picpay-green"></i>
                <span class="truncate text-zinc-200">715260091625.pages.dev</span>
            </div>
            <div class="flex items-center space-x-3">
                <i onclick="reloadApp()" data-lucide="rotate-cw" class="w-3.5 h-3.5 cursor-pointer hover:text-white transition"></i>
            </div>
        </div>

        <!-- CONTEÚDO PRINCIPAL DO APP PICPAY (Deslizável) -->
        <div id="app-screen" class="flex-1 bg-picpay-bg text-white overflow-y-auto no-scrollbar pb-36 relative">
            
            <!-- CABEÇALHO PICPAY -->
            <div class="p-4 flex items-center justify-between">
                <div class="flex items-center space-x-3">
                    <div class="relative cursor-pointer" onclick="openTouchID('admin')">
                        <img id="user-avatar" src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=200&auto=format&fit=crop" class="w-10 h-10 rounded-full border-2 border-picpay-green object-cover" alt="User">
                        <div class="absolute -bottom-1 -right-1 bg-picpay-green rounded-full p-0.5">
                            <i data-lucide="settings" class="w-3 h-3 text-black"></i>
                        </div>
                    </div>
                    <div>
                        <p class="text-xs text-picpay-textMuted font-medium">Olá,</p>
                        <h4 id="user-name-display" class="font-bold text-sm">Amanda Oliveira</h4>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <button onclick="toggleVisibility()" class="p-2 hover:bg-zinc-800 rounded-full transition">
                        <i id="eye-icon" data-lucide="eye" class="w-5 h-5 text-picpay-green"></i>
                    </button>
                    <button onclick="openTouchID('admin')" class="p-2 hover:bg-zinc-800 rounded-full transition">
                        <i data-lucide="sliders-horizontal" class="w-5 h-5 text-zinc-400"></i>
                    </button>
                </div>
            </div>

            <!-- CARTÃO DE SALDO PRINCIPAL -->
            <div class="mx-4 p-5 bg-picpay-card rounded-2xl border border-picpay-border shadow-md">
                <div class="flex items-center justify-between mb-2">
                    <span class="text-xs text-picpay-textMuted font-medium">Saldo PicPay</span>
                    <span class="bg-picpay-lightGreen text-picpay-darkGreen text-[10px] font-bold px-2 py-0.5 rounded-full">Rendimento 102% CDI</span>
                </div>
                
                <div class="mb-4">
                    <h2 id="balance-value" class="text-2xl font-extrabold tracking-tight">R$ 1.542,80</h2>
                    <p id="balance-hidden" class="text-2xl font-extrabold tracking-tight hidden">R$ ••••••</p>
                </div>

                <!-- RENDIMENTOS INTERNOS -->
                <div class="flex items-center justify-between pt-3 border-t border-zinc-800 text-xs text-zinc-400">
                    <div class="flex items-center space-x-1">
                        <i data-lucide="sparkles" class="w-3.5 h-3.5 text-yellow-500"></i>
                        <span>Cashback: <strong id="cashback-value" class="text-white">R$ 48,90</strong></span></div>
                    <span class="text-picpay-green flex items-center font-semibold cursor-pointer">Extrato <i data-lucide="chevron-right" class="w-3.5 h-3.5 ml-0.5"></i></span>
                </div>
            </div>

            <!-- CARROSSEL DE ATALHOS -->
            <div class="mt-6 px-4">
                <h3 class="text-xs font-bold text-zinc-400 uppercase tracking-wider mb-3">Sugestões para você</h3>
                <div class="grid grid-cols-4 gap-2">
                    <button onclick="openPixModal()" class="flex flex-col items-center p-3 bg-picpay-card rounded-xl border border-picpay-border hover:bg-zinc-800 transition active:scale-95">
                        <div class="w-10 h-10 bg-emerald-950/40 rounded-full flex items-center justify-center mb-1 text-picpay-green">
                            <i data-lucide="qr-code" class="w-5 h-5"></i>
                        </div>
                        <span class="text-[10px] text-center font-semibold">Fazer Pix</span>
                    </button>

                    <button onclick="simulatePushNotification('Notificação', 'Recebemos o seu depósito de R$ 500,00')" class="flex flex-col items-center p-3 bg-picpay-card rounded-xl border border-picpay-border hover:bg-zinc-800 transition active:scale-95">
                        <div class="w-10 h-10 bg-zinc-800/60 rounded-full flex items-center justify-center mb-1 text-zinc-200">
                            <i data-lucide="arrow-down-left" class="w-5 h-5"></i>
                        </div>
                        <span class="text-[10px] text-center font-semibold">Receber</span>
                    </button>

                    <button onclick="alertCustom('Funcionalidade de recarga de telemóvel integrada com a sua conta PicPay.')" class="flex flex-col items-center p-3 bg-picpay-card rounded-xl border border-picpay-border hover:bg-zinc-800 transition active:scale-95">
                        <div class="w-10 h-10 bg-zinc-800/60 rounded-full flex items-center justify-center mb-1 text-zinc-200">
                            <i data-lucide="smartphone" class="w-5 h-5"></i>
                        </div>
                        <span class="text-[10px] text-center font-semibold">Celular</span>
                    </button>

                    <button onclick="alertCustom('Cartão PicPay Card com cashback de até 1.2% disponível!')" class="flex flex-col items-center p-3 bg-picpay-card rounded-xl border border-picpay-border hover:bg-zinc-800 transition active:scale-95">
                        <div class="w-10 h-10 bg-zinc-800/60 rounded-full flex items-center justify-center mb-1 text-zinc-200">
                            <i data-lucide="credit-card" class="w-5 h-5"></i>
                        </div>
                        <span class="text-[10px] text-center font-semibold">Cartões</span>
                    </button>
                </div>
            </div>

            <!-- BANNER INFORMATIVO -->
            <div class="mx-4 mt-6 p-4 bg-gradient-to-r from-emerald-900 to-emerald-950 rounded-2xl border border-picpay-green/30 flex items-center justify-between">
                <div class="max-w-[70%]">
                    <span class="bg-picpay-green text-black font-extrabold text-[8px] uppercase px-1.5 py-0.5 rounded">Novidade</span>
                    <h4 class="font-bold text-xs mt-1.5 text-white">Guarde dinheiro nos Cofres PicPay</h4>
                    <p class="text-[10px] text-zinc-300 mt-0.5">Rendimento garantido de 102% do CDI desde o primeiro dia.</p>
                </div>
                <div class="w-12 h-12 bg-picpay-green/20 rounded-full flex items-center justify-center text-picpay-green">
                    <i data-lucide="piggy-bank" class="w-7 h-7"></i>
                </div>
            </div>

            <!-- HISTÓRICO DE TRANSAÇÕES -->
            <div class="mt-6 px-4">
                <div class="flex items-center justify-between mb-3">
                    <h3 class="text-xs font-bold text-zinc-400 uppercase tracking-wider">Atividade Recente</h3><button onclick="clearHistory()" class="text-xs text-red-500 font-semibold hover:underline">Limpar</button>
                </div>
                
                <div id="transactions-list" class="space-y-3">
                    <!-- Conteúdo gerado dinamicamente -->
                </div>
            </div>
        </div>

        <!-- BARRA DE NAVEGAÇÃO DO PICPAY -->
        <div class="absolute bottom-11 left-0 right-0 bg-zinc-950 border-t border-zinc-900 px-6 py-2 flex justify-between items-center z-40">
            <button onclick="switchTab('inicio')" class="flex flex-col items-center space-y-0.5 text-picpay-green transition">
                <i data-lucide="home" class="w-5 h-5"></i>
                <span class="text-[9px] font-bold">Início</span>
            </button>
            <button onclick="openPixModal()" class="flex flex-col items-center space-y-0.5 text-zinc-400 hover:text-white transition">
                <i data-lucide="scan-line" class="w-5 h-5"></i>
                <span class="text-[9px] font-bold">Pagar</span>
            </button>
            <!-- Botão centralizado verde de atalho -->
            <button onclick="openPixModal()" class="relative -top-5 w-14 h-14 bg-picpay-green hover:bg-picpay-darkGreen text-black rounded-full flex items-center justify-center shadow-lg transform transition active:scale-95 z-50">
                <i data-lucide="dollar-sign" class="w-7 h-7 font-black"></i>
            </button>
            <button onclick="alertCustom('Secção de Investimentos: CDI, LCI, LCA e Fundos.')" class="flex flex-col items-center space-y-0.5 text-zinc-400 hover:text-white transition">
                <i data-lucide="trending-up" class="w-5 h-5"></i>
                <span class="text-[9px] font-bold">Investir</span>
            </button>
            <button onclick="alertCustom('A sua carteira de cartões, cadastros de chaves e dados pessoais.')" class="flex flex-col items-center space-y-0.5 text-zinc-400 hover:text-white transition">
                <i data-lucide="wallet" class="w-5 h-5"></i>
                <span class="text-[9px] font-bold">Carteira</span>
            </button>
        </div>

        <!-- BARRA DE COMPLEMENTO SAFARI DO iOS (BARRA DE FERRAMENTAS DO NAVEGADOR) -->
        <div class="absolute bottom-0 left-0 right-0 h-11 bg-[#1C1C1E] border-t border-zinc-800 flex items-center justify-between px-8 text-zinc-400 z-40 select-none pb-2">
            <button class="hover:text-white active:scale-95 transition"><i data-lucide="chevron-left" class="w-5 h-5"></i></button>
            <button class="hover:text-white active:scale-95 transition"><i data-lucide="chevron-right" class="w-5 h-5"></i></button>
            <!-- Ícone clássico de Partilha do Safari -->
            <button onclick="openSafariShareSheet()" class="text-zinc-300 hover:text-picpay-green active:scale-95 transition">
                <i data-lucide="share" class="w-5 h-5"></i>
            </button>
            <button onclick="alertCustom('Favoritos do Safari.')" class="hover:text-white active:scale-95 transition"><i data-lucide="book-open" class="w-5 h-5"></i></button>
            <button onclick="alertCustom('Abas do Safari')" class="hover:text-white active:scale-95 transition"><i data-lucide="layers" class="w-5 h-5"></i></button>
        </div>

        <!-- INDICADOR DA BARRA INFERIOR (HOME INDICATOR) -->
        <div class="absolute bottom-0.5 left-1/2 -translate-x-1/2 w-32 h-1 bg-zinc-600 rounded-full z-50"></div>

        <!-- ================= MODAIS E SUB-ECRÃS ================= -->

        <!-- SHARE SHEET DO SAFARI (iOS MENU DE COMPARTILHAMENTO) -->
        <div id="safari-share-sheet" class="absolute inset-0 bg-black/60 z-50 flex flex-col justify-end hidden">
            <!-- Camada invisível de fecho rápido -->
            <div class="absolute inset-0" onclick="closeSafariShareSheet()"></div>
            
            <div class="bg-[#1C1C1E] rounded-t-[20px] p-4 text-white z-50 animate-share-sheet max-h-[85%] overflow-y-auto no-scrollbar pb-8"><!-- Cabeçalho do Compartilhar -->
                <div class="flex justify-between items-center border-b border-zinc-800 pb-3 mb-4">
                    <div class="flex items-center space-x-2">
                        <div class="w-7 h-7 bg-emerald-600 rounded flex items-center justify-center text-xs font-bold text-white">PP</div>
                        <div>
                            <h4 class="font-bold text-xs text-zinc-100">PicPay Fake Premium</h4>
                            <p class="text-[10px] text-zinc-500">715260091625.pages.dev</p>
                        </div>
                    </div>
                    <button onclick="closeSafariShareSheet()" class="bg-zinc-800 hover:bg-zinc-700 p-1.5 rounded-full">
                        <i data-lucide="x" class="w-4 h-4 text-zinc-400"></i>
                    </button>
                </div>

                <!-- Lista de Contactos Simulação -->
                <p class="text-[10px] font-bold text-zinc-500 uppercase mb-2">Sugestões de Envio</p>
                <div class="flex space-x-3 overflow-x-auto no-scrollbar pb-3 mb-4">
                    <div class="flex flex-col items-center space-y-1 text-center cursor-pointer min-w-[55px]" onclick="shareTo('WhatsApp')">
                        <div class="w-10 h-10 bg-emerald-500 rounded-full flex items-center justify-center text-white"><i data-lucide="message-square" class="w-5 h-5"></i></div>
                        <span class="text-[9px] text-zinc-300">WhatsApp</span>
                    </div>
                    <div class="flex flex-col items-center space-y-1 text-center cursor-pointer min-w-[55px]" onclick="shareTo('Mensagens')">
                        <div class="w-10 h-10 bg-blue-500 rounded-full flex items-center justify-center text-white"><i data-lucide="message-circle" class="w-5 h-5"></i></div>
                        <span class="text-[9px] text-zinc-300">Mensagens</span>
                    </div>
                    <div class="flex flex-col items-center space-y-1 text-center cursor-pointer min-w-[55px]" onclick="shareTo('E-mail')">
                        <div class="w-10 h-10 bg-zinc-600 rounded-full flex items-center justify-center text-white"><i data-lucide="mail" class="w-5 h-5"></i></div>
                        <span class="text-[9px] text-zinc-300">E-mail</span>
                    </div>
                    <div class="flex flex-col items-center space-y-1 text-center cursor-pointer min-w-[55px]" onclick="shareTo('AirDrop')">
                        <div class="w-10 h-10 bg-sky-400 rounded-full flex items-center justify-center text-white"><i data-lucide="wifi" class="w-5 h-5"></i></div>
                        <span class="text-[9px] text-zinc-300">AirDrop</span>
                    </div>
                </div>

                <!-- Lista de Ações do Safari -->
                <div class="space-y-1 bg-zinc-900 rounded-xl overflow-hidden mb-4">
                    <button onclick="copySafariLink()" class="w-full text-left px-4 py-3 hover:bg-zinc-800 flex items-center justify-between text-xs border-b border-zinc-800">
                        <span>Copiar Link</span>
                        <i data-lucide="copy" class="w-4 h-4 text-zinc-400"></i>
                    </button>
                    <button onclick="simulateSafariHomeAdd()" class="w-full text-left px-4 py-3 hover:bg-zinc-800 flex items-center justify-between text-xs text-picpay-green font-semibold border-b border-zinc-800">
                        <span>Adicionar à Tela de Início</span>
                        <i data-lucide="plus-square" class="w-4 h-4 text-picpay-green"></i>
                    </button>
                    <button onclick="alertCustom('Salvo nos Favoritos do Safari simulado.')" class="w-full text-left px-4 py-3 hover:bg-zinc-800 flex items-center justify-between text-xs">
                        <span>Adicionar aos Favoritos</span>
                        <i data-lucide="star" class="w-4 h-4 text-zinc-400"></i>
                    </button>
                </div><div class="text-center text-[10px] text-zinc-500 px-4">
                    Link sincronizado com o servidor de simulação PicPay 2026.
                </div>
            </div>
        </div>

        <!-- TELA DO TOUCH ID / FACE ID (iPHONE MODEL) -->
        <div id="touch-id-screen" class="absolute inset-0 bg-black/95 z-50 flex flex-col items-center justify-between py-20 px-8 hidden">
            <div class="flex flex-col items-center space-y-4 text-center mt-10">
                <div class="w-20 h-20 bg-emerald-950/50 rounded-full flex items-center justify-center border border-picpay-green/30 relative">
                    <div class="absolute inset-0 rounded-full border-4 border-picpay-green/20 pulse-ring"></div>
                    <i data-lucide="fingerprint" class="w-12 h-12 text-picpay-green"></i>
                </div>
                <h3 class="text-xl font-bold text-white">Touch ID / Face ID</h3>
                <p class="text-xs text-zinc-400 max-w-xs font-medium">Toque para autenticar e validar o acesso de segurança PicPay.</p>
            </div>

            <div class="flex flex-col items-center w-full space-y-3">
                <button onclick="simulateBiometricSuccess()" class="w-full bg-picpay-green hover:bg-picpay-darkGreen text-black py-3.5 rounded-xl font-bold text-sm transition active:scale-95">
                    Simular Impressão Digital
                </button>
                <button onclick="closeTouchID()" class="w-full bg-zinc-900 hover:bg-zinc-800 text-zinc-300 py-3 rounded-xl font-medium text-xs transition">
                    Cancelar
                </button>
            </div>
        </div>

        <!-- PAINEL DE CONFIGURAÇÕES / ADMIN (MODIFICAÇÃO DOS VALORES) -->
        <div id="admin-panel" class="absolute inset-x-0 bottom-0 top-12 bg-[#1C1C1E] rounded-t-[30px] z-50 flex flex-col overflow-hidden hidden">
            <!-- Header do painel -->
            <div class="p-4 border-b border-zinc-800 flex items-center justify-between">
                <div class="flex items-center space-x-2 text-picpay-green">
                    <i data-lucide="settings" class="w-5 h-5"></i>
                    <h3 class="font-bold text-white text-sm">Ajustes do App Fake</h3>
                </div>
                <button onclick="closeAdminPanel()" class="text-zinc-400 hover:text-white">
                    <i data-lucide="x" class="w-6 h-6"></i>
                </button>
            </div>

            <!-- Corpo do painel (Formulários) -->
            <div class="p-5 flex-1 overflow-y-auto space-y-5 no-scrollbar pb-10">
                <div class="bg-zinc-900 p-4 rounded-xl space-y-3">
                    <h4 class="text-xs font-bold text-picpay-green uppercase tracking-wide">Dados de Identidade</h4>
                    
                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Nome do Titular</label>
                        <input type="text" id="admin-name" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Amanda Oliveira">
                    </div>

                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Link da Foto (Avatar URL)</label>
                        <input type="text" id="admin-avatar" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="URL da foto">
                    </div>
                </div>

                <div class="bg-zinc-900 p-4 rounded-xl space-y-3">
                    <h4 class="text-xs font-bold text-picpay-green uppercase tracking-wide">Saldos da Conta</h4>
                    
                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Saldo Principal (R$)</label>
                        <input type="number" step="0.01" id="admin-balance" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="1542.80">
                    </div>

                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Saldo de Cashback (R$)</label>
                        <input type="number" step="0.01" id="admin-cashback" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="48.90">
                    </div>
                </div>

                <div class="bg-zinc-900 p-4 rounded-xl space-y-3">
                    <h4 class="text-xs font-bold text-picpay-green uppercase tracking-wide">Disparar Notificações</h4>
                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Título do Alerta</label>
                        <input type="text" id="admin-notify-title" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Envio realizado">
                    </div>
                    <div>
                        <label class="block text-xs text-zinc-400 mb-1">Mensagem do Push</label>
                        <input type="text" id="admin-notify-msg" class="w-full bg-zinc-800 border border-zinc-700 rounded-lg p-2 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Fez um pagamento Pix no valor de...">
                    </div>
                    <button onclick="triggerCustomNotification()" class="w-full bg-zinc-800 text-picpay-green py-2 rounded-lg text-xs font-bold border border-picpay-green/20 hover:bg-zinc-700 transition">
                        Disparar Alerta Instantâneo
                    </button>
                </div>
            </div>

            <!-- Rodapé Salvar -->
            <div class="p-4 bg-zinc-900 border-t border-zinc-800">
                <button onclick="saveAdminSettings()" class="w-full bg-picpay-green hover:bg-picpay-darkGreen text-black py-3 rounded-xl font-bold text-sm transition">
                    Guardar Alterações
                </button>
            </div>
        </div>

        <!-- MODAL DE TRANSFERIR PIX -->
        <div id="pix-modal" class="absolute inset-x-0 bottom-0 top-12 bg-zinc-950 rounded-t-[30px] z-50 flex flex-col overflow-hidden hidden">
            <!-- Header do pix -->
            <div class="p-4 border-b border-zinc-900 flex items-center justify-between bg-zinc-900">
                <div class="flex items-center space-x-2 text-picpay-green">
                    <i data-lucide="qr-code" class="w-5 h-5"></i>
                    <h3 class="font-bold text-white">Enviar Pix</h3>
                </div>
                <button onclick="closePixModal()" class="text-zinc-400 hover:text-white">
                    <i data-lucide="x" class="w-6 h-6"></i>
                </button>
            </div>

            <!-- Formulário Pix -->
            <div class="p-5 flex-1 overflow-y-auto space-y-4 no-scrollbar">
                <div class="bg-zinc-900 p-4 rounded-xl border border-zinc-800">
                    <label class="block text-xs text-picpay-green font-bold mb-2 uppercase">Nome do Recebedor</label>
                    <input type="text" id="pix-target-name" class="w-full bg-zinc-950 border border-zinc-700 rounded-lg p-3 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Ex: João Silva da Cruz">
                </div>

                <div class="bg-zinc-900 p-4 rounded-xl border border-zinc-800">
                    <label class="block text-xs text-picpay-green font-bold mb-2 uppercase">Chave Pix (CPF, Telefone ou E-mail)</label>
                    <input type="text" id="pix-target-key" class="w-full bg-zinc-955 border border-zinc-700 rounded-lg p-3 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Ex: 123.456.789-00">
                </div><div class="bg-zinc-900 p-4 rounded-xl border border-zinc-800">
                    <label class="block text-xs text-picpay-green font-bold mb-2 uppercase">Banco Destino</label>
                    <input type="text" id="pix-target-bank" class="w-full bg-zinc-955 border border-zinc-700 rounded-lg p-3 text-white text-sm focus:outline-none focus:border-picpay-green" placeholder="Ex: Banco PicPay S.A." value="Banco PicPay S.A.">
                </div>

                <div class="bg-zinc-900 p-4 rounded-xl border border-zinc-800">
                    <label class="block text-xs text-picpay-green font-bold mb-2 uppercase">Valor do Envio (R$)</label>
                    <input type="number" step="0.01" id="pix-amount" class="w-full bg-zinc-955 border border-zinc-700 rounded-lg p-3 text-white text-xl font-bold focus:outline-none focus:border-picpay-green" placeholder="R$ 0,00">
                </div>
            </div>

            <!-- Confirmar -->
            <div class="p-4 bg-zinc-900 border-t border-zinc-800">
                <button onclick="processPixPayment()" class="w-full bg-picpay-green hover:bg-picpay-darkGreen text-black py-3.5 rounded-xl font-bold text-sm transition flex items-center justify-center space-x-2">
                    <span>Confirmar Pix</span>
                    <i data-lucide="arrow-right" class="w-4 h-4"></i>
                </button>
            </div>
        </div>

        <!-- TELA DE PROCESSANDO PAGAMENTO -->
        <div id="processing-screen" class="absolute inset-0 bg-picpay-bg z-50 flex flex-col items-center justify-center p-8 hidden">
            <div class="flex flex-col items-center space-y-6 text-center">
                <!-- Ícone animado do Picpay -->
                <div class="w-24 h-24 bg-picpay-green/10 rounded-full flex items-center justify-center border border-picpay-green/30 animate-pulse">
                    <i data-lucide="shield-check" class="w-14 h-14 text-picpay-green"></i>
                </div>
                <h3 class="text-xl font-bold text-white">Análise de Segurança PicPay...</h3>
                <p class="text-xs text-zinc-400 max-w-xs">Analisando segurança da transação via Banco Central. Por favor, aguarde alguns instantes.</p>
                <div class="w-12 h-1.5 bg-zinc-800 rounded-full overflow-hidden">
                    <div class="h-full bg-picpay-green rounded-full animate-infinite w-1/2" style="animation: pulse-ring 1s infinite alternate;"></div>
                </div>
            </div>
        </div>

        <!-- TELA DO COMPROVANTE OFICIAL PICPAY -->
        <div id="receipt-screen" class="absolute inset-0 bg-[#121212] z-50 flex flex-col overflow-hidden hidden">
            <!-- Header do Comprovante -->
            <div class="p-4 border-b border-zinc-800 flex items-center justify-between bg-[#1A1A1A]">
                <h3 class="font-bold text-sm text-zinc-300">Comprovante de Transferência</h3>
                <button onclick="closeReceipt()" class="text-zinc-400 hover:text-white">
                    <i data-lucide="x" class="w-6 h-6"></i>
                </button>
            </div>

            <!-- Corpo do Comprovante -->
            <div class="p-6 flex-1 overflow-y-auto space-y-5 no-scrollbar text-xs">
                <!-- Logotipo PicPay -->
                <div class="flex items-center justify-between border-b border-zinc-800 pb-4">
                    <div class="flex items-center space-x-2">
                        <div class="w-8 h-8 bg-picpay-green rounded-full flex items-center justify-center">
                            <i data-lucide="dollar-sign" class="w-5 h-5 text-black font-bold"></i>
                        </div>
                        <span class="font-black text-white text-base tracking-tight">PicPay</span>
                    </div>
                    <span class="text-picpay-green font-bold">Pix Concluído</span>
                </div>

                <!-- Detalhes do Pagamento -->
                <div class="space-y-4">
                    <div><p class="text-zinc-400 text-[11px] uppercase tracking-wider">Valor Transferido</p>
                        <h2 id="receipt-amount" class="text-3xl font-extrabold text-white mt-1">R$ 150,00</h2>
                    </div>

                    <div class="border-t border-zinc-800 pt-4 space-y-3">
                        <p class="text-[11px] font-bold text-picpay-green uppercase tracking-wider mb-2">Destinatário</p>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Nome:</span>
                            <span id="receipt-to-name" class="text-white font-semibold">Marcos da Silva</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Chave Pix:</span>
                            <span id="receipt-to-key" class="text-white font-mono">***.456.***-00</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Banco:</span>
                            <span id="receipt-to-bank" class="text-white">Banco Itaú S.A.</span>
                        </div>
                    </div>

                    <div class="border-t border-zinc-800 pt-4 space-y-3">
                        <p class="text-[11px] font-bold text-picpay-green uppercase tracking-wider mb-2">Remetente</p>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Nome:</span>
                            <span id="receipt-from-name" class="text-white">Amanda Oliveira</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Instituição:</span>
                            <span class="text-white">PicPay Serviços S.A.</span>
                        </div>
                    </div>

                    <div class="border-t border-zinc-800 pt-4 space-y-3">
                        <p class="text-[11px] font-bold text-zinc-400 uppercase tracking-wider mb-2">Código da Transação</p>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Identificação:</span>
                            <span id="receipt-id" class="text-white font-mono text-[10px] break-all max-w-[200px] text-right">E00038162202610121304x882b3a9101</span>
                        </div>
                        <div class="flex justify-between">
                            <span class="text-zinc-400">Data e Hora:</span>
                            <span id="receipt-date" class="text-white">12/10/2026 - 13:45</span>
                        </div>
                    </div>
                </div>

                <div class="bg-zinc-900/60 border border-zinc-800 p-3 rounded-lg flex items-center space-x-3 text-zinc-400">
                    <i data-lucide="shield-alert" class="w-5 h-5 text-picpay-green"></i>
                    <p class="text-[10px] leading-relaxed">Este comprovante serve como registro de envio oficial de transação via Banco Central.</p>
                </div>
            </div>

            <!-- Ações -->
            <div class="p-4 bg-zinc-900 border-t border-zinc-800 space-y-2">
                <button onclick="copyReceiptText()" class="w-full bg-picpay-green text-black font-bold py-3 rounded-xl transition flex items-center justify-center space-x-2 active:scale-95">
                    <i data-lucide="copy" class="w-4 h-4"></i>
                    <span>Copiar Texto do Comprovante</span>
                </button>
                <button onclick="closeReceipt()" class="w-full bg-zinc-800 text-zinc-300 font-medium py-2.5 rounded-xl text-xs hover:bg-zinc-700 transition">
                    Fechar e Voltar ao Início
                </button>
            </div>
        </div>

        <!-- ALERTA CUSTOMIZADO --><div id="custom-alert-modal" class="absolute inset-0 bg-black/80 z-50 flex items-center justify-center p-6 hidden">
            <div class="bg-zinc-900 border border-zinc-800 rounded-2xl p-5 w-full max-w-[320px] text-center space-y-4">
                <div class="w-12 h-12 bg-picpay-green/10 rounded-full flex items-center justify-center mx-auto text-picpay-green">
                    <i data-lucide="info" class="w-6 h-6"></i>
                </div>
                <div>
                    <h4 class="font-bold text-white text-sm" id="alert-title">Aviso</h4>
                    <p class="text-xs text-zinc-400 mt-1" id="alert-message">Detalhes do alerta.</p>
                </div>
                <button onclick="closeCustomAlert()" class="w-full bg-picpay-green hover:bg-picpay-darkGreen text-black font-bold py-2 rounded-lg text-xs transition">
                    Entendido
                </button>
            </div>
        </div>

    </div>

    <!-- SCRIPTS DE COMPORTAMENTO E LÓGICA -->
    <script>
        // Estado central da aplicação
        let state = {
            userName: "Amanda Oliveira",
            userAvatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=200&auto=format&fit=crop",
            balance: 1542.80,
            cashback: 48.90,
            isVisible: true,
            transactions: [
                { id: "1", type: "pix_out", name: "Gabriel Menezes", key: "***.231.***-20", value: 340.00, date: "30 Jun 2026, 21:05" },
                { id: "2", type: "pix_in", name: "Lúcia S. Oliveira", key: "***.981.***-10", value: 500.00, date: "30 Jun 2026, 18:32" },
                { id: "3", type: "payment", name: "Supermercado Compre Bem", key: "Cnpj", value: 124.90, date: "29 Jun 2026, 14:10" }
            ],
            currentBiometricPurpose: "admin"
        };

        // Carregar ícones e dados no arranque
        window.addEventListener('DOMContentLoaded', () => {
            lucide.createIcons();
            updateClock();
            setInterval(updateClock, 1000);
            renderUI();
            
            // Valores padrão no formulário administrativo
            document.getElementById('admin-name').value = state.userName;
            document.getElementById('admin-avatar').value = state.userAvatar;
            document.getElementById('admin-balance').value = state.balance.toFixed(2);
            document.getElementById('admin-cashback').value = state.cashback.toFixed(2);
        });

        // Relógio do Telemóvel
        function updateClock() {
            const now = new Date();
            const hours = String(now.getHours()).padStart(2, '0');
            const minutes = String(now.getMinutes()).padStart(2, '0');
            document.getElementById('ios-time').textContent = `${hours}:${minutes}`;
        }

        // Renderização Global da UI
        function renderUI() {
            document.getElementById('user-name-display').textContent = state.userName;
            document.getElementById('user-avatar').src = state.userAvatar;
            
            if (state.isVisible) {
                document.getElementById('balance-value').textContent = formatCurrency(state.balance);
                document.getElementById('cashback-value').textContent = formatCurrency(state.cashback);
                document.getElementById('balance-value').classList.remove('hidden');
                document.getElementById('balance-hidden').classList.add('hidden');
            } else {
                document.getElementById('balance-value').classList.add('hidden');
                document.getElementById('balance-hidden').classList.remove('hidden');
                document.getElementById('cashback-value').textContent = "R$ ••••••";
            }

            renderTransactions();
        }

        // Lista de Transações Recentes
        function renderTransactions() {
            const container = document.getElementById('transactions-list');
            container.innerHTML = "";

            if (state.transactions.length === 0) {
                container.<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>PicPay - Carteira</title>
    <!-- Tailwind CSS para estilização rápida -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Lucide Icons para os ícones realistas -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Configurações de cores corporativas do PicPay -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        picpay: {
                            green: '#11C76F',
                            darkGreen: '#0B8F4F',
                            lightGreen: '#E6F9F0',
                            bg: '#121212',
                            card: '#1F1F1F',
                            border: '#2A2A2A',
                            textMuted: '#9E9E9E'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d0d0d;
            overflow-x: hidden;
            user-select: none;
            -webkit-user-select: none;
        }

        /* Esconder barras de rolagem mas manter funcionamento de scroll */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }

        /* Animação do Touch ID */
        @keyframes pulse-ring {
            0% { transform: scale(0.95); opacity: 0.8; }
            50% { transform: scale(1.1); opacity: 0.4; }
            100% { transform: scale(0.95); opacity: 0.8; }
        }
        .pulse-ring {
            animation: pulse-ring 2s infinite ease-in-out;
        }

        /* Notificação Push */
        @keyframes slide-down {
            0% { transform: translateY(-100%); opacity: 0; }
            15% { transform: translateY(0); opacity: 1; }
            85% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100%); opacity: 0; }
        }
        .notification-push {
            animation: slide-down 4s ease-in-out forwards;
        }

        /* Slide-up para o Share Sheet do iOS */
        @keyframes slide-up-share {
            from { transform: translateY(100%); }
            to { transform: translateY(0); }
        }
        .animate-share-sheet {
            animation: slide-up-share 0.3s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }
    </style>
</head>
<body class="flex justify-center items-center min-h-screen p-0 sm:p-4 bg-[#0a0a0a]">

    <!-- DISPOSITIVO IPHONE SIMULADO (Aparência do Link Premium) -->
    <div class="relative w-full max-w-[412px] h-[892px] bg-black rounded-[50px] shadow-[0_0_50px_rgba(17,199,111,0.15)] border-[10px] border-[#1f1f1f] flex flex-col overflow-hidden">
        
        <!-- Notificação Push (Injetada via JS) -->
        <div id="push-notification-container" class="absolute top-12 left-4 right-4 z-50 pointer-events-none"></div>

        <!-- Dynamic Island / Câmera Frontal do iPhone -->
        <div class="absolute top-3 left-1/2 -translate-x-1/2 w-28 h-[26px] bg-black rounded-3xl z-50 flex items-center justify-between px-3">
            <div class="w-3.5 h-3.5 bg-[#111] rounded-full"></div>
            <div class="w-8 h-1 bg-[#111] rounded-full"></div>
        </div>

        <!-- Barra de Estado do iOS -->
        <div class="h-11 bg-picpay-bg text-white px-6 flex justify-between items-end pb-1 text-[12px] font-semibold select-none z-40">
            <span id="ios-time">22:06</span>
            <div class="flex items-center space-x-1.5 pb-[2px]">
                <i data-lucide="signal" class="w-3.5 h-3.5"></i>
                <span class="text-[10px]">5G</span>innerHTML = `
                    <div class="text-center py-6 text-zinc-500">
                        <i data-lucide="inbox" class="w-8 h-8 mx-auto mb-2 opacity-50"></i>
                        <p class="text-xs">Nenhum movimento registrado hoje.</p>
                    </div>
                `;
                lucide.createIcons();
                return;
            }

            state.transactions.forEach(t => {
                let icon = "arrow-up-right";
                let iconClass = "bg-zinc-800 text-zinc-300";
                let sign = "-";
                let valClass = "text-white";

                if (t.type === 'pix_in') {
                    icon = "arrow-down-left";
                    iconClass = "bg-emerald-950/40 text-picpay-green";
                    sign = "+";
                    valClass = "text-picpay-green";
                }

                const cardHtml = `
                    <div class="flex items-center justify-between p-3 bg-picpay-card rounded-xl border border-picpay-border hover:bg-zinc-800 transition">
                        <div class="flex items-center space-x-3">
                            <div class="w-9 h-9 ${iconClass} rounded-full flex items-center justify-center">
                                <i data-lucide="${icon}" class="w-4 h-4"></i>
                            </div>
                            <div>
                                <h5 class="font-semibold text-xs text-white">${t.name}</h5>
                                <p class="text-[10px] text-zinc-400">${t.date}</p>
                            </div>
                        </div>
                        <div class="text-right">
                            <span class="font-extrabold text-xs ${valClass}">${sign} ${formatCurrency(t.value)}</span>
                            <p class="text-[9px] text-picpay-green font-bold">Pix</p>
                        </div>
                    </div>
                `;
                container.innerHTML += cardHtml;
            });

            lucide.createIcons();
        }

        // Moeda de Apresentação
        function formatCurrency(val) {
            return new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(val);
        }

        // Ocultar/Mostrar saldo
        function toggleVisibility() {
            state.isVisible = !state.isVisible;
            const eye = document.getElementById('eye-icon');
            if (state.isVisible) {
                eye.setAttribute('data-lucide', 'eye');
            } else {
                eye.setAttribute('data-lucide', 'eye-off');
            }
            renderUI();
        }

        // SISTEMA SAFARI SHARE SHEET (COMPARTILHAMENTO)
        function openSafariShareSheet() {
            document.getElementById('safari-share-sheet').classList.remove('hidden');
        }

        function closeSafariShareSheet() {
            document.getElementById('safari-share-sheet').classList.add('hidden');
        }

        function shareTo(platform) {
            closeSafariShareSheet();
            simulatePushNotification("Compartilhar Safari", `Enviando link do app para o ${platform}...`);
        }

        function copySafariLink() {
            closeSafariShareSheet();
            const dummy = document.createElement('input');
            dummy.value = "https://715260091625.pages.dev/";
            document.body.appendChild(dummy);
            dummy.select();
            document.execCommand('copy');
            document.body.removeChild(dummy);
            simulatePushNotification("Link Copiado", "Endereço do Safari copiado com sucesso!");
        }

        function simulateSafariHomeAdd() {
            closeSafariShareSheet();
            alertCustom("Para adicionar este app à sua Tela de Início:\n\n1. Toque no botão de Compartilhar do seu Safari real.\n2. Escolha 'Adicionar à Tela de Início'.\n3. Desfrute da experiência completa em tela cheia!", "Tela de Início");
        }

        function reloadApp() {
            simulatePushNotification("Safari", "Recarregando página...");setTimeout(() => {
                renderUI();
            }, 800);
        }

        // CONTROLES DO BIOMÉTRICO (TOUCH ID)
        function openTouchID(purpose) {
            state.currentBiometricPurpose = purpose;
            document.getElementById('touch-id-screen').classList.remove('hidden');
        }

        function closeTouchID() {
            document.getElementById('touch-id-screen').classList.add('hidden');
        }

        function simulateBiometricSuccess() {
            closeTouchID();
            if (state.currentBiometricPurpose === 'admin') {
                document.getElementById('admin-panel').classList.remove('hidden');
            } else if (state.currentBiometricPurpose === 'pix') {
                executePaymentFinalization();
            }
        }

        // CONTROLES DO PAINEL ADMIN (AJUSTAR SALDOS)
        function closeAdminPanel() {
            document.getElementById('admin-panel').classList.add('hidden');
        }

        function saveAdminSettings() {
            const nameInput = document.getElementById('admin-name').value.trim();
            const avatarInput = document.getElementById('admin-avatar').value.trim();
            const balanceInput = parseFloat(document.getElementById('admin-balance').value);
            const cashbackInput = parseFloat(document.getElementById('admin-cashback').value);

            if (nameInput) state.userName = nameInput;
            if (avatarInput) state.userAvatar = avatarInput;
            if (!isNaN(balanceInput)) state.balance = balanceInput;
            if (!isNaN(cashbackInput)) state.cashback = cashbackInput;

            renderUI();
            closeAdminPanel();
            simulatePushNotification("Sucesso", "Configurações da carteira salvas com sucesso.");
        }

        function triggerCustomNotification() {
            const title = document.getElementById('admin-notify-title').value || "Notificação";
            const msg = document.getElementById('admin-notify-msg').value || "Pix recebido!";
            simulatePushNotification(title, msg);
        }

        // DISPARADOR DE NOTIFICAÇÕES PUSH SIMULADAS
        function simulatePushNotification(title, text) {
            const container = document.getElementById('push-notification-container');
            const notification = document.createElement('div');
            notification.className = "notification-push bg-zinc-900/95 backdrop-blur-md border border-zinc-800 p-3.5 rounded-2xl shadow-[0_8px_30px_rgba(0,0,0,0.5)] flex items-start space-x-3 mb-2 z-50 text-white pointer-events-auto cursor-pointer";
            notification.innerHTML = `
                <div class="w-8 h-8 bg-picpay-green rounded-lg flex items-center justify-center text-black flex-shrink-0">
                    <i data-lucide="dollar-sign" class="w-5 h-5 font-black"></i>
                </div>
                <div class="flex-1">
                    <div class="flex justify-between items-center">
                        <span class="font-bold text-xs text-picpay-green">PicPay</span>
                        <span class="text-[9px] text-zinc-500">Agora</span>
                    </div>
                    <h5 class="font-semibold text-xs mt-0.5 text-zinc-100">${title}</h5>
                    <p class="text-[11px] text-zinc-400 mt-0.5 leading-snug">${text}</p>
                </div>
            `;

            container.appendChild(notification);
            lucide.createIcons();

            setTimeout(() => {
                notification.remove();
            }, 4000);
        }

        // FLUXO DE PAGAMENTO PIX
        function openPixModal() {
            document.getElementById('pix-modal').classList.remove('hidden');
        }

        function closePixModal() {
            document.getElementById('pix-modal').classList.add('hidden');
        }

        function processPixPayment() {
            const name = document.getElementById('pix-target-name').value.trim();
            const key = document.getElementById('pix-target-key').value.trim();
            const amount = parseFloat(document.getElementById('pix-amount').value);

            if (!name || !key || isNaN(amount) || amount <= 0) {
                alertCustom("Por favor, preencha todos os campos obrigatórios corretamente.");
                return;
            }

            if (amount > state.balance) {
                alertCustom("O seu saldo PicPay não é suficiente para realizar esta transferência.");
                return;
            }

            closePixModal();
            openTouchID('pix');
        }

        function executePaymentFinalization() {
            const name = document.getElementById('pix-target-name').value.trim();
            const key = document.getElementById('pix-target-key').value.trim();
            const bank = document.getElementById('pix-target-bank').value.trim() || "Banco PicPay S.A.";
            const amount = parseFloat(document.getElementById('pix-amount').value);

            document.getElementById('processing-screen').classList.remove('hidden');

            setTimeout(() => {
                state.balance -= amount;
                
                const now = new Date();
                const formattedDate = `${now.getDate()} ${now.toLocaleString('pt-BR', { month: 'short' })} ${now.getFullYear()}, ${String(now.getHours()).padStart(2, '0')}:${String(now.getMinutes()).padStart(2, '0')}`;
                
                state.transactions.unshift({
                    id: Date.now().toString(),
                    type: "pix_out",
                    name: name,
                    key: key,
                    value: amount,
                    date: formattedDate
                });

                renderUI();

                // Montar Comprovante
                document.getElementById('receipt-amount').textContent = formatCurrency(amount);
                document.getElementById('receipt-to-name').textContent = name;
                document.getElementById('receipt-to-key').textContent = key;
                document.getElementById('receipt-to-bank').textContent = bank;
                document.getElementById('receipt-from-name').textContent = state.userName;
                document.getElementById('receipt-id').textContent = 'E' + Math.random().toString().slice(2, 12) + '2026' + Math.random().toString().slice(2, 12);
                document.getElementById('receipt-date').textContent = formattedDate;

                document.getElementById('processing-screen').classList.add('hidden');
                document.getElementById('receipt-screen').classList.remove('hidden');

                simulatePushNotification("Pix Concluído!", `Você enviou ${formatCurrency(amount)} para ${name}.`);
            }, 2000);
        }

        // Fecha a tela do comprovante
        function closeReceipt() {
            document.getElementById('receipt-screen').classList.add('hidden');
            document.getElementById('pix-target-name').value = "";
            document.getElementById('pix-target-key').value = "";
            document.getElementById('pix-amount').value = "";
        }

        // Copia o resumo em formato de texto para área de transferência
        function copyReceiptText() {
            const name = document.getElementById('receipt-to-name').textContent;
            const amount = document.getElementById('receipt-amount').textContent;
            const key = document.getElementById('receipt-to-key').textContent;
            const bank = document.getElementById('receipt-to-bank').textContent;
            const date = document.getElementById('receipt-date').textContent;
            const txId = document.getElementById('receipt-id').textContent;

            const summary = `
=== COMPROVANTE PIX PICPAY ===
Valor: ${amount}
Destinatário: ${name}
Chave Pix: ${key}
Banco: ${bank}
Data: ${date}
ID Transação: ${txId}
==============================
            `.trim();

            const temp = document.createElement('textarea');
            temp.value = summary;
            document.body.appendChild(temp);
            temp.select();
            document.execCommand('copy');
            document.body.removeChild(temp);

            simulatePushNotification("Copiado", "Texto do comprovante copiado com sucesso!");
        }

        // Limpa o histórico de transações
        function clearHistory() {
            state.transactions = [];
            renderUI();
            simulatePushNotification("Limpo", "Histórico de atividade limpo com sucesso.");
        }

        // Alerta personalizado integrado
        function alertCustom(msg, title = "Aviso") {
            document.getElementById('alert-title').textContent = title;
            document.getElementById('alert-message').textContent = msg;
            document.getElementById('custom-alert-modal').classList.remove('hidden');
        }

        function closeCustomAlert() {
            document.getElementById('custom-alert-modal').classList.add('hidden');
        }

        // Retorna a aba ao início
        function switchTab(tab) {
            if (tab === 'inicio') {
                closePixModal();
                closeReceipt();
                closeAdminPanel();
            }
        }
    </script>
</body>
</html>
