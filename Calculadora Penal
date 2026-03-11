<!doctype html>
<html lang="pt-BR" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculadora de Penas GTA RP</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700;900&amp;family=Rajdhani:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    * { font-family: 'Rajdhani', sans-serif; }
    .font-title { font-family: 'Orbitron', monospace; }
    
    @keyframes pulse-glow {
      0%, 100% { box-shadow: 0 0 20px rgba(239, 68, 68, 0.3); }
      50% { box-shadow: 0 0 40px rgba(239, 68, 68, 0.6); }
    }
    
    @keyframes slide-in {
      from { opacity: 0; transform: translateX(-20px); }
      to { opacity: 1; transform: translateX(0); }
    }
    
    .crime-card {
      animation: slide-in 0.3s ease-out forwards;
      opacity: 0;
    }
    
    .result-glow {
      animation: pulse-glow 2s infinite;
    }
    
    .scrollbar-dark::-webkit-scrollbar {
      width: 6px;
    }
    .scrollbar-dark::-webkit-scrollbar-track {
      background: #1f2937;
      border-radius: 3px;
    }
    .scrollbar-dark::-webkit-scrollbar-thumb {
      background: #4b5563;
      border-radius: 3px;
    }
    .scrollbar-dark::-webkit-scrollbar-thumb:hover {
      background: #6b7280;
    }
  </style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-gray-900 text-white overflow-auto">
  <div id="app" class="min-h-full w-full bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 p-4 md:p-6"><!-- Header -->
   <header class="text-center mb-6">
    <div class="inline-flex items-center gap-3 mb-2">
     <svg class="w-10 h-10 text-red-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3" />
     </svg>
     <h1 id="main-title" class="font-title text-2xl md:text-4xl font-bold text-red-500 tracking-wider">CALCULADORA PENAL</h1>
    </div>
    <p id="city-subtitle" class="text-gray-400 text-lg tracking-wide">Departamento Jurídico da Cidade Mídia</p>
   </header>
   <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-3 gap-4 md:gap-6"><!-- Coluna 1: Seleção de Crimes -->
    <div class="lg:col-span-2 space-y-4"><!-- Dados do Processo -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl p-4 border border-gray-700">
      <div class="flex items-center gap-2 mb-4">
       <svg class="w-5 h-5 text-blue-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
       </svg>
       <h2 class="font-semibold text-lg">Dados do Processo</h2>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
       <div>
        <label class="block text-sm text-gray-400 mb-2">Nome do Réu</label><input type="text" id="reu-nome" placeholder="João da Silva" class="w-full px-3 py-2 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500 transition-all">
       </div>
       <div>
        <label class="block text-sm text-gray-400 mb-2">RG do Réu</label><input type="text" id="reu-rg" placeholder="123" class="w-full px-3 py-2 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-600 focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500 transition-all">
       </div>
       <div>
        <label class="block text-sm text-gray-400 mb-2">Nome do Advogado</label><input type="text" id="adv-nome" placeholder="Dr. Carlos Mendes" class="w-full px-3 py-2 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-600 focus:outline-none focus:border-green-500 focus:ring-1 focus:ring-green-500 transition-all">
       </div>
       <div>
        <label class="block text-sm text-gray-400 mb-2">OAB do Advogado</label><input type="text" id="adv-oab" placeholder="123/SP" class="w-full px-3 py-2 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-600 focus:outline-none focus:border-green-500 focus:ring-1 focus:ring-green-500 transition-all">
       </div>
       <div class="md:col-span-2">
        <label class="block text-sm text-gray-400 mb-2">Policiais Participantes (separados por vírgula)</label><textarea id="policiais-nomes" placeholder="Oficial João Silva, Oficial Maria Santos" class="w-full px-3 py-2 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-600 focus:outline-none focus:border-yellow-500 focus:ring-1 focus:ring-yellow-500 transition-all resize-none" rows="2"></textarea>
       </div>
      </div>
     </div><!-- Busca e Filtros -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl p-4 border border-gray-700">
      <div class="flex flex-col sm:flex-row gap-3">
       <div class="flex-1 relative">
        <svg class="absolute left-3 top-1/2 -translate-y-1/2 w-5 h-5 text-gray-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg><input type="text" id="search-input" placeholder="Buscar crime..." class="w-full pl-10 pr-4 py-2.5 bg-gray-900 border border-gray-600 rounded-lg text-white placeholder-gray-500 focus:outline-none focus:border-red-500 focus:ring-1 focus:ring-red-500 transition-all">
       </div><select id="category-filter" class="px-4 py-2.5 bg-gray-900 border border-gray-600 rounded-lg text-white focus:outline-none focus:border-red-500 cursor-pointer"> <option value="all">Todas Categorias</option> <option value="pessoa">Contra a Pessoa</option> <option value="patrimonio">Contra o Patrimônio</option> <option value="ordem">Contra a Ordem Pública</option> <option value="estado">Contra o Estado</option> <option value="transito">Trânsito</option> <option value="drogas">Drogas</option> <option value="armas">Armas</option> </select>
      </div>
     </div><!-- Lista de Crimes -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl border border-gray-700 overflow-hidden">
      <div class="p-3 bg-gray-900/50 border-b border-gray-700 flex items-center justify-between">
       <h2 class="font-semibold text-lg flex items-center gap-2">
        <svg class="w-5 h-5 text-red-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
        </svg> Código Penal</h2><span id="crime-count" class="text-sm text-gray-400">0 crimes</span>
      </div>
      <div id="crimes-list" class="max-h-[400px] overflow-y-auto scrollbar-dark p-3 space-y-2"><!-- Crimes serão inseridos aqui via JS -->
      </div>
     </div><!-- Crimes Selecionados -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl border border-gray-700 overflow-hidden">
      <div class="p-3 bg-gray-900/50 border-b border-gray-700 flex items-center justify-between">
       <h2 class="font-semibold text-lg flex items-center gap-2">
        <svg class="w-5 h-5 text-yellow-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
        </svg> Crimes Imputados</h2><button id="clear-all" class="text-sm text-red-400 hover:text-red-300 transition-colors">Limpar Tudo</button>
      </div>
      <div id="selected-crimes" class="max-h-[250px] overflow-y-auto scrollbar-dark p-3">
       <p id="no-crimes-msg" class="text-gray-500 text-center py-6">Nenhum crime selecionado</p>
       <div id="selected-list" class="space-y-2 hidden"></div>
      </div>
      <div class="p-3 border-t border-gray-700">
       <button id="clear-selected" class="w-full py-2 bg-red-600/20 hover:bg-red-600/30 border border-red-600/50 rounded-lg text-red-400 font-semibold transition-all flex items-center justify-center gap-2">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
        </svg> Remover Selecionados </button>
      </div>
     </div>
    </div><!-- Coluna 2: Atenuantes e Resultado -->
    <div class="space-y-4"><!-- Atenuantes -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl border border-gray-700 overflow-hidden">
      <div class="p-3 bg-gray-900/50 border-b border-gray-700">
       <h2 class="font-semibold text-lg flex items-center gap-2">
        <svg class="w-5 h-5 text-green-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
        </svg> Atenuantes</h2>
      </div>
      <div class="p-3 space-y-3"><label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="att-advogado" class="w-5 h-5 rounded border-gray-600 text-green-500 focus:ring-green-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-green-400 transition-colors">Jurídico Constituído</span>
         <p class="text-sm text-gray-500">-15% da pena total</p>
        </div><span class="text-green-500 font-bold">-15%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="att-confissao" class="w-5 h-5 rounded border-gray-600 text-green-500 focus:ring-green-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-green-400 transition-colors">Reu Confessor</span>
         <p class="text-sm text-gray-500">-10% da pena total</p>
        </div><span class="text-green-500 font-bold">-10%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="att-primario" class="w-5 h-5 rounded border-gray-600 text-green-500 focus:ring-green-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-green-400 transition-colors">Réu Primário</span>
         <p class="text-sm text-gray-500">-10% da pena total</p>
        </div><span class="text-green-500 font-bold">-10%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="att-colaboracao" class="w-5 h-5 rounded border-gray-600 text-green-500 focus:ring-green-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-green-400 transition-colors">Delação Premiada</span>
         <p class="text-sm text-gray-500">-20% da pena total</p>
        </div><span class="text-green-500 font-bold">-20%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="att-bons-antecedentes" class="w-5 h-5 rounded border-gray-600 text-green-500 focus:ring-green-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-green-400 transition-colors">Bons Antecedentes</span>
         <p class="text-sm text-gray-500">-5% da pena total</p>
        </div><span class="text-green-500 font-bold">-5%</span> </label>
      </div>
     </div><!-- Agravantes -->
     <div class="bg-gray-800/80 backdrop-blur rounded-xl border border-gray-700 overflow-hidden">
      <div class="p-3 bg-gray-900/50 border-b border-gray-700">
       <h2 class="font-semibold text-lg flex items-center gap-2">
        <svg class="w-5 h-5 text-red-500" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z" />
        </svg> Agravantes</h2>
      </div>
      <div class="p-3 space-y-3"><label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="agr-reincidente" class="w-5 h-5 rounded border-gray-600 text-red-500 focus:ring-red-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-red-400 transition-colors">Reincidência</span>
         <p class="text-sm text-gray-500">+20% da pena total</p>
        </div><span class="text-red-500 font-bold">+20%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="agr-fuga" class="w-5 h-5 rounded border-gray-600 text-red-500 focus:ring-red-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-red-400 transition-colors">Tentativa de Fuga</span>
         <p class="text-sm text-gray-500">+15% da pena total</p>
        </div><span class="text-red-500 font-bold">+15%</span> </label> <label class="flex items-center gap-3 p-3 bg-gray-900/50 rounded-lg cursor-pointer hover:bg-gray-900 transition-colors group"> <input type="checkbox" id="agr-org-criminosa" class="w-5 h-5 rounded border-gray-600 text-red-500 focus:ring-red-500 focus:ring-offset-gray-800 cursor-pointer">
        <div class="flex-1"><span class="font-medium group-hover:text-red-400 transition-colors">Organização Criminosa</span>
         <p class="text-sm text-gray-500">+25% da pena total</p>
        </div><span class="text-red-500 font-bold">+25%</span> </label>
      </div>
     </div><!-- Resultado Final -->
     <div class="bg-gradient-to-br from-gray-800 to-gray-900 rounded-xl border border-red-900/50 overflow-hidden result-glow">
      <div class="p-3 bg-red-900/20 border-b border-red-900/30">
       <h2 class="font-title font-semibold text-lg flex items-center gap-2 text-red-400">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 11h.01M12 11h.01M9 11h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
        </svg> SENTENÇA FINAL</h2>
      </div>
      <div class="p-4 space-y-4">
       <div class="grid grid-cols-2 gap-3 text-sm">
        <div class="bg-gray-900/50 rounded-lg p-3">
         <p class="text-gray-500 text-xs uppercase tracking-wide">Pena Base</p>
         <p id="base-penalty" class="text-xl font-bold text-white">0 meses</p>
        </div>
        <div class="bg-gray-900/50 rounded-lg p-3">
         <p class="text-gray-500 text-xs uppercase tracking-wide">Multa Base</p>
         <p id="base-fine" class="text-xl font-bold text-yellow-500">R$ 0</p>
        </div>
        <div class="bg-gray-900/50 rounded-lg p-3">
         <p class="text-gray-500 text-xs uppercase tracking-wide">Fiança Base</p>
         <p id="base-bail" class="text-xl font-bold text-cyan-500">R$ 0</p>
        </div>
       </div>
       <div class="space-y-2 text-sm">
        <div class="flex justify-between items-center text-green-400"><span>Atenuantes aplicados:</span> <span id="total-atenuantes">-0%</span>
        </div>
        <div class="flex justify-between items-center text-red-400"><span>Agravantes aplicados:</span> <span id="total-agravantes">+0%</span>
        </div>
       </div>
       <div class="border-t border-gray-700 pt-4">
        <div class="text-center">
         <p class="text-gray-400 text-sm uppercase tracking-wider mb-1">Pena Total</p>
         <p id="final-penalty" class="font-title text-4xl font-black text-red-500">0 MESES</p>
        </div>
        <div class="text-center mt-3">
         <p class="text-gray-400 text-sm uppercase tracking-wider mb-1">Multa Total</p>
         <p id="final-fine" class="font-title text-2xl font-bold text-yellow-500">R$ 0</p>
        </div>
        <div class="text-center mt-3">
         <p class="text-gray-400 text-sm uppercase tracking-wider mb-1">Fiança Total</p>
         <p id="final-bail" class="font-title text-2xl font-bold text-cyan-500">R$ 0</p>
        </div>
       </div><button id="copy-result" class="w-full py-3 bg-red-600 hover:bg-red-500 rounded-lg font-semibold transition-all hover:scale-[1.02] active:scale-[0.98] flex items-center justify-center gap-2">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
        </svg> Copiar Sentença Completa </button>
      </div>
     </div>
    </div>
   </div><!-- Toast Notification -->
   <div id="toast" class="fixed bottom-4 right-4 bg-green-600 text-white px-4 py-3 rounded-lg shadow-lg transform translate-y-20 opacity-0 transition-all duration-300 flex items-center gap-2">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
    </svg><span id="toast-message">Copiado!</span>
   </div>
  </div>
  <script>
    // Configuração padrão
    const defaultConfig = {
      app_title: 'CALCULADORA PENAL',
      city_name: 'Mídia City',
      primary_color: '#111827',
      secondary_color: '#1f2937',
      text_color: '#ffffff',
      accent_color: '#ef4444',
      highlight_color: '#eab308',
      font_family: 'Rajdhani',
      font_size: 16
    };

    // Base de dados de crimes
    const crimes = [
      // Contra a Pessoa
      { id: 1, name: 'Homicídio Qualificado', months: 50, fine: 20000, category: 'pessoa', bailable: false },
      { id: 2, name: 'Feminicídio', months: 35, fine: 20000, category: 'pessoa', bailable: false },
      { id: 3, name: 'Homicídio Culposo', months: 10, fine: 5000, category: 'pessoa', bailable: true },
      { id: 4, name: 'Homicídio Doloso', months: 35, fine: 20000, category: 'pessoa', bailable: false },
      { id: 5, name: 'Homicídio Doloso Qualificado', months: 50, fine: 25000, category: 'pessoa', bailable: false },
      { id: 6, name: 'Induzimento', months: 15, fine: 7000, category: 'pessoa', bailable: true },
      { id: 7, name: 'Tentativa de Homicídio', months: 25, fine: 10000, category: 'pessoa', bailable: false },
      { id: 8, name: 'Lesão Corporal', months: 8, fine: 2000, category: 'pessoa', bailable: true },
      { id: 9, name: 'Lesão Corporal Grave', months: 15, fine: 3000, category: 'pessoa', bailable: true },
      { id: 10, name: 'Lesão Corporal Seguida de Morte', months: 35, fine: 15000, category: 'pessoa', bailable: false },
      { id: 11, name: 'Lesão Corporal Culposa', months: 10, fine: 5000, category: 'pessoa', bailable: true },
      { id: 12, name: 'Lesão Corporal Contra Agente Público', months: 20, fine: 8000, category: 'pessoa', bailable: false },
      { id: 13, name: 'Ameaça', months: 6, fine: 1000, category: 'pessoa', bailable: true },
      { id: 14, name: 'Constrangimento Ilegal', months: 8, fine: 5000, category: 'pessoa', bailable: true },
      { id: 15, name: 'Sequestro e Cárcere Privado', months: 25, fine: 15000, category: 'pessoa', bailable: false },
      { id: 16, name: 'Sequestro', months: 20, fine: 10000, category: 'pessoa', bailable: false },
      { id: 17, name: 'Sequestro Qualificado', months: 30, fine: 20000, category: 'pessoa', bailable: false },
      { id: 18, name: 'Redução à Condição análoga à de escravo', months: 15, fine: 8000, category: 'pessoa', bailable: false },
      { id: 19, name: 'Tráfico de Pessoa', months: 10, fine: 5000, category: 'pessoa', bailable: false },
      { id: 20, name: 'Assédio Sexual', months: 80, fine: 50000, category: 'pessoa', bailable: false },
      { id: 21, name: 'Importunação Sexual', months: 35, fine: 20000, category: 'pessoa', bailable: false },
      { id: 22, name: 'Violação Sexual Mediante Fraude', months: 60, fine: 30000, category: 'pessoa', bailable: false },
      { id: 23, name: 'Divulgação Não Consentida de Conteúdo Íntimo', months: 20, fine: 10000, category: 'pessoa', bailable: true },
      { id: 24, name: 'Exploração Sexual', months: 50, fine: 25000, category: 'pessoa', bailable: true },
      { id: 25, name: 'Omissão de Socorro', months: 15, fine: 6000, category: 'pessoa', bailable: false },
      { id: 26, name: 'Crimes Contra a Honra', months: 20, fine: 20000, category: 'pessoa', bailable: false },

      
      // Contra o Patrimônio
      { id: 27, name: 'Furto', months: 10, fine: 2000, category: 'patrimonio', bailable: true },
      { id: 28, name: 'Furto Qualificado', months: 20, fine: 5000, category: 'patrimonio', bailable: true },
      { id: 29, name: 'Roubo', months: '15', fine: 5000, category: 'patrimonio', bailable: true },
      { id: 30, name: 'Roubo Qualificado', months: 30, fine: 15000, category: 'patrimonio', bailable: true },
      { id: 31, name: 'Extorsão', months: 20, fine: 8000, category: 'patrimonio', bailable: true },
      { id: 32, name: 'Extorsão Mediante Sequestro', months: 40, fine: 16000, category: 'patrimonio', bailable: false },
      { id: 33, name: 'Estelionato', months: 10, fine: 8000, category: 'patrimonio', bailable: true },
      { id: 34, name: 'Dano ao Patrimônio Público', months: 10, fine: 2000, category: 'patrimonio', bailable: true },
      { id: 35, name: 'Dano ao Patrimônio Público Qualificado', months: 15, fine: 4000, category: 'patrimonio', bailable: true },
      { id: 36, name: 'Receptação', months: 10, fine: 2000, category: 'patrimonio', bailable: true },
      
      // Contra a Ordem Pública
      { id: 37, name: 'Desacato', months: 10, fine: 5000, category: 'ordem', bailable: false },
      { id: 38, name: 'Desobediência', months: 10, fine: 2000, category: 'ordem', bailable: true },
      { id: 39, name: 'Resistência', months: 10, fine: 2000, category: 'ordem', bailable: true },
      { id: 40, name: 'Perturbação da Ordem Pública', months: 15, fine: 5000, category: 'ordem', bailable: false },
      { id: 41, name: 'Apologia ao Crime', months: 15, fine: 6000, category: 'ordem', bailable: true },
      
      // Contra o Estado
      { id: 42, name: 'Corrupção Ativa', months: 30, fine: 15000, category: 'estado', bailable: false },
      { id: 43, name: 'Corrupção Passiva', months: 20, fine: 5000, category: 'estado', bailable: false },
      { id: 44, name: 'Peculato', months: 15, fine: 5000, category: 'estado', bailable: true },
      { id: 45, name: 'Prevaricação', months: 15, fine: 5000, category: 'estado', bailable: false },
      { id: 46, name: 'Falsificação de Documento', months: 5, fine: 1000, category: 'estado', bailable: true },
      { id: 47, name: 'Uso de Documento Falso', months: 5, fine: 1000, category: 'estado', bailable: true },
      { id: 48, name: 'Exposição Indevida de Finado', months: 15, fine: 5000, category: 'estado', bailable: true },
      { id: 49, name: 'Falsidade Ideológica', months: 10, fine: 5000, category: 'estado', bailable: true },
      { id: 50, name: 'Falsa Identidade', months: 7, fine: 2000, category: 'estado', bailable: true },
      { id: 51, name: 'Tentativa de Suborno', months: 15, fine: 15000, category: 'estado', bailable: true },
      { id: 52, name: 'Uso Indevido de Equipamento Restrito', months: 15, fine: 8000, category: 'estado', bailable: true },
      { id: 53, name: 'Tráfico de Influência', months: 20, fine: 5000, category: 'estado', bailable: true },
      { id: 54, name: 'Concussão', months: 10, fine: 2000, category: 'estado', bailable: true },
      { id: 55, name: 'Abuso de autoridade', months: 15, fine: 5000, category: 'estado', bailable: false },
      { id: 56, name: 'Omissão Funcional Grave', months: 15, fine: 5000, category: 'estado', bailable: true },

      // Trânsito
      { id: 57, name: 'Direção Perigosa', months: 8, fine: 5000, category: 'transito', bailable: true },
      { id: 58, name: 'Racha', months: 18, fine: 10000, category: 'transito', bailable: true },
      { id: 59, name: 'Fuga de Blitz', months: 15, fine: 7000, category: 'transito', bailable: true },
      { id: 60, name: 'Atropelamento', months: 10, fine: 2000, category: 'transito', bailable: true },
      
      // Drogas
      { id: 61, name: 'Posse Irregular de Substância Entorpecente', months: 15, fine: 10000, category: 'drogas', bailable: true },
      { id: 62, name: 'Tráfico de Drogas', months: 15, fine: 8000, category: 'drogas', bailable: true },
      { id: 63, name: 'Tráfico Internacional', months: 144, fine: 150000, category: 'drogas', bailable: true },
      { id: 64, name: 'Cultivo de Drogas', months: 60, fine: 40000, category: 'drogas', bailable: true },
      { id: 65, name: 'Associação ao Tráfico', months: 20, fine: 10000, category: 'drogas', bailable: true },
      { id: 66, name: 'Tráfico de Matéria-Prima Ilícita', months: 16, fine: 10000, category: 'drogas', bailable: true },
      // Armas
      { id: 67, name: 'Porte Ilegal de Arma', months: 24, fine: 15000, category: 'armas', bailable: true },
      { id: 68, name: 'Disparo de Arma de Fogo', months: 24, fine: 12000, category: 'armas', bailable: true },
      { id: 69, name: 'Tráfico de Armas', months: 25, fine: 10000, category: 'armas', bailable: true },
      { id: 70, name: 'Porte de Arma Pesada', months: 48, fine: 30000, category: 'armas', bailable: true },
      { id: 71, name: 'Fabricação de Armas', months: 72, fine: 50000, category: 'armas', bailable: true },
      { id: 72, name: 'Porte ou Irregular de Arma de Uso Permitido', months: 20, fine: 10000, category: 'armas', bailable: true },
      { id: 73, name: 'Tráfico de Munições e Explosivos', months: 25, fine: 10000, category: 'armas', bailable: true },
      { id: 74, name: 'Posse Irregular de Munição, Explosivo ou Artefato Controlado', months: 15, fine: 5000, category: 'armas', bailable: true },
      { id: 75, name: 'Tráfico de Colete Balístico', months: 25, fine: 10000, category: 'armas', bailable: true },
      { id: 76, name: 'Posse de Itens Ilegais', months: 8, fine: 5000, category: 'armas', bailable: true }
    ];

    // Estado da aplicação
    let selectedCrimes = [];
    let currentConfig = { ...defaultConfig };

    // Categorias com cores
    const categoryColors = {
      pessoa: { bg: 'bg-red-900/30', border: 'border-red-700/50', text: 'text-red-400', label: 'Contra a Pessoa' },
      patrimonio: { bg: 'bg-yellow-900/30', border: 'border-yellow-700/50', text: 'text-yellow-400', label: 'Contra o Patrimônio' },
      ordem: { bg: 'bg-blue-900/30', border: 'border-blue-700/50', text: 'text-blue-400', label: 'Contra a Ordem Pública' },
      estado: { bg: 'bg-purple-900/30', border: 'border-purple-700/50', text: 'text-purple-400', label: 'Contra o Estado' },
      transito: { bg: 'bg-cyan-900/30', border: 'border-cyan-700/50', text: 'text-cyan-400', label: 'Trânsito' },
      drogas: { bg: 'bg-green-900/30', border: 'border-green-700/50', text: 'text-green-400', label: 'Drogas' },
      armas: { bg: 'bg-orange-900/30', border: 'border-orange-700/50', text: 'text-orange-400', label: 'Armas' }
    };

    // Renderizar lista de crimes
    function renderCrimesList(filter = 'all', search = '') {
      const container = document.getElementById('crimes-list');
      const countEl = document.getElementById('crime-count');
      
      let filteredCrimes = crimes;
      
      if (filter !== 'all') {
        filteredCrimes = filteredCrimes.filter(c => c.category === filter);
      }
      
      if (search) {
        const searchLower = search.toLowerCase();
        filteredCrimes = filteredCrimes.filter(c => 
          c.name.toLowerCase().includes(searchLower)
        );
      }
      
      countEl.textContent = `${filteredCrimes.length} crimes`;
      
      container.innerHTML = filteredCrimes.map((crime, index) => {
        const cat = categoryColors[crime.category];
        const isSelected = selectedCrimes.some(sc => sc.id === crime.id);
        
        return `
          <div class="crime-card ${cat.bg} ${cat.border} border rounded-lg p-3 cursor-pointer hover:scale-[1.02] transition-all ${isSelected ? 'ring-2 ring-white/50' : ''}"
               style="animation-delay: ${index * 30}ms"
               onclick="toggleCrime(${crime.id})">
            <div class="flex items-center justify-between">
              <div class="flex-1">
                <div class="flex items-center gap-2">
                  <span class="font-semibold text-white">${crime.name}</span>
                  ${isSelected ? '<svg class="w-4 h-4 text-green-400" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/></svg>' : ''}
                </div>
                <span class="text-xs ${cat.text}">${cat.label}</span>
              </div>
              <div class="text-right">
                <p class="font-bold text-white">${crime.months} meses</p>
                <p class="text-xs text-yellow-500">R$ ${crime.fine.toLocaleString('pt-BR')}</p>
              </div>
            </div>
          </div>
        `;
      }).join('');
    }

    // Toggle crime selecionado
    function toggleCrime(crimeId) {
      const crime = crimes.find(c => c.id === crimeId);
      const index = selectedCrimes.findIndex(sc => sc.id === crimeId);
      
      if (index > -1) {
        selectedCrimes.splice(index, 1);
      } else {
        selectedCrimes.push({ ...crime, quantity: 1 });
      }
      
      renderCrimesList(
        document.getElementById('category-filter').value,
        document.getElementById('search-input').value
      );
      renderSelectedCrimes();
      calculatePenalty();
    }

    // Renderizar crimes selecionados
    function renderSelectedCrimes() {
      const noMsg = document.getElementById('no-crimes-msg');
      const list = document.getElementById('selected-list');
      
      if (selectedCrimes.length === 0) {
        noMsg.classList.remove('hidden');
        list.classList.add('hidden');
        return;
      }
      
      noMsg.classList.add('hidden');
      list.classList.remove('hidden');
      
      list.innerHTML = selectedCrimes.map(crime => {
        const cat = categoryColors[crime.category];
        return `
          <div class="flex items-center gap-3 ${cat.bg} ${cat.border} border rounded-lg p-2">
            <div class="flex-1">
              <p class="font-medium text-sm">${crime.name}</p>
              <p class="text-xs text-gray-400">${crime.months * crime.quantity} meses • R$ ${(crime.fine * crime.quantity).toLocaleString('pt-BR')}</p>
            </div>
            <div class="flex items-center gap-1">
              <button onclick="updateQuantity(${crime.id}, -1)" class="w-7 h-7 bg-gray-700 hover:bg-gray-600 rounded flex items-center justify-center transition-colors">−</button>
              <span class="w-8 text-center font-bold">${crime.quantity}x</span>
              <button onclick="updateQuantity(${crime.id}, 1)" class="w-7 h-7 bg-gray-700 hover:bg-gray-600 rounded flex items-center justify-center transition-colors">+</button>
            </div>
            <button onclick="removeCrime(${crime.id})" class="w-7 h-7 bg-red-900/50 hover:bg-red-800 rounded flex items-center justify-center transition-colors">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
              </svg>
            </button>
          </div>
        `;
      }).join('');
    }

    // Atualizar quantidade
    function updateQuantity(crimeId, delta) {
      const crime = selectedCrimes.find(sc => sc.id === crimeId);
      if (crime) {
        crime.quantity = Math.max(1, crime.quantity + delta);
        renderSelectedCrimes();
        calculatePenalty();
      }
    }

    // Remover crime
    function removeCrime(crimeId) {
      selectedCrimes = selectedCrimes.filter(sc => sc.id !== crimeId);
      renderCrimesList(
        document.getElementById('category-filter').value,
        document.getElementById('search-input').value
      );
      renderSelectedCrimes();
      calculatePenalty();
    }

    // Calcular pena
    function calculatePenalty() {
      const MAX_PENALTY_MONTHS = 150; // Limite máximo de pena em meses
      
      let baseMonths = 0;
      let baseFine = 0;
      let baseBail = 0; // Fiança inicial
      let hasNonBailable = false; // Verifica se há crimes inafiançáveis
      
      selectedCrimes.forEach(crime => {
        baseMonths += crime.months * crime.quantity;
        baseFine += crime.fine * crime.quantity;
        // Fiança é 40% da multa (se o crime for afiançável)
        if (crime.bailable) {
          baseBail += (crime.fine * 0.4) * crime.quantity;
        } else {
          hasNonBailable = true;
        }
      });
      
      // Calcular atenuantes
      let atenuantesPercent = 0;
      if (document.getElementById('att-advogado').checked) atenuantesPercent += 15;
      if (document.getElementById('att-confissao').checked) atenuantesPercent += 10;
      if (document.getElementById('att-primario').checked) atenuantesPercent += 10;
      if (document.getElementById('att-colaboracao').checked) atenuantesPercent += 20;
      if (document.getElementById('att-bons-antecedentes').checked) atenuantesPercent += 5;
      
      // Calcular agravantes
      let agravantesPercent = 0;
      if (document.getElementById('agr-reincidente').checked) agravantesPercent += 20;
      if (document.getElementById('agr-fuga').checked) agravantesPercent += 15;
      if (document.getElementById('agr-org-criminosa').checked) agravantesPercent += 25;
      
      // Calcular pena final com limite de 150 meses
      const totalModifier = 1 + (agravantesPercent / 100) - (atenuantesPercent / 100);
      let finalMonths = Math.max(0, Math.round(baseMonths * totalModifier));
      
      // Aplicar limite de 150 meses (a pena não aumenta mais, mas contabiliza os crimes)
      if (finalMonths > MAX_PENALTY_MONTHS) {
        finalMonths = MAX_PENALTY_MONTHS;
      }
      
      // A multa e fiança continuam somando normalmente sem limite
      const finalFine = Math.max(0, Math.round(baseFine * totalModifier));
      const finalBail = hasNonBailable ? 0 : Math.max(0, Math.round(baseBail * totalModifier));
      
      // Atualizar UI
      document.getElementById('base-penalty').textContent = `${baseMonths} meses`;
      document.getElementById('base-fine').textContent = `R$ ${baseFine.toLocaleString('pt-BR')}`;
      const baseBailEl = document.getElementById('base-bail');
      baseBailEl.textContent = hasNonBailable ? 'INAFIANÇÁVEL' : `R$ ${baseBail.toLocaleString('pt-BR')}`;
      baseBailEl.className = hasNonBailable ? 'text-xl font-bold text-red-500' : 'text-xl font-bold text-cyan-500';
      document.getElementById('total-atenuantes').textContent = `-${atenuantesPercent}%`;
      document.getElementById('total-agravantes').textContent = `+${agravantesPercent}%`;
      document.getElementById('final-penalty').textContent = `${finalMonths} MESES${finalMonths >= MAX_PENALTY_MONTHS && baseMonths * totalModifier > MAX_PENALTY_MONTHS ? ' (LIMITE MÁXIMO ATINGIDO)' : ''}`;
      document.getElementById('final-fine').textContent = `R$ ${finalFine.toLocaleString('pt-BR')}`;
      const finalBailEl = document.getElementById('final-bail');
      finalBailEl.textContent = hasNonBailable ? 'CRIME INAFIANÇÁVEL' : `R$ ${finalBail.toLocaleString('pt-BR')}`;
      finalBailEl.className = hasNonBailable ? 'font-title text-2xl font-bold text-red-500' : 'font-title text-2xl font-bold text-cyan-500';
    }

    // Copiar resultado
    function copyResult() {
      const reuNome = document.getElementById('reu-nome').value || 'Não informado';
      const reuRg = document.getElementById('reu-rg').value || 'Não informado';
      const advNome = document.getElementById('adv-nome').value || 'Não informado';
      const advOab = document.getElementById('adv-oab').value || 'Não informado';
      const policiais = document.getElementById('policiais-nomes').value || 'Não informado';
      
      // Gerar lista detalhada de crimes com multas
      let crimesDetalhados = '';
      selectedCrimes.forEach(c => {
        const multa = c.fine * c.quantity;
        crimesDetalhados += `   • ${c.name} (x${c.quantity}) - R$ ${multa.toLocaleString('pt-BR')}\n`;
      });
      
      const basePenalty = document.getElementById('base-penalty').textContent;
      const baseFine = document.getElementById('base-fine').textContent;
      const baseBail = document.getElementById('base-bail').textContent;
      const finalPenalty = document.getElementById('final-penalty').textContent;
      const finalFine = document.getElementById('final-fine').textContent;
      const finalBail = document.getElementById('final-bail').textContent;
      const atenuantes = document.getElementById('total-atenuantes').textContent;
      const agravantes = document.getElementById('total-agravantes').textContent;
      
      let atenuantesList = [];
      if (document.getElementById('att-advogado').checked) atenuantesList.push('Jurídico Constituído (-15%)');
      if (document.getElementById('att-confissao').checked) atenuantesList.push('Confissão Espontânea (-10%)');
      if (document.getElementById('att-primario').checked) atenuantesList.push('Réu Primário (-10%)');
      if (document.getElementById('att-colaboracao').checked) atenuantesList.push('Colaboração Premiada (-20%)');
      if (document.getElementById('att-bons-antecedentes').checked) atenuantesList.push('Bons Antecedentes (-5%)');
      
      let agravantesList = [];
      if (document.getElementById('agr-reincidente').checked) agravantesList.push('Reincidência (+20%)');
      if (document.getElementById('agr-fuga').checked) agravantesList.push('Tentativa de Fuga (+15%)');
      if (document.getElementById('agr-org-criminosa').checked) agravantesList.push('Organização Criminosa (+25%)');
      
      const text = `
╔═══════════════════════════════════════════════════════╗
║                  SENTENÇA JUDICIAL                    ║
║     Departamento Jurídico da Cidade Mídia             ║
╚═══════════════════════════════════════════════════════╝

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📋 IDENTIFICAÇÃO DO RÉU:

   Nome do Réu: ${reuNome}
   RG: ${reuRg}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

⚖️ REPRESENTAÇÃO LEGAL:

   Advogado(a): ${advNome}
   OAB: ${advOab}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

👮 AUTORIDADES PARTICIPANTES:

   ${policiais}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

⚡ CRIMES IMPUTADOS:

${crimesDetalhados || '   • Nenhum crime selecionado'}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📊 CÁLCULO DETALHADO:

   Pena Base: ${basePenalty}
   Multa Base: ${baseFine}
   Fiança Base: ${baseBail}

✅ ATENUANTES APLICADOS (${atenuantes}):
${atenuantesList.length > 0 ? atenuantesList.map(a => `   • ${a}`).join('\n') : '   • Nenhum atenuante aplicado'}

❌ AGRAVANTES APLICADOS (${agravantes}):
${agravantesList.length > 0 ? agravantesList.map(a => `   • ${a}`).join('\n') : '   • Nenhum agravante aplicado'}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🔨 SENTENÇA FINAL CONDENATÓRIA:

   ⏱️  PENA PRIVATIVA DE LIBERDADE: ${finalPenalty}
   
   💰 MULTA CONDENATÓRIA: ${finalFine}
   
   🔒 FIANÇA: ${finalBail}

╔═══════════════════════════════════════════════════════╗
║     Documento gerado automaticamente pelo Sistema     ║
║        de Justiça da Cidade Mídia                     ║
╚═══════════════════════════════════════════════════════╝
      `.trim();
      
      navigator.clipboard.writeText(text).then(() => {
        showToast('Sentença copiada com sucesso!');
      });
    }

    // Mostrar toast
    function showToast(message) {
      const toast = document.getElementById('toast');
      const toastMessage = document.getElementById('toast-message');
      toastMessage.textContent = message;
      toast.classList.remove('translate-y-20', 'opacity-0');
      
      setTimeout(() => {
        toast.classList.add('translate-y-20', 'opacity-0');
      }, 2500);
    }

    // Event Listeners
    document.getElementById('search-input').addEventListener('input', (e) => {
      renderCrimesList(document.getElementById('category-filter').value, e.target.value);
    });

    document.getElementById('category-filter').addEventListener('change', (e) => {
      renderCrimesList(e.target.value, document.getElementById('search-input').value);
    });

    document.getElementById('clear-all').addEventListener('click', () => {
      selectedCrimes = [];
      document.querySelectorAll('input[type="checkbox"]').forEach(cb => cb.checked = false);
      renderCrimesList(
        document.getElementById('category-filter').value,
        document.getElementById('search-input').value
      );
      renderSelectedCrimes();
      calculatePenalty();
    });

    document.getElementById('clear-selected').addEventListener('click', () => {
      selectedCrimes = [];
      document.querySelectorAll('input[type="checkbox"]').forEach(cb => cb.checked = false);
      renderCrimesList(
        document.getElementById('category-filter').value,
        document.getElementById('search-input').value
      );
      renderSelectedCrimes();
      calculatePenalty();
    });

    document.getElementById('copy-result').addEventListener('click', copyResult);

    // Listeners para checkboxes
    document.querySelectorAll('input[type="checkbox"]').forEach(cb => {
      cb.addEventListener('change', calculatePenalty);
    });

    // Element SDK
    async function onConfigChange(config) {
      currentConfig = { ...defaultConfig, ...config };
      
      // Atualizar título
      const titleEl = document.getElementById('main-title');
      if (titleEl) titleEl.textContent = config.app_title || defaultConfig.app_title;
      
      // Atualizar nome da cidade
      const cityEl = document.getElementById('city-subtitle');
      if (cityEl) cityEl.textContent = `Departamento de Justiça • ${config.city_name || defaultConfig.city_name}`;
      
      // Aplicar cores
      document.body.style.setProperty('--primary-color', config.primary_color || defaultConfig.primary_color);
      document.body.style.setProperty('--accent-color', config.accent_color || defaultConfig.accent_color);
      
      // Aplicar fonte
      const fontFamily = config.font_family || defaultConfig.font_family;
      document.body.style.fontFamily = `${fontFamily}, sans-serif`;
      
      // Aplicar tamanho de fonte
      const fontSize = config.font_size || defaultConfig.font_size;
      document.body.style.fontSize = `${fontSize}px`;
    }

    function mapToCapabilities(config) {
      return {
        recolorables: [
          {
            get: () => config.primary_color || defaultConfig.primary_color,
            set: (value) => { config.primary_color = value; window.elementSdk.setConfig({ primary_color: value }); }
          },
          {
            get: () => config.secondary_color || defaultConfig.secondary_color,
            set: (value) => { config.secondary_color = value; window.elementSdk.setConfig({ secondary_color: value }); }
          },
          {
            get: () => config.text_color || defaultConfig.text_color,
            set: (value) => { config.text_color = value; window.elementSdk.setConfig({ text_color: value }); }
          },
          {
            get: () => config.accent_color || defaultConfig.accent_color,
            set: (value) => { config.accent_color = value; window.elementSdk.setConfig({ accent_color: value }); }
          },
          {
            get: () => config.highlight_color || defaultConfig.highlight_color,
            set: (value) => { config.highlight_color = value; window.elementSdk.setConfig({ highlight_color: value }); }
          }
        ],
        borderables: [],
        fontEditable: {
          get: () => config.font_family || defaultConfig.font_family,
          set: (value) => { config.font_family = value; window.elementSdk.setConfig({ font_family: value }); }
        },
        fontSizeable: {
          get: () => config.font_size || defaultConfig.font_size,
          set: (value) => { config.font_size = value; window.elementSdk.setConfig({ font_size: value }); }
        }
      };
    }

    function mapToEditPanelValues(config) {
      return new Map([
        ['app_title', config.app_title || defaultConfig.app_title],
        ['city_name', config.city_name || defaultConfig.city_name]
      ]);
    }

    // Inicialização
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities,
        mapToEditPanelValues
      });
    }

    // Renderizar inicial
    renderCrimesList();
    renderSelectedCrimes();
    calculatePenalty();
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9da1f0f077fa6449',t:'MTc3MzE0MTc0Mi4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
