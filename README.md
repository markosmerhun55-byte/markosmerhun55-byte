<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <base target="_self">
  <title>Developer Portfolio</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/@preline/preline@2.0.0/dist/preline.min.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            primary: {
              50: '#f0f9ff',
              100: '#e0f2fe',
              200: '#bae6fd',
              300: '#7dd3fc',
              400: '#38bdf8',
              500: '#0ea5e9',
              600: '#0284c7',
              700: '#0369a1',
              800: '#075985',
              900: '#0c4a6e',
            }
          },
          animation: {
            'float': 'float 3s ease-in-out infinite',
          },
          keyframes: {
            float: {
              '0%, 100%': { transform: 'translateY(0)' },
              '50%': { transform: 'translateY(-10px)' },
            }
          }
        }
      }
    }
  </script>
  <style>
    .gradient-text {
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      background-image: linear-gradient(90deg, #3b82f6, #8b5cf6);
    }
    .project-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
    }
  </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-100 transition-colors duration-300">
  <div class="min-h-screen flex flex-col">
    <!-- Navigation -->
    <nav class="sticky top-0 z-50 bg-white/80 dark:bg-gray-900/80 backdrop-blur-sm border-b border-gray-200 dark:border-gray-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex items-center">
            <a href="#home" class="text-xl font-bold gradient-text">Haro-Dev</a>
          </div>
          <div class="hidden md:flex items-center space-x-8">
            <a href="#home" class="hover:text-primary-500 transition-colors">Home</a>
            <a href="#about" class="hover:text-primary-500 transition-colors">About</a>
            <a href="#projects" class="hover:text-primary-500 transition-colors">Projects</a>
            <a href="#skills" class="hover:text-primary-500 transition-colors">Skills</a>
            <a href="#contact" class="hover:text-primary-500 transition-colors">Contact</a>
            <button id="theme-toggle" class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-700">
              <i class="fas fa-sun dark:hidden"></i>
              <i class="fas fa-moon hidden dark:block"></i>
            </button>
          </div>
          <div class="md:hidden flex items-center">
            <button id="mobile-menu-button" class="p-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-700">
              <i class="fas fa-bars"></i>
            </button>
          </div>
        </div>
      </div>
      
      <!-- Mobile menu -->
      <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-gray-900 border-t border-gray-200 dark:border-gray-800">
        <div class="px-2 pt-2 pb-3 space-y-1">
          <a href="#home" class="block px-3 py-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800">Home</a>
          <a href="#about" class="block px-3 py-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800">About</a>
          <a href="#projects" class="block px-3 py-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800">Projects</a>
          <a href="#skills" class="block px-3 py-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800">Skills</a>
          <a href="#contact" class="block px-3 py-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800">Contact</a>
          <div class="px-3 py-2">
            <button id="mobile-theme-toggle" class="flex items-center space-x-2">
              <span>Toggle Theme</span>
              <i class="fas fa-sun dark:hidden"></i>
              <i class="fas fa-moon hidden dark:block"></i>
            </button>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <div class="flex flex-col md:flex-row items-center justify-between gap-12">
          <div class="md:w-1/2">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
              Hi, I'm <span class="gradient-text">Developer</span>
            </h1>
            <p class="text-lg md:text-xl text-gray-600 dark:text-gray-300 mb-8">
              Full Stack Developer specializing in modern web technologies. I build responsive, accessible, and performant web applications.
            </p>
            <div class="flex flex-wrap gap-4">
              <a href="#contact" class="px-6 py-3 bg-primary-500 text-white rounded-lg hover:bg-primary-600 transition-colors">
                Contact Me
              </a>
              <a href="#projects" class="px-6 py-3 border border-gray-300 dark:border-gray-600 rounded-lg hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors">
                View Projects
              </a>
            </div>
          </div>
          <div class="md:w-1/2 flex justify-center">
            <div class="relative w-64 h-64 sm:w-80 sm:h-80">
              <div class="absolute inset-0 bg-gradient-to-br from-primary-400 to-purple-500 rounded-full opacity-20 blur-xl"></div>
              <div class="relative w-full h-full flex items-center justify-center">
                <img src="https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                     alt="Developer" 
                     class="w-full h-full object-cover rounded-full border-4 border-white dark:border-gray-800 shadow-lg">
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-12">About Me</h2>
        <div class="flex flex-col md:flex-row gap-12">
          <div class="md:w-1/2">
            <h3 class="text-2xl font-semibold mb-4">Who I Am</h3>
            <p class="text-gray-600 dark:text-gray-300 mb-6">
              I'm a passionate developer with 2+ years of experience building web applications. I specialize in JavaScript frameworks and have a strong background in both frontend and backend development.
            </p>
            <p class="text-gray-600 dark:text-gray-300 mb-6">
              My approach combines technical expertise with creative problem-solving to deliver high-quality solutions that meet user needs and business objectives.
            </p>
            <div class="flex flex-wrap gap-4">
              <div class="flex items-center">
                <i class="fas fa-map-marker-alt text-primary-500 mr-2"></i>
                <span>Addis Ababa</span>
              </div>
              <div class="flex items-center">
                <i class="fas fa-envelope text-primary-500 mr-2"></i>
                <span>markosmerhun55@gmail.com</span>
              </div>
            </div>
          </div>
          <div class="md:w-1/2">
            <h3 class="text-2xl font-semibold mb-4">My Experience</h3>
            <div class="space-y-6">
              <div class="border-l-4 border-primary-500 pl-4">
                <h4 class="font-semibold">Senior Frontend Developer</h4>
                <p class="text-gray-500 dark:text-gray-400 text-sm">TechCorp • 2020 - Present</p>
                <p class="text-gray-600 dark:text-gray-300 mt-2">
                  Lead the frontend development team, implementing modern React applications with TypeScript and Next.js.
                </p>
              </div>
              <div class="border-l-4 border-primary-500 pl-4">
                <h4 class="font-semibold">Full Stack Developer</h4>
                <p class="text-gray-500 dark:text-gray-400 text-sm">WebSolutions • 2018 - 2020</p>
                <p class="text-gray-600 dark:text-gray-300 mt-2">
                  Developed full-stack applications using Node.js, Express, and MongoDB with React frontends.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-12">My Skills</h2>
        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6">
          <div class="skill-card p-6 bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 flex flex-col items-center hover:shadow-md transition-all">
            <div class="w-16 h-16 mb-4 flex items-center justify-center bg-primary-50 dark:bg-gray-700 rounded-full">
              <i class="fab fa-js text-3xl text-yellow-400"></i>
            </div>
            <h3 class="font-semibold">JavaScript</h3>
            <div class="w-full bg-gray-200 dark:bg-gray-700 h-2 mt-3 rounded-full">
              <div class="bg-primary-500 h-2 rounded-full" style="width: 90%"></div>
            </div>
          </div>
          
          <div class="skill-card p-6 bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 flex flex-col items-center hover:shadow-md transition-all">
            <div class="w-16 h-16 mb-4 flex items-center justify-center bg-primary-50 dark:bg-gray-700 rounded-full">
              <i class="fab fa-react text-3xl text-blue-400"></i>
            </div>
            <h3 class="font-semibold">React</h3>
            <div class="w-full bg-gray-200 dark:bg-gray-700 h-2 mt-3 rounded-full">
              <div class="bg-primary-500 h-2 rounded-full" style="width: 85%"></div>
            </div>
          </div>
          
          <div class="skill-card p-6 bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 flex flex-col items-center hover:shadow-md transition-all">
            <div class="w-16 h-16 mb-4 flex items-center justify-center bg-primary-50 dark:bg-gray-700 rounded-full">
              <i class="fab fa-node-js text-3xl text-green-500"></i>
            </div>
            <h3 class="font-semibold">Node.js</h3>
            <div class="w-full bg-gray-200 dark:bg-gray-700 h-2 mt-3 rounded-full">
              <div class="bg-primary-500 h-2 rounded-full" style="width: 80%"></div>
            </div>
          </div>
          
          <div class="skill-card p-6 bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 flex flex-col items-center hover:shadow-md transition-all">
            <div class="w-16 h-16 mb-4 flex items-center justify-center bg-primary-50 dark:bg-gray-700 rounded-full">
              <i class="fas fa-database text-3xl text-blue-500"></i>
            </div>
            <h3 class="font-semibold">MongoDB/MYSQL</h3>
            <div class="w-full bg-gray-200 dark:bg-gray-700 h-2 mt-3 rounded-full">
              <div class="bg-primary-500 h-2 rounded-full" style="width: 75%"></div>
            </div>
          </div>
          
          <div class="skill-card p-6 bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 flex flex-col items-center hover:shadow-md transition-all">
            <div class="w-16 h-16 mb-4 flex items-center justify-center bg-primary-50 dark:bg-gray-700 rounded-full">
              <i class="fab fa-css3-alt text-3xl text-blue-300"></i>
            </div>
            <h3 class="font-semibold">CSS/Tailwind</h3>
            <div class="w-full bg-gray-200 dark:bg-gray-700 h-2 mt-3 rounded-full">
              <div class="bg-primary-500 h-2 rounded-full" style="width: 95%"></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50 dark:bg-gray-800">
      <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-12">Featured Projects</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Project 1 -->
          <div class="project-card bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 overflow-hidden transition-all duration-300">
            <div class="h-48 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                   alt="Email Spam Checker" 
                   class="w-full h-full object-cover transition-transform duration-500 hover:scale-105">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">E-commerce Platform</h3>
              <p class="text-gray-600 dark:text-gray-300 mb-4">
               An Email Spam Checker identifies whether an email is spam or legitimate using machine learning.
              </p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">React</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Node.js</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">MongoDB</span>
              </div>
              <div class="flex space-x-3">
                <a href="#" class="text-primary-500 hover:text-primary-600 transition-colors">
                  <i class="fas fa-external-link-alt"></i> Live Demo
                </a>
                <a href="#" class="text-gray-500 hover:text-gray-600 dark:hover:text-gray-300 transition-colors">
                  <i class="fab fa-github"></i> Code
                </a>
              </div>
            </div>
          </div>
          
          <!-- Project 2 -->
          <div class="project-card bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 overflow-hidden transition-all duration-300">
            <div class="h-48 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1555421689-3f034debb7a6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                   alt="House price Predection App" 
                   class="w-full h-full object-cover transition-transform duration-500 hover:scale-105">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">House price Predection App</h3>
              <p class="text-gray-600 dark:text-gray-300 mb-4">
               A House Price Prediction App estimates the market price of a house based on its features using machine learning.
              </p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Vue.js</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Firebase</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Tailwind</span>
              </div>
              <div class="flex space-x-3">
                <a href="#" class="text-primary-500 hover:text-primary-600 transition-colors">
                  <i class="fas fa-external-link-alt"></i> Live Demo
                </a>
                <a href="#" class="text-gray-500 hover:text-gray-600 dark:hover:text-gray-300 transition-colors">
                  <i class="fab fa-github"></i> Code
                </a>
              </div>
            </div>
          </div>
          
          <!-- Project 3 -->
          <div class="project-card bg-white dark:bg-gray-800 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700 overflow-hidden transition-all duration-300">
            <div class="h-48 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1522542550221-31fd19575a2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                   alt="Social Media Dashboard" 
                   class="w-full h-full object-cover transition-transform duration-500 hover:scale-105">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-2">Social Media Dashboard</h3>
              <p class="text-gray-600 dark:text-gray-300 mb-4">
                Analytics dashboard for tracking social media metrics with real-time data visualization.
              </p>
              <div class="flex flex-wrap gap-2 mb-4">
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Next.js</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">TypeScript</span>
                <span class="px-2 py-1 bg-primary-100 dark:bg-gray-700 text-primary-800 dark:text-primary-300 text-xs rounded">Chart.js</span>
              </div>
              <div class="flex space-x-3">
                <a href="#" class="text-primary-500 hover:text-primary-600 transition-colors">
                  <i class="fas fa-external-link-alt"></i> Live Demo
                </a>
                <a href="#" class="text-gray-500 hover:text-gray-600 dark:hover:text-gray-300 transition-colors">
                  <i class="fab fa-github"></i> Code
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-4 sm:px-6 lg:px-8">
      <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-bold text-center mb-12">Get In Touch</h2>
        <div class="flex flex-col md:flex-row gap-12">
          <div class="md:w-1/2">
            <h3 class="text-2xl font-semibold mb-6">Contact Information</h3>
            <div class="space-y-6">
              <div class="flex items-start">
                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-primary-100 dark:bg-gray-700 flex items-center justify-center mr-4">
                  <i class="fas fa-envelope text-primary-500"></i>
                </div>
                <div>
                  <h4 class="font-medium">Email</h4>
                  <p class="text-gray-600 dark:text-gray-300">haroutura4@gmail.com</p>
                </div>
              </div>
              <div class="flex items-start">
                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-primary-100 dark:bg-gray-700 flex items-center justify-center mr-4">
                  <i class="fas fa-phone-alt text-primary-500"></i>
                </div>
                <div>
                  <h4 class="font-medium">Phone</h4>
                  <p class="text-gray-600 dark:text-gray-300">+251912485544</p>
                </div>
              </div>
              <div class="flex items-start">
                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-primary-100 dark:bg-gray-700 flex items-center justify-center mr-4">
                  <i class="fas fa-map-marker-alt text-primary-500"></i>
                </div>
                <div>
                  <h4 class="font-medium">Location</h4>
                  <p class="text-gray-600 dark:text-gray-300">Addis Ababa</p>
                </div>
              </div>
            </div>
            <div class="mt-8">
              <h4 class="font-medium mb-4">Follow Me</h4>
              <div class="flex space-x-4">
                <a href="https://github.com/markosmerhun55-byte" class="h-10 w-10 rounded-full bg-gray-100 dark:bg-gray-700 flex items-center justify-center hover:bg-primary-500 hover:text-white transition-colors">
                  <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/in/merhun-markos-mache-a63a44415?utm_source=share_via&utm_content=profile&utm_medium=member_ios" class="h-10 w-10 rounded-full bg-gray-100 dark:bg-gray-700 flex items-center justify-center hover:bg-blue-500 hover:text-white transition-colors">
                  <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="#" class="h-10 w-10 rounded-full bg-gray-100 dark:bg-gray-700 flex items-center justify-center hover:bg-blue-400 hover:text-white transition-colors">
                  <i class="fab fa-twitter"></i>
                </a>
                <a href="https://www.instagram.com/merhunmark?igsh=MW40cm1lNHZ2N2dlcQ%3D%3D&utm_source=qr" class="h-10 w-10 rounded-full bg-gray-100 dark:bg-gray-700 flex items-center justify-center hover:bg-pink-500 hover:text-white transition-colors">
                  <i class="fab fa-instagram"></i>
                </a>
              </div>
            </div>
          </div>
          <div class="md:w-1/2">
            <form id="contact-form" class="space-y-6">
              <div>
                <label for="name" class="block text-sm font-medium mb-1">Name</label>
                <input type="text" id="name" name="name" required 
                       class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-800">
              </div>
              <div>
                <label for="email" class="block text-sm font-medium mb-1">Email</label>
                <input type="email" id="email" name="email" required 
                       class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-800">
              </div>
              <div>
                <label for="subject" class="block text-sm font-medium mb-1">Subject</label>
                <input type="text" id="subject" name="subject" 
                       class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-800">
              </div>
              <div>
                <label for="message" class="block text-sm font-medium mb-1">Message</label>
                <textarea id="message" name="message" rows="4" required 
                          class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 dark:bg-gray-800"></textarea>
              </div>
              <button type="submit" class="px-6 py-3 bg-primary-500 text-white rounded-lg hover:bg-primary-600 transition-colors w-full">
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-100 dark:bg-gray-800 py-8 px-4 sm:px-6 lg:px-8 border-t border-gray-200 dark:border-gray-700">
      <div class="max-w-7xl mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="mb-4 md:mb-0">
            <a href="#home" class="text-xl font-bold gradient-text">Haro-Dev</a>
            <p class="text-gray-500 dark:text-gray-400 text-sm mt-2">
              © 2025 Developer Portfolio. All rights reserved.
            </p>
          </div>
          <div class="flex space-x-6">
            <a href="https://github.com/markosmerhun55-byte" class="text-gray-500 hover:text-gray-700 dark:hover:text-gray-300 transition-colors">
              <i class="fab fa-github"></i>
            </a>
            <a href="https://www.linkedin.com/in/merhun-markos-mache-a63a44415?utm_source=share_via&utm_content=profile&utm_medium=member_ios" class="text-gray-500 hover:text-gray-700 dark:hover:text-gray-300 transition-colors">
              <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-700 dark:hover:text-gray-300 transition-colors">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="https://www.instagram.com/merhunmark?igsh=MW40cm1lNHZ2N2dlcQ%3D%3D&utm_source=qr" class="h-10 w-10 rounded-full bg-gray-100 dark:bg-gray-700 flex items-center justify-center hover:bg-pink-500 hover:text-white transition-colors" class="text-gray-500 hover:text-gray-700 dark:hover:text-gray-300 transition-colors">
              <i class="fab fa-instagram"></i>
            </a>
          </div>
        </div>
      </div>
    </footer>
  </div>

  <script>
    // Theme toggle
    const themeToggle = document.getElementById('theme-toggle');
    const mobileThemeToggle = document.getElementById('mobile-theme-toggle');
    const html = document.documentElement;
    
    function toggleTheme() {
      if (html.classList.contains('dark')) {
        html.classList.remove('dark');
        localStorage.setItem('theme', 'light');
      } else {
        html.classList.add('dark');
        localStorage.setItem('theme', 'dark');
      }
    }

    // Apply saved theme
    (function applySavedTheme() {
      const savedTheme = localStorage.getItem('theme');
      if (savedTheme === 'dark') {
        html.classList.add('dark');
      } else if (savedTheme === 'light') {
        html.classList.remove('dark');
      }
    })();

    // Mobile menu toggle
    const mobileMenuButton = document.getElementById('mobile-menu-button');
    const mobileMenu = document.getElementById('mobile-menu');
    
    mobileMenuButton.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });

    // Close mobile menu when clicking a link
    document.querySelectorAll('#mobile-menu a').forEach(link => {
      link.addEventListener('click', () => {
        mobileMenu.classList.add('hidden');
      });
    });

    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const targetId = this.getAttribute('href');
        const targetElement = document.querySelector(targetId);
        
        if (targetElement) {
          window.scrollTo({
            top: targetElement.offsetTop - 80,
            behavior: 'smooth'
          });
        }
      });
    });

    // Form submission
    const contactForm = document.getElementById('contact-form');
    if (contactForm) {
      contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        // Here you would typically send the form data to a server
        alert('Thank you for your message! I will get back to you soon.');
        this.reset();
      });
    }

    // Theme toggle events
    if (themeToggle) themeToggle.addEventListener('click', toggleTheme);
    if (mobileThemeToggle) mobileThemeToggle.addEventListener('click', toggleTheme);
  </script>
</body>
</html>
