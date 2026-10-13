<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🥝 Primeira Venda Pro — Especialista em Vendas Kiwify</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: { kiwi: { orange: '#FF7A00', yellow: '#FFB800', dark: '#C25A00', light: '#FFF8EB' } },
                    fontFamily: { sans: ['Inter', 'sans-serif'], display: ['Poppins', 'sans-serif'] },
                    animation: { 'float': 'float 6s ease-in-out infinite' },
                    keyframes: { float: { '0%,100%': { transform: 'translateY(0)' }, '50%': { transform: 'translateY(-8px)' } } }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Poppins:wght@400;500;600;700;800;900&display=swap');
        body { background: linear-gradient(135deg, #FFF8EB 0%, #FFEBCD 40%, #FFE0B2 100%); min-height: 100vh; }
        .card-shadow { box-shadow: 0 15px 50px rgba(255, 122, 0, 0.18); }
        .gradient-text { background: linear-gradient(90deg, #FF7A00, #FFB800, #FF7A00); background-size: 200% auto; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: shine 4s linear infinite; }
        @keyframes shine { to { background-position: 200% center; } }
        .scroll-container { max-height: 70vh; overflow-y: auto; }
        .scroll-container::-webkit-scrollbar { width: 6px; }
        .scroll-container::-webkit-scrollbar-thumb { background: linear-gradient(180deg, #FF7A00, #FFB800); border-radius: 3px; }
        .fade-in { animation: fadeIn 0.5s ease forwards; opacity: 0; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
        .dica-item { border-left: 3px solid transparent; transition: all 0.25s ease; }
        .dica-item:hover { border-left-color: #FF7A00; background: rgba(255, 122, 0, 0.05); transform: translateX(3px); }
        .chat-bubble-user { border-radius: 18px 18px 4px 18px; background: linear-gradient(135deg, #FF7A00, #FFB800); color: white; box-shadow: 0 4px 15px rgba(255,122,0,0.3); }
        .chat-bubble-ai { border-radius: 18px 18px 18px 4px; background: white; border: 1px solid #FFE4B5; box-shadow: 0 2px 10px rgba(0,0,0,0.04); }
        .typing-dot { animation: typing 1.4s infinite; }
        .typing-dot:nth-child(2) { animation-delay: 0.2s; }
        .typing-dot:nth-child(3) { animation-delay: 0.4s; }
        @keyframes typing { 0%, 60%, 100% { transform: translateY(0); opacity: 0.4; } 30% { transform: translateY(-5px); opacity: 1; } }
        .badge-pro { background: linear-gradient(135deg, #1F2937, #374151); }
    </style>
</head>
<body class="font-sans">
    <div class="container mx-auto px-4 py-8 max-w-4xl">
        <!-- Cabeçalho Premium -->
        <header class="text-center mb-8 fade-in">
            <div class="inline-block relative mb-4 animate-float">
                <div class="w-24 h-24 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center shadow-2xl">
                    <span class="text-white text-5xl">🥝</span>
                </div>
                <div class="absolute -bottom-1 -right-1 badge-pro text-white text-xs font-bold px-3 py-1 rounded-full shadow-lg">PRO</div>
            </div>
            <h1 class="text-[clamp(1.8rem,5vw,3.2rem)] font-display font-black mb-2">
                <span class="gradient-text">Primeira Venda Pro</span>
            </h1>
            <p class="text-gray-600 max-w-xl mx-auto mb-1">Seu Especialista particular em Vendas na Kiwify</p>
            <div class="inline-flex items-center gap-2 text-xs text-gray-500 bg-white/60 px-4 py-1.5 rounded-full">
                <span class="w-2 h-2 bg-green-500 rounded-full animate-pulse"></span>
                +10.000 combinações de respostas · Calculadora integrada · Listas sob demanda
            </div>
            
            <div class="mt-5 bg-white rounded-2xl p-4 card-shadow max-w-lg mx-auto">
                <p class="text-sm text-gray-500 italic">
                    <i class="fa fa-quote-left text-kiwi-orange mr-2"></i>
                    <strong>Opinião do Criador:</strong> Fazer uma IA com HTML é uma das melhores opções que existe! Leve, funciona em qualquer navegador, total controle e <strong>super fácil de aprender</strong>! Qualquer pessoa cria coisas incríveis com dedicação. Simples, rápido e poderoso!
                    <i class="fa fa-quote-right text-kiwi-orange ml-2"></i>
                </p>
                <p class="text-xs text-right text-gray-400 mt-2">— O Dono ✅</p>
            </div>
        </header>

        <!-- Abas -->
        <div class="flex flex-wrap justify-center gap-2 mb-6 fade-in">
            <button onclick="mostrarSecao('inicio')" id="tab-inicio" class="px-5 py-2.5 rounded-full font-semibold bg-gradient-to-r from-kiwi-orange to-kiwi-yellow text-white shadow-md text-sm transition-all"><i class="fa fa-home mr-1"></i>Início</button>
            <button onclick="mostrarSecao('sobre')" id="tab-sobre" class="px-5 py-2.5 rounded-full font-semibold bg-white text-gray-700 hover:bg-orange-50 transition-all text-sm"><i class="fa fa-info-circle mr-1"></i>Sobre a Kiwify</button>
            <button onclick="mostrarSecao('passo')" id="tab-passo" class="px-5 py-2.5 rounded-full font-semibold bg-white text-gray-700 hover:bg-orange-50 transition-all text-sm"><i class="fa fa-shoe-prints mr-1"></i>Passo a Passo</button>
            <button onclick="mostrarSecao('dicas')" id="tab-dicas" class="px-5 py-2.5 rounded-full font-semibold bg-white text-gray-700 hover:bg-orange-50 transition-all text-sm"><i class="fa fa-lightbulb mr-1"></i>100 Dicas</button>
            <button onclick="mostrarSecao('chat')" id="tab-chat" class="px-5 py-2.5 rounded-full font-semibold bg-white text-gray-700 hover:bg-orange-50 transition-all text-sm"><i class="fa fa-robot mr-1"></i>Especialista 🤖</button>
        </div>

        <!-- INÍCIO -->
        <section id="sec-inicio" class="fade-in">
            <div class="bg-white rounded-3xl p-6 card-shadow">
                <h2 class="text-2xl font-bold text-gray-800 mb-4">Bem-vindo ao <span class="gradient-text">Primeira Venda Pro</span>! 🎉</h2>
                <p class="text-gray-600 mb-6">Tudo o que você precisa para conquistar sua primeira venda na Kiwify e muito mais!</p>
                
                <div class="grid md:grid-cols-3 gap-4 mb-6">
                    <div class="bg-gradient-to-br from-orange-50 to-yellow-50 rounded-2xl p-5 border border-orange-100">
                        <span class="text-3xl">🥝</span>
                        <h3 class="font-bold mt-2 mb-1 text-gray-800">Especialista Kiwify</h3>
                        <p class="text-xs text-gray-600">Responde tudo sobre a plataforma, vendas e estratégias</p>
                    </div>
                    <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-5 border border-blue-100">
                        <span class="text-3xl">📋</span>
                        <h3 class="font-bold mt-2 mb-1 text-gray-800">Listas sob Demanda</h3>
                        <p class="text-xs text-gray-600">Peça "10 opções", "5 dicas", "20 maneiras" — ele gera na hora!</p>
                    </div>
                    <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-2xl p-5 border border-green-100">
                        <span class="text-3xl">🧮</span>
                        <h3 class="font-bold mt-2 mb-1 text-gray-800">Calculadora</h3>
                        <p class="text-xs text-gray-600">Digite uma conta e ele resolve na hora!</p>
                    </div>
                </div>

                <div class="bg-gradient-to-r from-orange-500 to-yellow-500 rounded-2xl p-5 text-white">
                    <h3 class="font-bold text-lg mb-2">🤖 Como usar o Especialista?</h3>
                    <p class="text-sm opacity-95 mb-3">Clique na aba <strong>"Especialista 🤖"</strong> e pergunte o que quiser:</p>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-2 text-xs">
                        <div class="bg-white/20 rounded-lg px-3 py-2">💬 "Me dê 10 opções de como vender na Kiwify"</div>
                        <div class="bg-white/20 rounded-lg px-3 py-2">💬 "5 dicas de divulgação no Instagram"</div>
                        <div class="bg-white/20 rounded-lg px-3 py-2">💬 "Quanto é 25×4?"</div>
                        <div class="bg-white/20 rounded-lg px-3 py-2">💬 "Como criar minha conta?"</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- SOBRE -->
        <section id="sec-sobre" class="hidden">
            <div class="bg-white rounded-3xl p-6 card-shadow scroll-container">
                <h2 class="text-2xl font-bold text-gray-800 mb-5">Tudo Sobre a Kiwify 🥝</h2>
                <div class="space-y-4">
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">🤔</span><h3 class="font-bold mt-1 mb-1">O que é?</h3><p class="text-sm text-gray-600">Plataforma brasileira para vender produtos digitais. Simples, em português, sem mensalidade.</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">📦</span><h3 class="font-bold mt-1 mb-1">O que vender?</h3><p class="text-sm text-gray-600">E-books, cursos, mentorias, templates, planilhas, áudios, vídeos, assinaturas. Tudo digital!</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">💳</span><h3 class="font-bold mt-1 mb-1">Pagamento</h3><p class="text-sm text-gray-600">Pix, cartão e boleto. Saque para conta bancária quando quiser, sem valor mínimo.</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">💰</span><h3 class="font-bold mt-1 mb-1">Quanto custa?</h3><p class="text-sm text-gray-600"><strong>Zero mensalidade!</strong> Só R$0,99 + 4,99% por venda. Não vendeu? Não paga nada.</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">🎨</span><h3 class="font-bold mt-1 mb-1">Páginas de Vendas</h3><p class="text-sm text-gray-600">Modelos prontos e profissionais. Escolhe, troca texto e imagem — pronto! Sem programar.</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">🔗</span><h3 class="font-bold mt-1 mb-1">Link Único</h3><p class="text-sm text-gray-600">Cada produto tem um link exclusivo. Venda 24h por dia, automaticamente!</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">📊</span><h3 class="font-bold mt-1 mb-1">Painel em Tempo Real</h3><p class="text-sm text-gray-600">Visitas, vendas, valores e origem dos clientes. Tudo atualizado na hora!</p></div>
                    <div class="p-4 bg-orange-50 rounded-xl"><span class="text-2xl">💬</span><h3 class="font-bold mt-1 mb-1">Suporte em Português</h3><p class="text-sm text-gray-600">Fala sua língua! 🇧🇷 Suporte rápido e eficiente.</p></div>
                </div>
            </div>
        </section>

        <!-- PASSO A PASSO -->
        <section id="sec-passo" class="hidden">
            <div class="bg-white rounded-3xl p-6 card-shadow scroll-container">
                <h2 class="text-2xl font-bold text-gray-800 mb-5">🚀 Passo a Passo — Sua Primeira Venda</h2>
                <div class="space-y-4">
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">📝</div><div><h3 class="font-bold">1. Crie sua Conta</h3><p class="text-sm text-gray-600">kiwify.com.br → "Criar conta". Gratuito, 5 minutos!</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">🏦</div><div><h3 class="font-bold">2. Configure seus Dados</h3><p class="text-sm text-gray-600">Dados bancários em "Configurações".</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">📦</div><div><h3 class="font-bold">3. Crie seu Produto</h3><p class="text-sm text-gray-600">"Novo Produto". Nome com benefício!</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">📤</div><div><h3 class="font-bold">4. Faça o Upload</h3><p class="text-sm text-gray-600">Arquivo (PDF, ZIP, vídeo) ou link externo.</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">🏷️</div><div><h3 class="font-bold">5. Defina o Preço</h3><p class="text-sm text-gray-600">Pense no valor entregue. Pesquise concorrentes.</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">🎨</div><div><h3 class="font-bold">6. Monte sua Página</h3><p class="text-sm text-gray-600">Modelo pronto + título chamativo + benefícios + imagem.</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">🚀</div><div><h3 class="font-bold">7. Publique e Divulgue!</h3><p class="text-sm text-gray-600">Copie seu link e compartilhe!</p></div></div>
                    <div class="flex gap-4 items-start p-4 rounded-xl hover:bg-orange-50 transition-all"><div class="flex-shrink-0 w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-white text-xl">📈</div><div><h3 class="font-bold">8. Acompanhe e Melhore</h3><p class="text-sm text-gray-600">Painel todo dia. Ajuste até acertar!</p></div></div>
                </div>
            </div>
        </section>

        <!-- 100 DICAS -->
        <section id="sec-dicas" class="hidden">
            <div class="bg-white rounded-3xl p-6 card-shadow scroll-container">
                <h2 class="text-2xl font-bold text-gray-800 mb-3">💡 100 Dicas para Vender na Kiwify</h2>
                <p class="text-gray-500 text-sm mb-5">Cada dica com emoji! Deslize pra ver todas! 💪</p>
                <div id="lista-dicas" class="space-y-3 text-sm text-gray-600"></div>
            </div>
        </section>

        <!-- ESPECIALISTA (CHAT) -->
        <section id="sec-chat" class="hidden">
            <div class="bg-white rounded-3xl card-shadow overflow-hidden flex flex-col" style="height: 75vh;">
                <div class="p-4 border-b border-orange-100 flex items-center gap-3 bg-gradient-to-r from-orange-50 to-yellow-50">
                    <div class="w-12 h-12 bg-gradient-to-br from-kiwi-orange to-kiwi-yellow rounded-full flex items-center justify-center text-2xl shadow-lg">🥝</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-gray-800">Especialista Primeira Venda Pro</h3>
                        <p class="text-xs text-green-600 flex items-center gap-1"><span class="w-2 h-2 bg-green-500 rounded-full animate-pulse"></span> Online · Milhares de respostas · Calcula · Gera listas</p>
                    </div>
                    <span class="badge-pro text-white text-[10px] font-bold px-2 py-1 rounded-full">PRO</span>
                </div>
                <div id="chat-mensagens" class="flex-1 overflow-y-auto p-4 space-y-4 text-sm"></div>
                <div class="p-4 border-t border-orange-100 bg-orange-50/30">
                    <form id="form-pergunta" class="flex gap-2">
                        <input type="text" id="entrada-pergunta" placeholder="Pergunte... Ex: me dê 10 opções de como vender na kiwify" class="flex-1 px-4 py-2.5 rounded-full border border-orange-200 bg-white focus:outline-none focus:border-kiwi-orange focus:ring-2 focus:ring-orange-100 text-sm transition-all">
                        <button type="submit" class="bg-gradient-to-r from-kiwi-orange to-kiwi-yellow text-white px-5 py-2.5 rounded-full font-semibold text-sm hover:shadow-lg hover:shadow-orange-200 transition-all"><i class="fa fa-paper-plane"></i></button>
                    </form>
                    <p class="text-[10px] text-gray-400 text-center mt-2">Dica: peça listas! "5 dicas", "10 opções", "20 maneiras..."</p>
                </div>
            </div>
        </section>

        <footer class="text-center mt-6 py-4 text-gray-500 text-xs">
            <p>🥝 <strong>Primeira Venda Pro</strong> — Especialista em Vendas Kiwify · Feito com ❤️</p>
        </footer>
    </div>

    <script>
    // ============================================================
    // 🧠 PRIMEIRA VENDA PRO — CÉREBRO INTELIGENTE
    // +10.000 combinações de respostas via categorias × variações × listas
    // ============================================================

    // ---------- POLO GIGANTE DE ESTRATÉGIAS (para gerar listas) ----------
    const poolEstrategias = [
        "Compartilhe seu link nos status do WhatsApp com um texto persuasivo",
        "Crie conteúdo no Instagram Reels sobre o problema que seu produto resolve",
        "Participe de grupos do Facebook relacionados ao seu nicho e ajude pessoas",
        "Ofereça um cupom de desconto para os 10 primeiros compradores",
        "Peça para amigos e familiares compartilharem seu link",
        "Faça lives no Instagram explicando os benefícios do seu produto",
        "Crie um grupo no Telegram com pessoas interessadas no tema",
        "Use provas sociais: depoimentos de quem já comprou",
        "Invista R$10/dia em anúncios do Instagram/Facebook Ads",
        "Escreva um artigo no Medium ou blog sobre o tema e coloque seu link",
        "Comente em posts de influenciadores do nicho de forma útil",
        "Crie um e-book gratuito como isca digital e ofereça seu produto no final",
        "Use o Pinterest — ele atrai pessoas buscando soluções",
        "Faça parceria com outros produtores para trocar divulgação",
        "Crie um canal no YouTube com vídeos curtos sobre o tema",
        "Use o TikTok — vídeos virais podem trazer muitas vendas",
        "Ofereça garantia de 7 dias para reduzir o medo de comprar",
        "Atualize sua página de vendas com um título mais forte",
        "Teste um preço um pouco mais baixo para as primeiras vendas",
        "Crie um senso de urgência: 'Oferta por tempo limitado'",
        "Responda comentários e mensagens em até 1 hora — velocidade vende",
        "Faça um webinar gratuito e venda no final",
        "Use listas de transmissão no WhatsApp com conteúdo de valor",
        "Crie um quiz divertido relacionado ao tema e indique seu produto",
        "Peça indicação para quem já comprou — dê um bônus em troca",
        "Divulgue em fóruns