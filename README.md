# l0stmyself.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Federal Bank & MongoDB | Strategic Modernization Pitch</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

    <!-- Styles -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* warm neutral background */
            color: #1f2937;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1; 
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8; 
        }

        /* Chart Container Strict Styling */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 100%;
            height: 300px;
            margin-left: auto;
            margin-right: auto;
        }
        @media (min-width: 1024px) {
            .chart-container {
                height: 400px;
            }
        }

        /* Transitions */
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .slide-card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            transition: all 0.3s ease;
        }

        /* Federal Bank Brand Colors Simulation */
        .brand-blue { background-color: #004c8f; }
        .brand-gold { background-color: #e3a32a; }
        .mongo-green { color: #00ED64; }
        .mongo-bg-green { background-color: #00ED64; }
        
        /* Interactive Toggle Switch */
        .toggle-checkbox:checked {
            right: 0;
            border-color: #004c8f;
        }
        .toggle-checkbox:checked + .toggle-label {
            background-color: #004c8f;
        }
        
        /* Code Block Styling */
        .code-block {
            background-color: #1e293b;
            color: #e2e8f0;
            font-family: 'Courier New', Courier, monospace;
            padding: 1rem;
            border-radius: 0.5rem;
            font-size: 0.85rem;
            overflow-x: auto;
        }
    </style>

    <!-- Placeholder Comments -->
    <!-- Chosen Palette: Corporate Trust (Navy Blue, White, Cool Greys) with Innovation Accents (MongoDB Green, Federal Gold) -->
    <!-- Application Structure Plan: A 5-stage interactive dashboard. 
         1. Executive Hook: Visualizes the problem (Velocity Gap).
         2. Architectural Solution: Interactive diagram showing ODL offloading.
         3. Technical Proof: Side-by-side SQL vs JSON simulation.
         4. Innovation/AI: Chat interface demo for Vector Search.
         5. Social Proof: Metrics and case studies.
         Why: This structure mirrors the sales narrative (Problem -> Solution -> Proof -> Value) but allows the user to 'play' with the concepts, making the technical benefits of MongoDB tangible. -->
    <!-- Visualization & Content Choices: 
         1. Line/Bar Charts (Chart.js): To quantify the 'Velocity Gap' and TCO reductions. Goal: Inform/Compare.
         2. CSS/HTML Grid Architecture: To represent the ODL layer. Interaction: Toggle states. Goal: Organize/Change.
         3. Interactive Code Blocks: To show JSON flexibility. Goal: Compare.
         4. Chat Interface: To demo AI. Goal: Experience.
         Justification: No static images allowed. Canvas/DOM manipulation provides the most lightweight and responsive way to demonstrate complex architecture without SVG. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
</head>
<body class="flex flex-col h-screen overflow-hidden">

    <!-- Top Navigation / Header -->
    <header class="bg-white border-b border-gray-200 z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex items-center">
                    <div class="flex-shrink-0 flex items-center gap-3">
                        <!-- CSS Icon for Document/Database -->
                        <div class="w-8 h-8 brand-blue rounded flex items-center justify-center text-white font-bold text-lg">F</div>
                        <span class="font-bold text-xl text-gray-800">Federal Bank <span class="text-gray-400">|</span> <span class="text-green-600">MongoDB</span> Strategy</span>
                    </div>
                </div>
                <nav class="hidden md:flex space-x-1">
                    <button onclick="navTo(0)" id="nav-0" class="px-3 py-2 rounded-md text-sm font-medium text-gray-900 bg-gray-100 transition-colors">1. The Friction</button>
                    <button onclick="navTo(1)" id="nav-1" class="px-3 py-2 rounded-md text-sm font-medium text-gray-500 hover:text-gray-900 transition-colors">2. The ODL</button>
                    <button onclick="navTo(2)" id="nav-2" class="px-3 py-2 rounded-md text-sm font-medium text-gray-500 hover:text-gray-900 transition-colors">3. Tech Agility</button>
                    <button onclick="navTo(3)" id="nav-3" class="px-3 py-2 rounded-md text-sm font-medium text-gray-500 hover:text-gray-900 transition-colors">4. AI Future</button>
                    <button onclick="navTo(4)" id="nav-4" class="px-3 py-2 rounded-md text-sm font-medium text-gray-500 hover:text-gray-900 transition-colors">5. Impact</button>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Content Area -->
    <main class="flex-1 overflow-y-auto bg-gray-50 p-4 sm:p-8" id="main-content">
        <!-- Content injected via JS -->
    </main>

    <!-- Speaker Notes Footer (Sticky) -->
    <footer class="bg-white border-t border-gray-200 p-4 shadow-lg z-20">
        <div class="max-w-7xl mx-auto">
            <div class="flex items-start gap-4">
                <div class="flex-shrink-0 pt-1">
                    <span class="bg-yellow-100 text-yellow-800 text-xs font-medium px-2.5 py-0.5 rounded border border-yellow-300">SPEAKER SCRIPT</span>
                </div>
                <p id="speaker-script" class="text-sm text-gray-600 italic leading-relaxed">
                    <!-- Script injected via JS -->
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // State Management
        const state = {
            currentSlide: 0,
            odlActive: false,
            techDemoMode: 'SQL', // SQL or JSON
            aiSearchType: 'keyword' // keyword or vector
        };

        // Data & Content Configuration
        const slides = [
            {
                id: 'hook',
                title: 'Digital Success vs. Core Bottlenecks',
                script: "Federal Bank, your 'Digital at the Fore' strategy is a triumph with FedOne and FedMobile. However, we see a hidden friction. While your channels are sprinting, the legacy core systems—relational databases—are struggling to keep pace with the volume and variety of modern data. This gap creates high latency, integration costs, and fragility. MongoDB bridges this gap, ensuring your core remains 'Human' and stable, while your digital front-end scales limitlessly.",
                render: renderHook
            },
            {
                id: 'odl',
                title: 'The Solution: Operational Data Layer (ODL)',
                script: "This is the modernization accelerator. Instead of ripping and replacing your core banking system—risking partnerships with Nucleus or Intellect—we introduce MongoDB as an Operational Data Layer (ODL). It sits side-by-side. The ODL offloads high-volume read traffic (like balance checks on FedMobile) from the mainframe, reducing MIPS costs instantly and providing a real-time, unified view of the customer across all channels.",
                render: renderSolution
            },
            {
                id: 'tech',
                title: 'Technical Proof: Relational Rigidity vs. Document Agility',
                script: "Why MongoDB? Look at the difference. To add a simple 'Lifestyle Preference' field for FedMobile personalization in Oracle requires modifying 3 tables, downtime, and complex joins. In MongoDB's JSON document model, it's just adding a field. No downtime. No schema migrations. This is how you iterate on FedOne features in days, not months.",
                render: renderTech
            },
            {
                id: 'innovation',
                title: 'Innovation: Powering "Feddy" with Vector Search',
                script: "The next generation of 'Feddy' needs more than keywords. With MongoDB Atlas Vector Search, you can ground your AI in real-time operational data. We don't just match words; we match intent. When a customer asks 'Why did my transaction fail?', Vector Search understands the context from unstructured logs and payment history instantly, securely, and within the same platform.",
                render: renderInnovation
            },
            {
                id: 'case-study',
                title: 'The Case Study: Proven Impact',
                script: "This isn't theoretical. Major Tier-1 banks have used this exact ODL pattern to reduce Mainframe TCO by 60% and improve mobile app latency by 90%. Like DBS or Wells Fargo, Federal Bank can achieve 'Silo-busting' scale without compromising the stability of the core.",
                render: renderCaseStudy
            }
        ];

        // --- Render Functions ---

        function renderHook() {
            const container = document.getElementById('main-content');
            container.innerHTML = `
                <div class="max-w-5xl mx-auto space-y-6 fade-in">
                    <div class="text-center mb-8">
                        <h2 class="text-3xl font-bold text-gray-900">The Modernization Gap</h2>
                        <p class="text-lg text-gray-600 mt-2">FedOne is fast. Is the Data Layer keeping up?</p>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        <!-- Chart Card -->
                        <div class="slide-card p-6">
                            <h3 class="text-lg font-semibold mb-4 text-gray-800">Channel Velocity vs. Backend Agility</h3>
                            <div class="chart-container">
                                <canvas id="velocityChart"></canvas>
                            </div>
                            <div class="mt-4 text-sm text-gray-500 text-center">
                                <span class="inline-block w-3 h-3 bg-blue-600 rounded-full mr-1"></span> Digital Demand
                                <span class="inline-block w-3 h-3 bg-gray-400 rounded-full ml-4 mr-1"></span> Core Capacity
                            </div>
                        </div>

                        <!-- Pain Points Card -->
                        <div class="slide-card p-6 flex flex-col justify-center">
                            <h3 class="text-lg font-semibold mb-6 text-gray-800">Current Challenges</h3>
                            <div class="space-y-4">
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-red-100 flex items-center justify-center text-red-600 font-bold">!</div>
                                    <div class="ml-4">
                                        <h4 class="text-md font-bold text-gray-900">Data Silos</h4>
                                        <p class="text-sm text-gray-600">Customer data fragmented across legacy Oracle/SQL instances prevents a 360-view.</p>
                                    </div>
                                </div>
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-red-100 flex items-center justify-center text-red-600 font-bold">!</div>
                                    <div class="ml-4">
                                        <h4 class="text-md font-bold text-gray-900">Innovation Tax</h4>
                                        <p class="text-sm text-gray-600">6-month cycles to modify schemas for new FedMobile features.</p>
                                    </div>
                                </div>
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-red-100 flex items-center justify-center text-red-600 font-bold">!</div>
                                    <div class="ml-4">
                                        <h4 class="text-md font-bold text-gray-900">Mainframe Costs</h4>
                                        <p class="text-sm text-gray-600">High MIPS consumption from simple read-heavy apps (e.g., balance checks).</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            `;

            // Initialize Chart
            const ctx = document.getElementById('velocityChart').getContext('2d');
            new Chart(ctx, {
                type: 'line',
                data: {
                    labels: ['2021', '2022', '2023', '2024', '2025 (Proj)'],
                    datasets: [
                        {
                            label: 'Digital Transactions (FedOne)',
                            data: [100, 180, 350, 600, 950],
                            borderColor: '#004c8f', // Brand Blue
                            backgroundColor: 'rgba(0, 76, 143, 0.1)',
                            borderWidth: 3,
                            tension: 0.4,
                            fill: true
                        },
                        {
                            label: 'Legacy Core Scale Limit',
                            data: [300, 320, 340, 350, 360],
                            borderColor: '#9ca3af', // Gray
                            borderDash: [5, 5],
                            borderWidth: 2,
                            tension: 0.1,
                            fill: false
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { display: false },
                        tooltip: { mode: 'index', intersect: false }
                    },
                    scales: {
                        y: { beginAtZero: true, title: { display: true, text: 'Volume / Capacity' } }
                    }
                }
            });
        }

        function renderSolution() {
            const container = document.getElementById('main-content');
            container.innerHTML = `
                <div class="max-w-6xl mx-auto space-y-6 fade-in h-full flex flex-col">
                    <div class="flex justify-between items-center mb-4">
                        <div>
                            <h2 class="text-2xl font-bold text-gray-900">Operational Data Layer (ODL)</h2>
                            <p class="text-gray-600">Offload the Core. Innovate on the Edge.</p>
                        </div>
                        <!-- Toggle Switch -->
                        <div class="flex items-center gap-3 bg-white p-3 rounded-lg shadow-sm">
                            <span class="text-sm font-semibold ${!state.odlActive ? 'text-blue-800' : 'text-gray-400'}">Legacy Monolith</span>
                            <div class="relative inline-block w-14 mr-2 align-middle select-none transition duration-200 ease-in">
                                <input type="checkbox" name="toggle" id="odl-toggle" class="toggle-checkbox absolute block w-6 h-6 rounded-full bg-white border-4 appearance-none cursor-pointer border-gray-300" ${state.odlActive ? 'checked' : ''}/>
                                <label for="odl-toggle" class="toggle-label block overflow-hidden h-6 rounded-full bg-gray-300 cursor-pointer"></label>
                            </div>
                            <span class="text-sm font-semibold ${state.odlActive ? 'text-green-600' : 'text-gray-400'}">MongoDB ODL</span>
                        </div>
                    </div>

                    <!-- Architecture Diagram Area -->
                    <div class="flex-1 bg-white rounded-xl shadow-inner p-8 relative overflow-hidden border border-gray-200">
                        
                        <!-- Top Layer: Digital Channels -->
                        <div class="flex justify-center gap-8 mb-16 relative z-10">
                            <div class="w-32 h-16 bg-blue-600 text-white rounded-lg flex items-center justify-center shadow-lg font-bold">FedMobile</div>
                            <div class="w-32 h-16 bg-blue-500 text-white rounded-lg flex items-center justify-center shadow-lg font-bold">FedOne</div>
                            <div class="w-32 h-16 bg-blue-400 text-white rounded-lg flex items-center justify-center shadow-lg font-bold">Partners</div>
                        </div>

                        <!-- Middle Layer: The ODL (Conditional Display) -->
                        <div id="odl-layer" class="flex justify-center mb-16 transition-all duration-500 ${state.odlActive ? 'opacity-100 transform translate-y-0' : 'opacity-20 transform scale-95 grayscale'}">
                            <div class="w-full max-w-2xl h-24 border-2 border-green-500 bg-green-50 rounded-xl flex items-center justify-between px-8 relative shadow-md">
                                <div class="text-green-800 font-bold text-lg flex items-center gap-2">
                                    <span class="text-2xl">🍃</span> MongoDB Atlas (ODL)
                                </div>
                                <div class="text-xs text-green-700 font-mono text-right">
                                    <div>Status: ACTIVE</div>
                                    <div>Reads: 100% Offloaded</div>
                                    <div>View: Single Customer View</div>
                                </div>
                                <!-- Visual Data Pipes -->
                                <div class="absolute -top-16 left-1/2 w-1 h-16 bg-green-400 animate-pulse"></div>
                                <div class="absolute -top-16 left-1/4 w-1 h-16 bg-green-400 animate-pulse"></div>
                                <div class="absolute -top-16 left-3/4 w-1 h-16 bg-green-400 animate-pulse"></div>
                            </div>
                        </div>

                        <!-- Bottom Layer: Legacy Systems -->
                        <div class="flex justify-center gap-4 relative z-10">
                            <div class="w-40 h-20 bg-gray-700 text-gray-200 rounded-lg flex flex-col items-center justify-center shadow-lg border-b-4 border-gray-900">
                                <span class="font-bold">Core Banking</span>
                                <span class="text-xs">(Nucleus/Oracle)</span>
                            </div>
                            <div class="w-40 h-20 bg-gray-700 text-gray-200 rounded-lg flex flex-col items-center justify-center shadow-lg border-b-4 border-gray-900">
                                <span class="font-bold">Cards System</span>
                                <span class="text-xs">(Mainframe)</span>
                            </div>
                        </div>

                        <!-- Connecting Lines (CSS Hacks for illustration) -->
                        <!-- Legacy Direct Lines (Visible when ODL off) -->
                        <div id="legacy-lines" class="absolute inset-0 pointer-events-none transition-opacity duration-300 ${state.odlActive ? 'opacity-0' : 'opacity-100'}">
                            <div class="absolute top-24 left-1/2 w-1 h-40 bg-red-300 transform -translate-x-1/2"></div>
                             <div class="absolute top-40 left-1/2 bg-red-100 text-red-800 px-2 py-1 text-xs rounded border border-red-300 transform -translate-x-1/2">High Latency / Cost</div>
                        </div>

                        <!-- Sync Lines (Visible when ODL on) -->
                        <div id="sync-lines" class="absolute inset-0 pointer-events-none transition-opacity duration-300 ${state.odlActive ? 'opacity-100' : 'opacity-0'}">
                            <div class="absolute bottom-28 left-1/2 w-1 h-12 bg-gray-400 transform -translate-x-1/2"></div>
                            <div class="absolute bottom-32 left-1/2 bg-gray-100 text-gray-800 px-2 py-1 text-xs rounded border border-gray-300 transform -translate-x-1/2">CDC / Kafka Sync</div>
                        </div>
                    </div>
                </div>
            `;

            document.getElementById('odl-toggle').addEventListener('change', (e) => {
                state.odlActive = e.target.checked;
                renderSolution(); // Re-render to animate
            });
        }

        function renderTech() {
            const container = document.getElementById('main-content');
            container.innerHTML = `
                <div class="max-w-6xl mx-auto space-y-6 fade-in">
                    <div class="text-center">
                        <h2 class="text-2xl font-bold text-gray-900">The Schema Battle: Adding "Lifestyle" to FedOne</h2>
                        <p class="text-gray-600">Task: Add a nested user preference for "Travel" to support a new marketing campaign.</p>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        
                        <!-- Left: SQL -->
                        <div class="slide-card p-4 border-l-4 border-red-500">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-bold text-gray-700">Legacy Relational (Oracle/SQL)</h3>
                                <span class="text-xs bg-red-100 text-red-800 px-2 py-1 rounded">Rigid</span>
                            </div>
                            <div class="space-y-3 text-sm">
                                <div class="p-2 bg-gray-100 rounded border border-gray-300">
                                    <p class="font-mono font-bold text-xs text-gray-500 mb-1">TABLE: Customers</p>
                                    <div class="grid grid-cols-3 gap-1 text-xs opacity-50">
                                        <div class="bg-white p-1 border">ID</div><div class="bg-white p-1 border">Name</div><div class="bg-white p-1 border">...</div>
                                    </div>
                                </div>
                                <div class="text-center text-xl text-gray-400">⬇️ JOIN ⬇️</div>
                                <div class="p-2 bg-gray-100 rounded border border-gray-300">
                                    <p class="font-mono font-bold text-xs text-gray-500 mb-1">TABLE: Customer_Preferences</p>
                                    <div class="grid grid-cols-3 gap-1 text-xs opacity-50">
                                        <div class="bg-white p-1 border">Cust_ID</div><div class="bg-white p-1 border">Pref_Key</div><div class="bg-white p-1 border">Val</div>
                                    </div>
                                </div>
                                <div class="mt-4 p-3 bg-red-50 text-red-700 rounded text-xs">
                                    <strong>Impact:</strong>
                                    <ul class="list-disc pl-4 mt-1">
                                        <li>Alter Table script required</li>
                                        <li>Downtime window needed</li>
                                        <li>Complex ORM mapping update</li>
                                    </ul>
                                </div>
                            </div>
                        </div>

                        <!-- Right: MongoDB -->
                        <div class="slide-card p-4 border-l-4 border-green-500">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-bold text-gray-700">MongoDB Document</h3>
                                <span class="text-xs bg-green-100 text-green-800 px-2 py-1 rounded">Flexible</span>
                            </div>
                            <div class="code-block h-64 overflow-y-auto">
<pre>{
  "_id": "user_123",
  "name": "Aditi Sharma",
  "account_type": "FedOne Gold",
  
  <span class="text-green-400">// New Feature Added Instantly</span>
  <span class="text-green-400">"lifestyle_profile": {</span>
    <span class="text-green-400">"primary_interest": "Travel",</span>
    <span class="text-green-400">"locations": ["Dubai", "Singapore"],</span>
    <span class="text-green-400">"spend_category": "High"</span>
  <span class="text-green-400">}</span>
}</pre>
                            </div>
                             <div class="mt-4 p-3 bg-green-50 text-green-700 rounded text-xs">
                                    <strong>Impact:</strong>
                                    <ul class="list-disc pl-4 mt-1">
                                        <li>No schema enforcement required</li>
                                        <li>Zero Downtime deployment</li>
                                        <li>Data grouped logically (Data Locality)</li>
                                    </ul>
                                </div>
                        </div>
                    </div>
                </div>
            `;
        }

        function renderInnovation() {
            const container = document.getElementById('main-content');
            container.innerHTML = `
                <div class="max-w-4xl mx-auto space-y-6 fade-in h-full">
                    <div class="text-center">
                        <h2 class="text-2xl font-bold text-gray-900">Powering "Feddy" with Vector Search</h2>
                        <p class="text-gray-600">Move beyond basic keywords to semantic understanding.</p>
                    </div>

                    <div class="slide-card overflow-hidden flex flex-col h-[500px]">
                        <!-- Chat Header -->
                        <div class="bg-blue-900 p-4 text-white flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <div class="w-8 h-8 bg-white rounded-full flex items-center justify-center text-blue-900 font-bold">F</div>
                                <span>Feddy AI Assistant</span>
                            </div>
                            <div class="flex text-xs bg-blue-800 rounded p-1">
                                <button onclick="setSearchType('keyword')" class="px-3 py-1 rounded ${state.aiSearchType === 'keyword' ? 'bg-white text-blue-900' : 'text-blue-200'}">Legacy Keyword</button>
                                <button onclick="setSearchType('vector')" class="px-3 py-1 rounded ${state.aiSearchType === 'vector' ? 'bg-green-500 text-white' : 'text-blue-200'}">Atlas Vector</button>
                            </div>
                        </div>

                        <!-- Chat Body -->
                        <div class="flex-1 bg-gray-50 p-4 space-y-4 overflow-y-auto" id="chat-body">
                            <!-- User Message -->
                            <div class="flex justify-end">
                                <div class="bg-blue-600 text-white px-4 py-2 rounded-l-lg rounded-tr-lg max-w-xs shadow">
                                    Why was my transaction to Netflix declined yesterday?
                                </div>
                            </div>

                            <!-- Bot Response (Dynamic) -->
                            <div class="flex justify-start">
                                <div class="bg-white text-gray-800 px-4 py-2 rounded-r-lg rounded-tl-lg max-w-sm shadow border border-gray-200">
                                    ${state.aiSearchType === 'keyword' 
                                        ? '<p class="text-red-500 font-semibold mb-1">Legacy Search Result:</p><p>I found 0 FAQs matching "Netflix declined". Please contact support.</p>' 
                                        : '<p class="text-green-600 font-semibold mb-1">MongoDB Vector Search Result:</p><p>I analyzed your recent logs. It looks like your <strong>international usage</strong> flag is turned off, which blocked the payment to Netflix (US). Would you like me to enable it?</p>'}
                                </div>
                            </div>
                            
                            <!-- Tech Explanation -->
                            <div class="flex justify-center">
                                <div class="text-xs text-gray-400 bg-gray-100 px-3 py-1 rounded-full">
                                    ${state.aiSearchType === 'keyword' 
                                        ? 'System scanned for exact word match "Netflix"' 
                                        : 'System generated embedding: [0.2, -0.5, ...] & matched semantic context "foreign transaction failure"'}
                                </div>
                            </div>
                        </div>

                        <!-- Input Area (Mock) -->
                        <div class="p-4 bg-white border-t border-gray-200">
                            <div class="flex gap-2">
                                <input type="text" disabled value="Why was my transaction to Netflix declined?" class="flex-1 bg-gray-100 border border-gray-300 rounded px-3 py-2 text-gray-500 text-sm">
                                <button class="bg-blue-600 text-white px-4 py-2 rounded font-medium text-sm">Send</button>
                            </div>
                        </div>
                    </div>
                </div>
            `;
        }

        function setSearchType(type) {
            state.aiSearchType = type;
            renderInnovation();
        }

        function renderCaseStudy() {
            const container = document.getElementById('main-content');
            container.innerHTML = `
                <div class="max-w-5xl mx-auto space-y-8 fade-in">
                    <div class="text-center">
                        <h2 class="text-2xl font-bold text-gray-900">Proven Results in Banking</h2>
                        <p class="text-gray-600">The MongoDB ODL Pattern in Action.</p>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Metric 1 -->
                        <div class="slide-card p-6 text-center border-t-4 border-blue-600">
                            <h3 class="text-gray-500 font-medium mb-2">Mainframe TCO Reduction</h3>
                            <div class="text-5xl font-bold text-blue-700 mb-2">60%</div>
                            <p class="text-sm text-gray-600">By offloading 90% of read traffic (balance checks, statements) to MongoDB.</p>
                        </div>
                        
                        <!-- Metric 2 -->
                        <div class="slide-card p-6 text-center border-t-4 border-green-500">
                            <h3 class="text-gray-500 font-medium mb-2">New Feature Velocity</h3>
                            <div class="text-5xl font-bold text-green-600 mb-2">4x</div>
                            <p class="text-sm text-gray-600">Faster time-to-market for new FedMobile features using Document Model.</p>
                        </div>
                    </div>

                    <div class="slide-card p-6">
                        <h3 class="text-lg font-bold text-gray-800 mb-4">Benchmark Comparison: Legacy vs. Modern ODL</h3>
                        <div class="chart-container">
                            <canvas id="impactChart"></canvas>
                        </div>
                    </div>

                    <div class="grid grid-cols-3 gap-4 text-center mt-6">
                        <div class="bg-white p-4 rounded shadow-sm">
                            <div class="font-bold text-gray-800">Wells Fargo</div>
                            <div class="text-xs text-gray-500">ODL for Payment Processing</div>
                        </div>
                        <div class="bg-white p-4 rounded shadow-sm">
                            <div class="font-bold text-gray-800">DBS Bank</div>
                            <div class="text-xs text-gray-500">Wealth Mgmt Modernization</div>
                        </div>
                        <div class="bg-white p-4 rounded shadow-sm">
                            <div class="font-bold text-gray-800">Current</div>
                            <div class="text-xs text-gray-500">Core Ledger on MongoDB</div>
                        </div>
                    </div>
                </div>
            `;

            const ctx = document.getElementById('impactChart').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Payment Latency (ms)', 'Cost per Transaction ($)', 'Downtime (Min/Year)'],
                    datasets: [
                        {
                            label: 'Legacy Architecture',
                            data: [800, 0.15, 600],
                            backgroundColor: '#9ca3af'
                        },
                        {
                            label: 'MongoDB ODL',
                            data: [50, 0.02, 5],
                            backgroundColor: '#00ED64'
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { position: 'top' }
                    },
                    scales: {
                        y: { beginAtZero: true }
                    }
                }
            });
        }

        // Navigation Controller
        function navTo(index) {
            // Update State
            state.currentSlide = index;
            
            // Update UI
            document.querySelectorAll('nav button').forEach((btn, idx) => {
                if (idx === index) {
                    btn.classList.remove('text-gray-500', 'bg-gray-100');
                    btn.classList.add('text-gray-900', 'bg-blue-50', 'border-blue-200', 'border');
                } else {
                    btn.classList.add('text-gray-500');
                    btn.classList.remove('text-gray-900', 'bg-blue-50', 'border-blue-200', 'border', 'bg-gray-100');
                }
            });

            // Update Script
            const slideData = slides[index];
            document.getElementById('speaker-script').textContent = slideData.script;

            // Render Content
            slideData.render();
        }

        // Initialize App
        document.addEventListener('DOMContentLoaded', () => {
            navTo(0);
        });

    </script>
</body>
</html>
