# Aplicativo-De-Relacinamento
Desenvolvimento 
<!DOCTYPE html>

<!-- VS Code Settings -->
<!--
{
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "files.associations": {
        "*.html": "html"
    },
    "emmet.includeLanguages": {
        "html": "html"
    },
    "liveServer.settings.donotVerifyTags": true,
    "liveServer.settings.AdvanceCustomBrowserCmdLine": "",
    "liveServer.settings.ChromeDebuggingAttachment": false,
    "liveServer.settings.ignoreFiles": [
        ".vscode/**",
        "**/*.scss",
        "**/*.sass"
    ]
}
-->
<html lang="en">
<head>
    <meta charset="UTF-8">
                <div class="relative group">
                    <button class="gender-filter p-2 rounded-full hover:bg-gray-200 dark:hover:bg-gray-700">
                        <i class="fas fa-venus-mars"></i>
                    </button>
                    <div class="absolute right-0 mt-2 w-48 bg-white dark:bg-gray-800 rounded-md shadow-lg hidden group-hover:block z-50">
                        <div class="py-1">
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700 flex items-center">
                                <span class="w-3 h-3 rounded-full bg-[var(--gender-male)] mr-2"></span> Male
                            </a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700 flex items-center">
                                <span class="w-3 h-3 rounded-full bg-[var(--gender-female)] mr-2"></span> Female
                            </a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700 flex items-center">
                                <span class="w-3 h-3 rounded-full bg-[var(--gender-nonbinary)] mr-2"></span> Non-binary
                            </a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700 flex items-center">
                                <span class="w-3 h-3 rounded-full bg-[var(--gender-bisexual)] mr-2"></span> Bisexual
                            </a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700 flex items-center">
                                <span class="w-3 h-3 rounded-full bg-[var(--gender-trans)] mr-2"></span> Trans
                            </a>
                        </div>
                    </div>
                </div>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GlobalConnect - Dating App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6C63FF;
            --secondary: #4D4C7D;
            --dark: #363062;
            --light: #F5F5F5;
            --success: #3BB143;
            --gender-male: #4A90E2;
            --gender-female: #FF6B8B;
            --gender-nonbinary: #9B59B6;
            --gender-bisexual: #FF8C42;
            --gender-trans: #5BC0EB;
        }
        
        .dark-mode {
            --primary: #7D72E1;
            --secondary: #5A5773;
            --dark: #2A2740;
            --light: #3A3A3A;
            --success: #4CD964;
            background-color: #2A2740;
            color: #F5F5F5;
        }
        
        .dark-mode .card {
            background-color: #2f3542;
            border-color: #57606f;
        }
        
        .dark-mode .navbar {
            background-color: #1e272e;
            border-color: #57606f;
        }
        
        .premium-badge {
            background: linear-gradient(45deg, #ff9a9e, #fad0c4);
            color: white;
        }
        
        .match-animation {
            animation: pulse 1.5s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .language-selector {
            transition: all 0.3s ease;
        }
        
        .language-selector:hover {
            transform: translateY(-3px);
        }
    </style>
</head>
<body class="bg-gray-100 transition-colors duration-300">
    <!-- Navigation Bar -->
    <nav class="navbar bg-white shadow-md p-4 fixed w-full top-0 z-50 transition-colors duration-300">
        <div class="container mx-auto flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-heart text-2xl text-red-500"></i>
                <span class="text-xl font-bold">GlobalConnect</span>
            </div>
            
            <div class="flex items-center space-x-4">
                <button id="darkModeToggle" class="p-2 rounded-full hover:bg-gray-200 dark:hover:bg-gray-700">
                    <i class="fas fa-moon"></i>
                </button>
                
                <div class="relative group">
                    <button class="language-selector flex items-center space-x-1 p-2 rounded-full hover:bg-gray-200 dark:hover:bg-gray-700">
                        <i class="fas fa-globe"></i>
                        <span>EN</span>
                    </button>
                    <div class="absolute right-0 mt-2 w-48 bg-white dark:bg-gray-800 rounded-md shadow-lg hidden group-hover:block z-50">
                        <div class="py-1">
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">English</a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Español</a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Português</a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Français</a>
                            <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Deutsch</a>
                        </div>
                    </div>
                </div>
                
                <button id="menuToggle" class="p-2 rounded-full hover:bg-gray-200 dark:hover:bg-gray-700">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <div class="container mx-auto mt-20 p-4">
        <!-- Profile Cards -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Profile Card 1 -->
            <div class="card bg-white rounded-xl shadow-md overflow-hidden transition-transform duration-300 hover:shadow-lg dark:bg-gray-800">
                <div class="relative">
                    <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Profile" class="w-full h-64 object-cover">
                    <div class="absolute top-2 right-2 premium-badge px-2 py-1 rounded-full text-xs font-bold">
                        <i class="fas fa-crown mr-1"></i> PREMIUM
                    </div>
                    <div class="absolute bottom-2 left-2 flex space-x-2">
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-map-marker-alt mr-1 text-xs"></i> Brazil
                        </span>
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-language mr-1 text-xs"></i> PT, EN
                        </span>
                    </div>
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start">
                        <div>
                            <div class="flex items-center space-x-2">
                                <h3 class="font-bold text-xl">Ana, 28</h3>
                                <span class="gender-badge px-2 py-1 rounded-full text-xs font-bold" style="background-color: var(--gender-female); color: white;">
                                    <i class="fas fa-venus mr-1"></i> Female
                                </span>
                            </div>
                            <p class="text-gray-600 dark:text-gray-400">Photographer</p>
                        </div>
                        <div class="flex space-x-2">
                            <button class="like-btn p-2 rounded-full bg-red-100 text-red-500 hover:bg-red-200">
                                <i class="fas fa-heart"></i>
                            </button>
                            <button class="message-btn p-2 rounded-full bg-blue-100 text-blue-500 hover:bg-blue-200">
                                <i class="fas fa-comment"></i>
                            </button>
                        </div>
                    </div>
                    <p class="mt-2 text-gray-700 dark:text-gray-300">Adventure seeker and coffee lover. Let's explore the world together!</p>
                    <div class="mt-4 flex justify-between items-center">
                        <div class="flex space-x-1">
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Travel</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Photography</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Coffee</span>
                        </div>
                        <span class="text-xs text-gray-500">5km away</span>
                    </div>
                </div>
            </div>
            
            <!-- Profile Card 2 -->
            <div class="card bg-white rounded-xl shadow-md overflow-hidden transition-transform duration-300 hover:shadow-lg dark:bg-gray-800">
                <div class="relative">
                    <img src="https://randomuser.me/api/portraits/men/45.jpg" alt="Profile" class="w-full h-64 object-cover">
                    <div class="absolute bottom-2 left-2 flex space-x-2">
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-map-marker-alt mr-1 text-xs"></i> France
                        </span>
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-language mr-1 text-xs"></i> FR, EN
                        </span>
                    </div>
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start">
                        <div>
                            <div class="flex items-center space-x-2">
                                <h3 class="font-bold text-xl">Pierre, 32</h3>
                                <span class="gender-badge px-2 py-1 rounded-full text-xs font-bold" style="background-color: var(--gender-male); color: white;">
                                    <i class="fas fa-mars mr-1"></i> Male
                                </span>
                            </div>
                            <p class="text-gray-600 dark:text-gray-400">Chef</p>
                        </div>
                        <div class="flex space-x-2">
                            <button class="like-btn p-2 rounded-full bg-red-100 text-red-500 hover:bg-red-200">
                                <i class="fas fa-heart"></i>
                            </button>
                            <button class="message-btn p-2 rounded-full bg-blue-100 text-blue-500 hover:bg-blue-200">
                                <i class="fas fa-comment"></i>
                            </button>
                        </div>
                    </div>
                    <p class="mt-2 text-gray-700 dark:text-gray-300">Creating culinary magic. Looking for someone to share my passion for food and life.</p>
                    <div class="mt-4 flex justify-between items-center">
                        <div class="flex space-x-1">
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Cooking</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Wine</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Travel</span>
                        </div>
                        <span class="text-xs text-gray-500">12km away</span>
                    </div>
                </div>
            </div>
            
            <!-- Profile Card 3 -->
            <div class="card bg-white rounded-xl shadow-md overflow-hidden transition-transform duration-300 hover:shadow-lg dark:bg-gray-800">
                <div class="relative">
                    <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Profile" class="w-full h-64 object-cover">
                    <div class="absolute top-2 right-2 premium-badge px-2 py-1 rounded-full text-xs font-bold">
                        <i class="fas fa-crown mr-1"></i> PREMIUM
                    </div>
                    <div class="absolute bottom-2 left-2 flex space-x-2">
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-map-marker-alt mr-1 text-xs"></i> Japan
                        </span>
                        <span class="bg-white dark:bg-gray-800 px-2 py-1 rounded-full text-xs font-bold flex items-center">
                            <i class="fas fa-language mr-1 text-xs"></i> JP, EN
                        </span>
                    </div>
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start">
                        <div>
                            <h3 class="font-bold text-xl">Yuki, 26</h3>
                            <p class="text-gray-600 dark:text-gray-400">Graphic Designer</p>
                        </div>
                        <div class="flex space-x-2">
                            <button class="like-btn p-2 rounded-full bg-red-100 text-red-500 hover:bg-red-200">
                                <i class="fas fa-heart"></i>
                            </button>
                            <button class="message-btn p-2 rounded-full bg-blue-100 text-blue-500 hover:bg-blue-200">
                                <i class="fas fa-comment"></i>
                            </button>
                        </div>
                    </div>
                    <p class="mt-2 text-gray-700 dark:text-gray-300">Creative soul looking for meaningful connections. Love art, anime, and long walks.</p>
                    <div class="mt-4 flex justify-between items-center">
                        <div class="flex space-x-1">
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Art</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Anime</span>
                            <span class="bg-gray-200 dark:bg-gray-700 px-2 py-1 rounded-full text-xs">Nature</span>
                        </div>
                        <span class="text-xs text-gray-500">8km away</span>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Match Notification (Hidden by default) -->
        <div id="matchNotification" class="fixed bottom-4 right-4 bg-white dark:bg-gray-800 p-4 rounded-xl shadow-xl z-50 hidden match-animation">
            <div class="flex items-center space-x-4">
                <div class="relative">
                    <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Match" class="w-16 h-16 rounded-full object-cover">
                    <div class="absolute -bottom-1 -right-1 bg-green-500 rounded-full p-1">
                        <i class="fas fa-check text-white text-xs"></i>
                    </div>
                </div>
                <div>
                    <h4 class="font-bold">It's a match!</h4>
                    <p class="text-sm text-gray-600 dark:text-gray-400">You and Ana liked each other</p>
                    <button class="mt-2 bg-red-500 text-white px-3 py-1 rounded-full text-sm hover:bg-red-600">Say Hi</button>
                </div>
                <button id="closeMatch" class="absolute top-2 right-2 text-gray-400 hover:text-gray-600 dark:hover:text-gray-300">
                    <i class="fas fa-times"></i>
                </button>
            </div>
        </div>
        
        <!-- Subscription Modal (Hidden by default) -->
        <div id="subscriptionModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
            <div class="bg-white dark:bg-gray-800 rounded-xl p-6 max-w-md w-full mx-4">
                <div class="flex justify-between items-center mb-4">
                    <h3 class="text-xl font-bold">Upgrade to Premium</h3>
                    <button id="closeModal" class="text-gray-500 hover:text-gray-700 dark:hover:text-gray-300">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                
                <div class="space-y-4">
                    <div class="border border-gray-200 dark:border-gray-700 rounded-lg p-4">
                        <div class="flex justify-between items-center">
                            <div>
                                <h4 class="font-bold">GlobalConnect Premium</h4>
                                <p class="text-sm text-gray-600 dark:text-gray-400">Unlock all features</p>
                            </div>
                            <span class="text-lg font-bold">$9.99/month</span>
                        </div>
                        <ul class="mt-3 space-y-2 text-sm">
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Unlimited likes</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>See who liked you</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Advanced filters</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Message read receipts</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Priority customer support</span>
                            </li>
                        </ul>
                        <button class="mt-4 w-full bg-gradient-to-r from-pink-500 to-red-500 text-white py-2 rounded-lg font-bold hover:opacity-90">
                            Subscribe Now
                        </button>
                    </div>
                    
                    <div class="border border-gray-200 dark:border-gray-700 rounded-lg p-4">
                        <div class="flex justify-between items-center">
                            <div>
                                <h4 class="font-bold">GlobalConnect Gold</h4>
                                <p class="text-sm text-gray-600 dark:text-gray-400">Best value - Save 50%</p>
                            </div>
                            <span class="text-lg font-bold">$49.99/year</span>
                        </div>
                        <ul class="mt-3 space-y-2 text-sm">
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>All Premium features</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Profile boost weekly</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Exclusive badge</span>
                            </li>
                            <li class="flex items-center">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Travel mode (change location)</span>
                            </li>
                        </ul>
                        <button class="mt-4 w-full bg-gradient-to-r from-yellow-500 to-orange-500 text-white py-2 rounded-lg font-bold hover:opacity-90">
                            Get Gold Plan
                        </button>
                    </div>
                </div>
                
                <p class="mt-4 text-xs text-gray-500 text-center">Subscription automatically renews unless canceled at least 24 hours before the end of the current period.</p>
            </div>
        </div>
    </div>
    
    <!-- Bottom Navigation -->
    <div class="fixed bottom-0 left-0 right-0 bg-white dark:bg-gray-800 shadow-lg p-3 flex justify-around items-center z-40">
        <button class="flex flex-col items-center text-gray-600 dark:text-gray-400 hover:text-red-500 dark:hover:text-red-400">
            <i class="fas fa-home text-xl"></i>
            <span class="text-xs mt-1">Home</span>
        </button>
        <button class="flex flex-col items-center text-gray-600 dark:text-gray-400 hover:text-red-500 dark:hover:text-red-400">
            <i class="fas fa-search text-xl"></i>
            <span class="text-xs mt-1">Discover</span>
        </button>
        <button class="flex flex-col items-center text-red-500">
            <div class="relative">
                <i class="fas fa-heart text-2xl"></i>
                <span class="absolute -top-2 -right-2 bg-red-500 text-white text-xs rounded-full w-5 h-5 flex items-center justify-center">3</span>
            </div>
            <span class="text-xs mt-1">Matches</span>
        </button>
        <button class="flex flex-col items-center text-gray-600 dark:text-gray-400 hover:text-red-500 dark:hover:text-red-400">
            <i class="fas fa-comment text-xl"></i>
            <span class="text-xs mt-1">Messages</span>
        </button>
        <button class="flex flex-col items-center text-gray-600 dark:text-gray-400 hover:text-red-500 dark:hover:text-red-400">
            <i class="fas fa-user text-xl"></i>
            <span class="text-xs mt-1">Profile</span>
        </button>
    </div>

    <script>
        // Dark Mode Toggle
        const darkModeToggle = document.getElementById('darkModeToggle');
        const body = document.body;
        
        // Check for saved user preference
        if (localStorage.getItem('darkMode') === 'enabled') {
            body.classList.add('dark-mode');
            darkModeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
        
        darkModeToggle.addEventListener('click', () => {
            body.classList.toggle('dark-mode');
            
            if (body.classList.contains('dark-mode')) {
                localStorage.setItem('darkMode', 'enabled');
                darkModeToggle.innerHTML = '<i class="fas fa-sun"></i>';
            } else {
                localStorage.setItem('darkMode', 'disabled');
                darkModeToggle.innerHTML = '<i class="fas fa-moon"></i>';
            }
        });
        
        // Like Button Animation
        const likeButtons = document.querySelectorAll('.like-btn');
        likeButtons.forEach(button => {
            button.addEventListener('click', function() {
                this.innerHTML = '<i class="fas fa-heart text-red-500"></i>';
                this.classList.add('animate-ping');
                
                // Show match notification 30% of the time
                if (Math.random() < 0.3) {
                    setTimeout(() => {
                        document.getElementById('matchNotification').classList.remove('hidden');
                    }, 1000);
                }
                
                setTimeout(() => {
                    this.classList.remove('animate-ping');
                }, 500);
            });
        });
        
        // Close Match Notification
        document.getElementById('closeMatch').addEventListener('click', function() {
            document.getElementById('matchNotification').classList.add('hidden');
        });
        
        // Message Button - Show subscription modal for free users
        const messageButtons = document.querySelectorAll('.message-btn');
        messageButtons.forEach(button => {
            button.addEventListener('click', function() {
                document.getElementById('subscriptionModal').classList.remove('hidden');
            });
        });
        
        // Close Subscription Modal
        document.getElementById('closeModal').addEventListener('click', function() {
            document.getElementById('subscriptionModal').classList.add('hidden');
        });
        
        // Close modal when clicking outside
        document.getElementById('subscriptionModal').addEventListener('click', function(e) {
            if (e.target === this) {
                this.classList.add('hidden');
            }
        });
        
        // Responsive menu toggle
        document.getElementById('menuToggle').addEventListener('click', function() {
            alert('Menu functionality would be implemented here in a full app');
        });
        
        // Simulate loading more profiles when scrolling
        window.addEventListener('scroll', function() {
            if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight - 500) {
                // In a real app, this would load more profiles via AJAX
                console.log('Loading more profiles...');
            }
        });
    </script>
</body>
</html>
