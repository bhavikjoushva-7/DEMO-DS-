# DEMO-DS-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>G. Bhavik Joushva - Interactive Portfolio</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <!-- Chart.js CDN -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    body {
      font-family: 'Inter', sans-serif;
      transition: background 0.5s ease, color 0.3s ease;
    }
    
    /* Dynamic Theme Gradient Background Templates */
    body.theme-ocean {
      background: linear-gradient(135deg, #e0f2fe 0%, #f0f9ff 50%, #f4f4f9 100%);
      color: #1e293b;
    }
    body.theme-emerald {
      background: linear-gradient(135deg, #ecfdf5 0%, #f0fdf4 50%, #e6fffa 100%);
      color: #064e3b;
    }
    body.theme-sunset {
      background: linear-gradient(135deg, #fff1f2 0%, #fdf2f8 50%, #f5f3ff 100%);
      color: #4c1d95;
    }
    body.theme-midnight {
      background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #0f172a 100%);
      color: #f8fafc;
    }

    .glass-card {
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(229, 231, 235, 0.6);
    }
    body.theme-midnight .glass-card {
      background: rgba(30, 41, 59, 0.75);
      border: 1px solid rgba(51, 65, 85, 0.6);
    }
  </style>
</head>
<body class="theme-ocean min-h-screen">

  <!-- Navigation Bar -->
  <nav class="sticky top-0 z-40 bg-white/80 dark:bg-slate-900/80 backdrop-blur-md border-b border-gray-200/50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-blue-600 to-indigo-600 flex items-center justify-center text-white font-black text-lg shadow-md">
            BJ
          </div>
          <span class="font-bold text-xl tracking-tight">G. Bhavik Joushva</span>
        </div>
        
        <div class="hidden md:flex items-center space-x-6 font-medium text-sm">
          <a href="#about" class="hover:text-blue-600 transition">About</a>
          <a href="#education" class="hover:text-blue-600 transition">Education</a>
          <a href="#skills" class="hover:text-blue-600 transition">Skills Analytics</a>
          <a href="#certificates" class="hover:text-blue-600 transition">Certifications</a>
          <a href="#contact" class="hover:text-blue-600 transition">Contact</a>
        </div>

        <div class="flex items-center space-x-4">
          <!-- Background Color Template Selector -->
          <div class="flex items-center bg-gray-200/60 dark:bg-slate-800 p-1 rounded-full gap-1">
            <button onclick="setTheme('theme-ocean')" title="Ocean Blue" class="w-5 h-5 rounded-full bg-sky-400 hover:scale-110 transition-transform"></button>
            <button onclick="setTheme('theme-emerald')" title="Emerald Teal" class="w-5 h-5 rounded-full bg-emerald-400 hover:scale-110 transition-transform"></button>
            <button onclick="setTheme('theme-sunset')" title="Sunset Rose" class="w-5 h-5 rounded-full bg-rose-400 hover:scale-110 transition-transform"></button>
            <button onclick="setTheme('theme-midnight')" title="Midnight Dark" class="w-5 h-5 rounded-full bg-slate-900 hover:scale-110 transition-transform border border-slate-700"></button>
          </div>

          <button onclick="openModal()" class="bg-blue-600 hover:bg-blue-700 text-white text-sm font-semibold px-4 py-2 rounded-lg shadow-sm transition">
            <i class="fa-solid fa-file-pdf mr-2"></i>Resume
          </button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="about" class="py-16 md:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
      
      <!-- Profile Box (No Picture) -->
      <div class="lg:col-span-4 flex flex-col items-center text-center glass-card p-8 rounded-3xl shadow-xl border">
        <!-- Initials Avatar Badge -->
        <div class="w-32 h-32 rounded-3xl bg-gradient-to-tr from-blue-600 via-indigo-500 to-purple-600 flex items-center justify-center text-white font-extrabold text-4xl shadow-lg mb-6 ring-4 ring-blue-500/20">
          GBJ
        </div>
        
        <h1 class="text-2xl font-bold">G. Bhavik Joushva</h1>
        <p class="text-blue-600 font-semibold text-xs tracking-wider uppercase mt-1 mb-4">Undergraduate Data Science Student</p>
        
        <div class="flex flex-wrap gap-2 justify-center mb-6">
          <span class="px-3 py-1 bg-blue-500/10 text-blue-600 text-xs rounded-full font-medium">Data Analytics</span>
          <span class="px-3 py-1 bg-purple-500/10 text-purple-600 text-xs rounded-full font-medium">Generative AI</span>
          <span class="px-3 py-1 bg-emerald-500/10 text-emerald-600 text-xs rounded-full font-medium">Statistics</span>
        </div>

        <div class="w-full space-y-3 text-left text-sm opacity-90 border-t border-gray-200/50 pt-6">
          <div class="flex items-center gap-3">
            <i class="fa-solid fa-envelope text-blue-500 w-5"></i>
            <a href="mailto:bhavikjoushva@gmail.com" class="hover:underline">bhavikjoushva@gmail.com</a>
          </div>
          <div class="flex items-center gap-3">
            <i class="fa-solid fa-phone text-blue-500 w-5"></i>
            <span>+91 9108162034</span>
          </div>
          <div class="flex items-start gap-3">
            <i class="fa-solid fa-location-dot text-blue-500 w-5 mt-1"></i>
            <span>G01, Venus Aura Arvind, 6th Cross Wilson Garden Police Station, Bangalore-560027</span>
          </div>
          <div class="flex items-center gap-3">
            <i class="fa-brands fa-linkedin text-blue-500 w-5"></i>
            <a href="https://linkedin.com/in/G Bhavik Joushva" target="_blank" class="hover:underline">G Bhavik Joushva</a>
          </div>
          <div class="flex items-center gap-3">
            <i class="fa-brands fa-github text-blue-500 w-5"></i>
            <a href="https://github.com/bhavikjoushva-7" target="_blank" class="hover:underline">bhavikjoushva-7</a>
          </div>
        </div>
      </div>

      <!-- Objective & Bio -->
      <div class="lg:col-span-8 space-y-6">
        <div class="inline-flex items-center gap-2 px-3 py-1 bg-blue-500/10 text-blue-600 rounded-full text-xs font-bold uppercase tracking-wider">
          <i class="fa-solid fa-bullseye"></i> Career Objective
        </div>
        <h2 class="text-3xl sm:text-5xl font-extrabold leading-tight">
          Seeking Data Analyst Internship
        </h2>
        <p class="text-lg leading-relaxed opacity-90">
          Analytical and detail-oriented Data Science student having a strong foundation in statistical analysis and quantitative research[cite: 1]. Eager to leverage a problem-solving mindset and a passion for data-driven storytelling to help the future team uncover hidden patterns and translate complex information into clear, strategic recommendations[cite: 1].
        </p>

        <!-- Quick Stats Grid -->
        <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 pt-4">
          <div class="glass-card p-5 rounded-2xl text-center border">
            <p class="text-3xl font-black text-blue-600">3.63</p>
            <p class="text-xs font-semibold uppercase opacity-75 mt-1">Current CGPA (Sem 2)[cite: 1]</p>
          </div>
          <div class="glass-card p-5 rounded-2xl text-center border">
            <p class="text-3xl font-black text-indigo-600">4+</p>
            <p class="text-xs font-semibold uppercase opacity-75 mt-1">Certifications[cite: 1]</p>
          </div>
          <div class="glass-card p-5 rounded-2xl text-center border col-span-2 sm:col-span-1">
            <p class="text-3xl font-black text-emerald-600">5</p>
            <p class="text-xs font-semibold uppercase opacity-75 mt-1">Languages Spoken[cite: 1]</p>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- Interactive Skills Matrix -->
  <section id="skills" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-12">
      <h2 class="text-3xl font-bold">Skills & Analytical Matrix</h2>
      <p class="opacity-80 mt-2">Quantitative tools, programming stacks, and soft skills.</p>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
      <!-- Interactive Tabs -->
      <div class="lg:col-span-7 space-y-6">
        <div class="flex space-x-2 border-b border-gray-200/50 pb-2">
          <button onclick="switchTab('analytics')" id="tab-analytics" class="skill-tab active px-4 py-2 text-sm font-semibold rounded-xl bg-blue-600 text-white shadow-sm">Data Analytics</button>
          <button onclick="switchTab('programming')" id="tab-programming" class="skill-tab px-4 py-2 text-sm font-semibold rounded-xl hover:bg-white/50 transition">Programming</button>
          <button onclick="switchTab('professional')" id="tab-professional" class="skill-tab px-4 py-2 text-sm font-semibold rounded-xl hover:bg-white/50 transition">Professional Skills</button>
        </div>

        <div id="pane-analytics" class="tab-pane space-y-4">
          <div>
            <div class="flex justify-between text-sm font-medium mb-1">
              <span>Excel (Advanced Analytics & Modeling)[cite: 1]</span>
              <span>90%</span>
            </div>
            <div class="w-full bg-gray-200/60 h-2.5 rounded-full overflow-hidden">
              <div class="bg-blue-600 h-2.5 rounded-full" style="width: 90%"></div>
            </div>
          </div>
          <div>
            <div class="flex justify-between text-sm font-medium mb-1">
              <span>SQL (Database Querying & Structuring)[cite: 1]</span>
              <span>85%</span>
            </div>
            <div class="w-full bg-gray-200/60 h-2.5 rounded-full overflow-hidden">
              <div class="bg-blue-600 h-2.5 rounded-full" style="width: 85%"></div>
            </div>
          </div>
          <div>
            <div class="flex justify-between text-sm font-medium mb-1">
              <span>Power BI (Dashboards & Visualization)[cite: 1]</span>
              <span>80%</span>
            </div>
            <div class="w-full bg-gray-200/60 h-2.5 rounded-full overflow-hidden">
              <div class="bg-blue-600 h-2.5 rounded-full" style="width: 80%"></div>
            </div>
          </div>
        </div>

        <div id="pane-programming" class="tab-pane hidden space-y-4">
          <div>
            <div class="flex justify-between text-sm font-medium mb-1">
              <span>Python (Pandas, Data Manipulation)[cite: 1]</span>
              <span>85%</span>
            </div>
            <div class="w-full bg-gray-200/60 h-2.5 rounded-full overflow-hidden">
              <div class="bg-purple-600 h-2.5 rounded-full" style="width: 85%"></div>
            </div>
          </div>
          <div>
            <div class="flex justify-between text-sm font-medium mb-1">
              <span>R-Studio (Statistical Analysis)[cite: 1]</span>
              <span>80%</span>
            </div>
            <div class="w-full bg-gray-200/60 h-2.5 rounded-full overflow-hidden">
              <div class="bg-purple-600 h-2.5 rounded-full" style="width: 80%"></div>
            </div>
          </div>
        </div>

        <div id="pane-professional" class="tab-pane hidden">
          <div class="grid grid-cols-2 gap-3">
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-file-signature text-blue-500"></i>
              <span class="text-sm font-medium">Report Writing[cite: 1]</span>
            </div>
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-users text-blue-500"></i>
              <span class="text-sm font-medium">Public Relations[cite: 1]</span>
            </div>
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-people-group text-blue-500"></i>
              <span class="text-sm font-medium">Teamwork[cite: 1]</span>
            </div>
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-clock text-blue-500"></i>
              <span class="text-sm font-medium">Time Management[cite: 1]</span>
            </div>
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-comments text-blue-500"></i>
              <span class="text-sm font-medium">Effective Communication[cite: 1]</span>
            </div>
            <div class="p-3 glass-card rounded-xl border flex items-center gap-3">
              <i class="fa-solid fa-brain text-blue-500"></i>
              <span class="text-sm font-medium">Critical Thinking[cite: 1]</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Skill Chart -->
      <div class="lg:col-span-5 glass-card p-6 rounded-3xl border shadow-sm">
        <h3 class="text-xs font-bold uppercase tracking-wider opacity-60 mb-4 text-center">Skill Proficiency Radar</h3>
        <div class="w-full h-64">
          <canvas id="skillsChart"></canvas>
        </div>
      </div>
    </div>
  </section>

  <!-- Education Timeline -->
  <section id="education" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-12">
      <h2 class="text-3xl font-bold">Education Timeline</h2>
    </div>

    <div class="relative border-l-2 border-blue-500/40 ml-4 md:ml-32 space-y-8">
      
      <div class="relative pl-6 md:pl-8">
        <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-blue-600 ring-4 ring-white"></div>
        <div class="glass-card p-6 rounded-2xl border shadow-sm">
          <span class="text-xs font-bold text-blue-600 uppercase tracking-wider">Present</span>
          <h3 class="text-xl font-bold mt-1">Christ Central Campus</h3>
          <p class="text-sm font-medium opacity-80">B.Sc Data Science and Statistics[cite: 1]</p>
          <div class="mt-4 flex flex-wrap gap-4 text-sm">
            <div class="bg-blue-500/10 px-3 py-1.5 rounded-lg border border-blue-500/20">
              <span class="opacity-70">1st Sem CGPA:</span> <strong class="text-blue-600">3.6 / 4[cite: 1]</strong>
            </div>
            <div class="bg-blue-500/10 px-3 py-1.5 rounded-lg border border-blue-500/20">
              <span class="opacity-70">2nd Sem CGPA:</span> <strong class="text-blue-600">3.63 / 4[cite: 1]</strong>
            </div>
          </div>
        </div>
      </div>

      <div class="relative pl-6 md:pl-8">
        <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-blue-600 ring-4 ring-white"></div>
        <div class="glass-card p-6 rounded-2xl border shadow-sm">
          <span class="text-xs font-bold opacity-60 uppercase tracking-wider">2024 - 2025[cite: 1]</span>
          <h3 class="text-xl font-bold mt-1">Christ Junior College[cite: 1]</h3>
          <p class="text-sm font-medium opacity-80">12th Grade (Physics, Chemistry, Maths, Biology)[cite: 1]</p>
          <p class="mt-2 text-sm">Score Achieved: <strong class="text-blue-600">88%[cite: 1]</strong></p>
        </div>
      </div>

      <div class="relative pl-6 md:pl-8">
        <div class="absolute -left-[9px] top-1.5 w-4 h-4 rounded-full bg-blue-600 ring-4 ring-white"></div>
        <div class="glass-card p-6 rounded-2xl border shadow-sm">
          <span class="text-xs font-bold opacity-60 uppercase tracking-wider">2022 - 2023[cite: 1]</span>
          <h3 class="text-xl font-bold mt-1">Christ School (ICSE)[cite: 1]</h3>
          <p class="text-sm font-medium opacity-80">10th Grade Secondary Education[cite: 1]</p>
          <p class="mt-2 text-sm">Score Achieved: <strong class="text-blue-600">91%[cite: 1]</strong></p>
        </div>
      </div>

    </div>
  </section>

  <!-- Certifications & Languages -->
  <section id="certificates" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
      
      <div>
        <h2 class="text-2xl font-bold mb-6 flex items-center gap-2">
          <i class="fa-solid fa-certificate text-blue-500"></i> Certifications
        </h2>
        <div class="space-y-3">
          <div class="glass-card p-4 rounded-xl border flex items-center justify-between">
            <span class="font-medium">Business Analytics with Excel[cite: 1]</span>
            <span class="px-2.5 py-1 bg-green-500/10 text-green-600 text-xs rounded-full font-semibold">Verified</span>
          </div>
          <div class="glass-card p-4 rounded-xl border flex items-center justify-between">
            <span class="font-medium">Introduction to Generative AI[cite: 1]</span>
            <span class="px-2.5 py-1 bg-green-500/10 text-green-600 text-xs rounded-full font-semibold">Verified</span>
          </div>
          <div class="glass-card p-4 rounded-xl border flex items-center justify-between">
            <span class="font-medium">Introduction to Artificial Intelligence[cite: 1]</span>
            <span class="px-2.5 py-1 bg-green-500/10 text-green-600 text-xs rounded-full font-semibold">Verified</span>
          </div>
          <div class="glass-card p-4 rounded-xl border flex items-center justify-between">
            <span class="font-medium">Data Analytics with Generative AI[cite: 1]</span>
            <span class="px-2.5 py-1 bg-green-500/10 text-green-600 text-xs rounded-full font-semibold">Verified</span>
          </div>
        </div>
      </div>

      <div class="space-y-8">
        <div>
          <h2 class="text-2xl font-bold mb-6 flex items-center gap-2">
            <i class="fa-solid fa-language text-blue-500"></i> Languages
          </h2>
          <div class="flex flex-wrap gap-2">
            <span class="px-4 py-2 glass-card rounded-xl text-sm font-medium">English <span class="text-xs opacity-60">(Fluent)[cite: 1]</span></span>
            <span class="px-4 py-2 glass-card rounded-xl text-sm font-medium">Kannada <span class="text-xs opacity-60">(Fluent)[cite: 1]</span></span>
            <span class="px-4 py-2 glass-card rounded-xl text-sm font-medium">Hindi <span class="text-xs opacity-60">(Fluent)[cite: 1]</span></span>
            <span class="px-4 py-2 glass-card rounded-xl text-sm font-medium">Telugu <span class="text-xs opacity-60">(Fluent)[cite: 1]</span></span>
            <span class="px-4 py-2 glass-card rounded-xl text-sm font-medium">Tamil <span class="text-xs opacity-60">(Fluent)[cite: 1]</span></span>
          </div>
        </div>

        <div>
          <h2 class="text-2xl font-bold mb-4 flex items-center gap-2">
            <i class="fa-solid fa-icons text-blue-500"></i> Hobbies & Interests
          </h2>
          <div class="grid grid-cols-2 gap-3 text-sm">
            <div class="flex items-center gap-2 opacity-90">
              <i class="fa-solid fa-palette text-blue-500"></i> Poster Making[cite: 1]
            </div>
            <div class="flex items-center gap-2 opacity-90">
              <i class="fa-solid fa-film text-blue-500"></i> Movie Analysis[cite: 1]
            </div>
            <div class="flex items-center gap-2 opacity-90">
              <i class="fa-solid fa-robot text-blue-500"></i> AI Tools Research[cite: 1]
            </div>
            <div class="flex items-center gap-2 opacity-90">
              <i class="fa-solid fa-book text-blue-500"></i> Reading Books[cite: 1]
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- Resume Modal -->
  <div id="resumeModal" class="fixed inset-0 z-50 bg-black/60 backdrop-blur-sm hidden flex items-center justify-center p-4">
    <div class="bg-white text-gray-900 w-full max-w-3xl max-h-[90vh] rounded-2xl shadow-2xl flex flex-col overflow-hidden">
      <div class="p-4 border-b flex justify-between items-center bg-gray-50">
        <h3 class="font-bold flex items-center gap-2">
          <i class="fa-solid fa-file-pdf text-blue-500"></i> Resume View
        </h3>
        <div class="flex items-center gap-2">
          <button onclick="window.print()" class="px-3 py-1.5 text-xs font-semibold bg-gray-200 rounded-md hover:bg-gray-300">Print</button>
          <button onclick="closeModal()" class="text-gray-400 hover:text-gray-600 p-1">
            <i class="fa-solid fa-xmark text-xl"></i>
          </button>
        </div>
      </div>

      <div class="p-8 overflow-y-auto space-y-4 text-xs">
        <div class="border-b pb-4">
          <h1 class="text-2xl font-bold uppercase tracking-wide">G. Bhavik Joushva[cite: 1]</h1>
          <p class="text-blue-600 font-semibold uppercase mt-1">Undergraduate Student[cite: 1]</p>
          <p class="mt-2 text-gray-600">
            +91 9108162034[cite: 1] | bhavikjoushva@gmail.com[cite: 1] | G01, Venus Aura Arvind, 6th Cross Wilson Garden Police Station, Bangalore-560027[cite: 1]
          </p>
        </div>

        <div>
          <h4 class="font-bold border-b pb-1 mb-2 uppercase text-blue-600">Objective</h4>
          <p class="text-gray-700 leading-relaxed">
            Analytical and detail-oriented Data Science student having a strong foundation in statistical analysis and quantitative research seeking a Data Analyst internship[cite: 1]. Eager to leverage a problem-solving mindset and a passion for data-driven storytelling to help the future team uncover hidden patterns and translate complex information into clear, strategic recommendations[cite: 1].
          </p>
        </div>

        <div>
          <h4 class="font-bold border-b pb-1 mb-2 uppercase text-blue-600">Education</h4>
          <div class="space-y-1">
            <p><strong>Christ Central Campus</strong> - B.Sc Data Science and Statistics (Sem 1: 3.6/4 | Sem 2: 3.63/4)[cite: 1]</p>
            <p><strong>Christ Junior College</strong> - 12th Grade (88%)[cite: 1]</p>
            <p><strong>Christ School (ICSE)</strong> - 10th Grade (91%)[cite: 1]</p>
          </div>
        </div>

        <div>
          <h4 class="font-bold border-b pb-1 mb-2 uppercase text-blue-600">Key Skills</h4>
          <p>Excel, SQL, Power BI, Python, R-Studio, Report writing, Public Relations, Teamwork, Time Management, Effective Communication, Critical Thinking[cite: 1]</p>
        </div>
      </div>
    </div>
  </div>

  <script>
    // Theme Switcher Functionality
    function setTheme(themeName) {
      document.body.className = `${themeName} min-h-screen`;
    }

    // Skills Tab Switcher
    function switchTab(tabName) {
      document.querySelectorAll('.tab-pane').forEach(el => el.classList.add('hidden'));
      document.querySelectorAll('.skill-tab').forEach(el => {
        el.classList.remove('bg-blue-600', 'text-white', 'shadow-sm');
      });

      document.getElementById(`pane-${tabName}`).classList.remove('hidden');
      const activeTab = document.getElementById(`tab-${tabName}`);
      activeTab.classList.add('bg-blue-600', 'text-white', 'shadow-sm');
    }

    // Modal Control
    function openModal() {
      document.getElementById('resumeModal').classList.remove('hidden');
    }
    function closeModal() {
      document.getElementById('resumeModal').classList.add('hidden');
    }

    // Radar Chart Setup
    const ctx = document.getElementById('skillsChart').getContext('2d');
    new Chart(ctx, {
      type: 'radar',
      data: {
        labels: ['Excel & SQL', 'Power BI', 'Python', 'R-Studio', 'Statistics', 'AI Tools'],
        datasets: [{
          label: 'Proficiency',
          data: [90, 80, 85, 80, 88, 85],
          backgroundColor: 'rgba(59, 130, 246, 0.25)',
          borderColor: 'rgba(59, 130, 246, 1)',
          borderWidth: 2,
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          r: {
            angleLines: { color: 'rgba(156, 163, 175, 0.2)' },
            grid: { color: 'rgba(156, 163, 175, 0.2)' },
            ticks: { display: false }
          }
        },
        plugins: { legend: { display: false } }
      }
    });
  </script>

</body>
</html>
