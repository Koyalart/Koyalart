## Hi there 👋

<!--
**Koyalart/Koyalart** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Koyal Art Laser Zone - Custom Gifts & Laser Cutting</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#00E5E5',       /* Cyan/teal from logo */
                        primaryDark: '#00B5B5',   /* Darker teal */
                        secondary: '#FF3378',     /* Pink/red from logo */
                        secondaryDark: '#E02060', /* Darker pink */
                        accent: '#FFE000',        /* Yellow/gold from logo */
                        accentDark: '#E6CA00',    /* Darker gold */
                        light: '#FFFFFF',
                        dark: '#181818',
                        darkGray: '#333333',
                        lightGray: '#F5F5F5'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }

        // Check for dark mode preference
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

        body {
            font-family: 'Inter', sans-serif;
        }

        /* Hide scrollbar but allow scrolling */
        .hide-scrollbar {
            -ms-overflow-style: none;  /* IE and Edge */
            scrollbar-width: none;  /* Firefox */
        }
        
        .hide-scrollbar::-webkit-scrollbar {
            display: none;  /* Chrome, Safari and Opera */
        }

        .hero-pattern {
            background-color: #00E5E5;
            background-image: radial-gradient(#7cffff 0.5px, transparent 0.5px), radial-gradient(#7cffff 0.5px, #00E5E5 0.5px);
            background-size: 20px 20px;
            background-position: 0 0, 10px 10px;
        }

        .dark .hero-pattern {
            background-color: #00B5B5;
            background-image: radial-gradient(#5ce8e8 0.5px, transparent 0.5px), radial-gradient(#5ce8e8 0.5px, #00B5B5 0.5px);
        }

        .card {
            transition: all 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 0.5rem;
        }

        .gallery-item img {
            transition: transform 0.5s;
        }

        .gallery-item:hover img {
            transform: scale(1.05);
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0) 100%);
            padding: 1rem;
            color: white;
            transform: translateY(100%);
            transition: transform 0.3s;
        }

        .gallery-item:hover .gallery-overlay {
            transform: translateY(0);
        }

        .custom-input {
            transition: all 0.3s;
        }

        .custom-input:focus {
            border-color: #00E5E5;
            box-shadow: 0 0 0 3px rgba(0, 229, 229, 0.2);
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate-fadeIn {
            animation: fadeIn 0.5s ease-out forwards;
        }

        /* Mobile menu animation */
        .mobile-menu {
            transition: transform 0.3s ease-in-out;
            transform: translateX(-100%);
        }

        .mobile-menu.open {
            transform: translateX(0);
        }

        /* Laser animation */
        @keyframes laserBeam {
            0% { transform: scale(1); opacity: 0.6; }
            50% { transform: scale(1.2); opacity: 1; }
            100% { transform: scale(1); opacity: 0.6; }
        }
        
        .laser-beam {
            animation: laserBeam 2s infinite;
            transform-origin: center;
        }

        /* Logo glow effect */
        .logo-glow {
            filter: drop-shadow(0 0 5px rgba(0, 229, 229, 0.5));
            transition: filter 0.3s ease;
        }
        
        .logo-glow:hover {
            filter: drop-shadow(0 0 8px rgba(0, 229, 229, 0.8));
        }

        /* Neon text effect */
        .neon-text {
            text-shadow: 0 0 5px rgba(0, 229, 229, 0.5),
                         0 0 10px rgba(0, 229, 229, 0.3);
        }

        /* Cart animation */
        @keyframes cartBounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        
        .cart-bounce {
            animation: cartBounce 1s ease infinite;
        }

        /* Toast notification */
        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 9999;
            transition: all 0.3s ease;
            transform: translateY(100px);
            opacity: 0;
        }
        
        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }

        /* Make scrollbar nicer */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: transparent;
        }

        ::-webkit-scrollbar-thumb {
            background-color: rgba(155, 155, 155, 0.5);
            border-radius: 20px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background-color: rgba(155, 155, 155, 0.8);
        }

        /* Admin panel styles */
        .admin-panel {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            max-width: 100%;
            height: 100%;
            z-index: 1000;
            transition: right 0.3s ease;
        }
        
        .admin-panel.open {
            right: 0;
        }
        
        .admin-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 999;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease;
        }
        
        .admin-overlay.show {
            opacity: 1;
            visibility: visible;
        }

        /* Modal styles */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1001;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease;
        }
        
        .modal.show {
            opacity: 1;
            visibility: visible;
        }
        
        .modal-content {
            background-color: white;
            border-radius: 0.5rem;
            width: 100%;
            max-width: 500px;
            max-height: 90vh;
            overflow-y: auto;
            transform: translateY(20px);
            transition: transform 0.3s ease;
        }
        
        .modal.show .modal-content {
            transform: translateY(0);
        }
        
        .dark .modal-content {
            background-color: #333;
            color: white;
        }

        /* Product image container aspect ratio */
        .product-img-container {
            position: relative;
            width: 100%;
            padding-top: 100%; /* 1:1 aspect ratio */
            overflow: hidden;
        }
        
        .product-img-container img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    </style>
</head>
<body class="bg-light dark:bg-dark text-gray-800 dark:text-gray-200">
    <!-- Header/Navigation -->
    <header class="sticky top-0 z-50 bg-white dark:bg-darkGray shadow-md">
        <div class="container mx-auto px-4 py-3">
            <div class="flex justify-between items-center">
                <div class="flex items-center">
                    <div class="logo-glow h-12">
                        <img src="https://pfst.cf2.poecdn.net/base/image/f13c1583bc049c44c3588c057dc64e67309f1f35026c1e219a9e743281b8cb6a?w=200&h=auto" alt="Koyal Art Laser Zone" class="h-full">
                    </div>
                </div>
                
                <!-- Desktop Navigation -->
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Home</a>
                    <a href="#services" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Services</a>
                    <a href="#shop" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Shop</a>
                    <a href="#gallery" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Gallery</a>
                    <a href="#custom-order" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Custom Order</a>
                    <a href="#contact" class="font-medium hover:text-primary dark:hover:text-primary transition-colors">Contact</a>
                </nav>
                
                <div class="flex items-center">
                    <!-- Cart Button -->
                    <button id="cart-button" class="relative p-2 text-gray-500 dark:text-gray-400 hover:text-primary dark:hover:text-primary">
                        <i class="fas fa-shopping-cart text-xl"></i>
                        <span id="cart-count" class="absolute -top-1 -right-1 bg-secondary text-white text-xs rounded-full h-5 w-5 flex items-center justify-center">0</span>
                    </button>
                    
                    <!-- Admin Login Button -->
                    <button id="admin-login-button" class="ml-4 p-2 text-gray-500 dark:text-gray-400 hover:text-primary dark:hover:text-primary">
                        <i class="fas fa-user-shield text-xl"></i>
                    </button>
                    
                    <!-- Mobile menu button -->
                    <button id="mobile-menu-button" class="md:hidden ml-4 text-gray-500 dark:text-gray-400 hover:text-primary dark:hover:text-primary">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile Navigation -->
        <div id="mobile-menu" class="mobile-menu fixed top-0 left-0 bottom-0 w-64 bg-white dark:bg-darkGray shadow-lg z-50 md:hidden">
            <div class="p-4 border-b border-gray-200 dark:border-gray-700 flex justify-between items-center">
                <div class="h-8">
                    <img src="https://pfst.cf2.poecdn.net/base/image/f13c1583bc049c44c3588c057dc64e67309f1f35026c1e219a9e743281b8cb6a?w=160&h=auto" alt="Koyal Art Laser Zone" class="h-full">
                </div>
                <button id="close-mobile-menu" class="text-gray-500 dark:text-gray-400 hover:text-primary dark:hover:text-primary">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            <nav class="py-4">
                <a href="#home" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Home</a>
                <a href="#services" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Services</a>
                <a href="#shop" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Shop</a>
                <a href="#gallery" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Gallery</a>
                <a href="#custom-order" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Custom Order</a>
                <a href="#contact" class="mobile-nav-item block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-700">Contact</a>
            </nav>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="home" class="bg-gradient-to-r from-dark to-darkGray text-white py-20 md:py-32 relative overflow-hidden">
            <div class="absolute inset-0 opacity-30">
                <div class="laser-beam absolute top-1/3 left-1/4 w-16 h-16 rounded-full bg-accent"></div>
                <div class="laser-beam absolute top-2/3 right-1/3 w-10 h-10 rounded-full bg-primary" style="animation-delay: 0.5s;"></div>
                <div class="laser-beam absolute bottom-1/4 right-1/4 w-12 h-12 rounded-full bg-secondary" style="animation-delay: 1s;"></div>
            </div>
            <div class="container mx-auto px-4 relative z-10">
                <div class="max-w-3xl mx-auto text-center">
                    <div class="flex justify-center mb-10">
                        <img src="https://pfst.cf2.poecdn.net/base/image/f13c1583bc049c44c3588c057dc64e67309f1f35026c1e219a9e743281b8cb6a?w=300&h=auto" alt="Koyal Art Laser Zone" class="w-64 md:w-80 logo-glow">
                    </div>
                    <h1 class="text-4xl md:text-5xl font-bold mb-6 animate-fadeIn neon-text" style="animation-delay: 0.1s;">YOU THINK <span class="text-accent">WE CREATE</span></h1>
                    <p class="text-xl md:text-2xl mb-8 animate-fadeIn" style="animation-delay: 0.2s;">Custom gifts through laser cutting, neon art, and personalized printing</p>
                    <div class="flex flex-wrap justify-center gap-4 animate-fadeIn" style="animation-delay: 0.3s;">
                        <a href="#shop" class="bg-primary text-dark hover:bg-primaryDark px-6 py-3 rounded-full font-medium transition-colors">
                            Shop Now
                        </a>
                        <a href="#custom-order" class="bg-secondary hover:bg-secondaryDark px-6 py-3 rounded-full font-medium transition-colors">
                            Request Custom Order
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-16 bg-lightGray dark:bg-darkGray">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold mb-4 text-primary dark:text-primary">Our Services</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">We specialize in creating unique, personalized gifts and products using cutting-edge technology and artistic craftsmanship.</p>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Laser Cutting -->
                    <div class="card bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gradient-to-br from-accent to-primary flex items-center justify-center">
                            <div class="relative">
                                <i class="fas fa-cut text-6xl text-white"></i>
                                <div class="laser-beam absolute -bottom-4 left-1/2 transform -translate-x-1/2 w-8 h-2 bg-accent opacity-70"></div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2 text-primary">Laser Cutting</h3>
                            <p class="text-gray-600 dark:text-gray-400 mb-4">Custom laser-cut designs for wood, acrylic, and other materials. Perfect for signs, decorations, and personalized gifts.</p>
                            <ul class="space-y-2 mb-4">
                                <li class="flex items-center">
                                    <i class="fas fa-check text-accent mr-2"></i>
                                    <span>Personalized name signs</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-accent mr-2"></i>
                                    <span>Custom decorative pieces</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-accent mr-2"></i>
                                    <span>Intricate designs</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                    <!-- Neon Lights -->
                    <div class="card bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gradient-to-br from-primary to-secondary flex items-center justify-center">
                            <div class="relative">
                                <i class="fas fa-lightbulb text-6xl text-white neon-text"></i>
                                <div class="laser-beam absolute -bottom-4 left-1/2 transform -translate-x-1/2 w-8 h-2 bg-primary opacity-70"></div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2 text-primary">Neon Light Gifts</h3>
                            <p class="text-gray-600 dark:text-gray-400 mb-4">Bright, eye-catching neon light designs that add a unique glow to any space. Custom text and shapes available.</p>
                            <ul class="space-y-2 mb-4">
                                <li class="flex items-center">
                                    <i class="fas fa-check text-primary mr-2"></i>
                                    <span>Custom text signs</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-primary mr-2"></i>
                                    <span>Decorative light designs</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-primary mr-2"></i>
                                    <span>Logo illumination</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                    <!-- Custom Printing -->
                    <div class="card bg-white dark:bg-gray-800 rounded-xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gradient-to-br from-accent to-secondary flex items-center justify-center">
                            <div class="relative">
                                <i class="fas fa-tshirt text-6xl text-white"></i>
                                <div class="laser-beam absolute -bottom-4 left-1/2 transform -translate-x-1/2 w-8 h-2 bg-secondary opacity-70"></div>
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2 text-primary">Custom Printing</h3>
                            <p class="text-gray-600 dark:text-gray-400 mb-4">High-quality printing on t-shirts, cups, bottles, capes, bags, and more. Your designs or ours!</p>
                            <ul class="space-y-2 mb-4">
                                <li class="flex items-center">
                                    <i class="fas fa-check text-secondary mr-2"></i>
                                    <span>Apparel printing</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-secondary mr-2"></i>
                                    <span>Drinkware customization</span>
                                </li>
                                <li class="flex items-center">
                                    <i class="fas fa-check text-secondary mr-2"></i>
                                    <span>Accessories & bags</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Shop Section -->
        <section id="shop" class="py-16">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold mb-4 text-primary dark:text-primary">Shop Our Products</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">Browse our collection of handcrafted laser-cut gifts and personalized items.</p>
                </div>
                
                <!-- Category Filter -->
                <div class="mb-8 flex justify-center">
                    <div class="inline-flex flex-wrap gap-2 p-1 bg-gray-100 dark:bg-gray-800 rounded-full">
                        <button class="category-filter px-4 py-2 rounded-full text-sm font-medium bg-primary text-dark" data-category="all">All Products</button>
                        <button class="category-filter px-4 py-2 rounded-full text-sm font-medium text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700" data-category="clock">Clocks</button>
                        <button class="category-filter px-4 py-2 rounded-full text-sm font-medium text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700" data-category="light">LED & Neon</button>
                        <button class="category-filter px-4 py-2 rounded-full text-sm font-medium text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700" data-category="frames">Frames</button>
                        <button class="category-filter px-4 py-2 rounded-full text-sm font-medium text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-gray-700" data-category="accessories">Accessories</button>
                    </div>
                </div>
                
                <!-- Product Grid -->
                <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                    <!-- Products will be dynamically generated here -->
                </div>
            </div>
        </section>

        <!-- Gallery Section -->
        <section id="gallery" class="py-16 bg-lightGray dark:bg-darkGray">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold mb-4 text-primary dark:text-primary">Our Work</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">Browse through some of our favorite creations and get inspired for your custom order.</p>
                </div>
                
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                    <!-- Gallery items - using generated patterns instead of images -->
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="absolute inset-0 flex items-center justify-center">
                                <div class="w-2/3 h-2/3 border-2 border-primary rounded-lg flex items-center justify-center">
                                    <div class="text-5xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-primary to-accent neon-text">LOVE</div>
                                </div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Custom Neon Sign</h3>
                            <p class="text-sm">Personalized love sign for bedroom decor</p>
                        </div>
                    </div>
                    
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="relative w-3/4 h-3/4">
                                <div class="absolute inset-0 border-4 border-accent rounded-full"></div>
                                <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-3 h-3 bg-accent rounded-full"></div>
                                <div class="absolute top-1/2 left-1/2 h-2 w-1/3 bg-accent transform -translate-y-1/2 origin-left rotate-0"></div>
                                <div class="absolute top-1/2 left-1/2 h-2 w-1/4 bg-primary transform -translate-y-1/2 origin-left rotate-90"></div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Laser Cut Clock</h3>
                            <p class="text-sm">Minimalist design with custom engravings</p>
                        </div>
                    </div>
                    
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="relative w-1/2 aspect-square bg-white rounded-lg transform rotate-45">
                                <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-3/4 h-3/4 bg-gradient-to-br from-primary to-secondary rounded-lg rotate-45 flex items-center justify-center">
                                    <span class="text-white text-sm font-bold transform -rotate-45">Mug Design</span>
                                </div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Custom Printed Mug</h3>
                            <p class="text-sm">Perfect Mother's Day gift</p>
                        </div>
                    </div>
                    
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="w-3/4 h-1/2 border-2 border-secondary rounded-md flex flex-col items-center justify-center">
                                <div class="text-2xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-primary to-accent neon-text mb-2">FAMILY</div>
                                <div class="w-2/3 h-px bg-white"></div>
                                <div class="text-xs text-white mt-2">EST. 2022</div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Personalized Sign</h3>
                            <p class="text-sm">Custom laser-cut family name display</p>
                        </div>
                    </div>
                    
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="w-3/4 h-3/4 relative">
                                <div class="absolute inset-0 border-2 border-primary rounded-md"></div>
                                <div class="absolute top-1/4 left-1/2 transform -translate-x-1/2 w-1/2 h-1/2 bg-white rounded-sm flex items-center justify-center">
                                    <span class="text-xs font-bold text-darkGray">TEAM LOGO</span>
                                </div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Custom Printed T-Shirt</h3>
                            <p class="text-sm">Team merchandise with vibrant colors</p>
                        </div>
                    </div>
                    
                    <div class="gallery-item">
                        <div class="bg-gradient-to-br from-darkGray to-black aspect-square rounded-lg flex items-center justify-center relative overflow-hidden">
                            <div class="w-3/4 h-3/4 border-2 border-secondary rounded-full flex flex-col items-center justify-center">
                                <div class="text-lg font-bold text-primary">JOHN &</div>
                                <div class="text-lg font-bold text-accent">SARAH</div>
                                <div class="text-xs text-white mt-2">06.15.2023</div>
                            </div>
                            <div class="absolute bottom-0 w-full h-1/3 bg-gradient-to-t from-black to-transparent opacity-50"></div>
                        </div>
                        <div class="gallery-overlay">
                            <h3 class="font-bold">Wedding Gift</h3>
                            <p class="text-sm">Laser-cut commemorative piece</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Custom Order Section -->
        <section id="custom-order" class="py-16">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold mb-4 text-primary dark:text-primary">Request a Custom Order</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">Tell us about your project idea, and we'll help bring it to life.</p>
                </div>
                
                <div class="max-w-3xl mx-auto bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8">
                    <form id="order-form" class="space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="name" class="block text-sm font-medium mb-1">Your Name</label>
                                <input type="text" id="name" name="name" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium mb-1">Email Address</label>
                                <input type="email" id="email" name="email" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="phone" class="block text-sm font-medium mb-1">Phone Number</label>
                                <input type="tel" id="phone" name="phone" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                            </div>
                            <div>
                                <label for="product-type" class="block text-sm font-medium mb-1">Product Type</label>
                                <select id="product-type" name="product-type" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none">
                                    <option value="">Select an option</option>
                                    <option value="laser-cutting">Laser Cut Item</option>
                                    <option value="neon-sign">Neon Light Sign</option>
                                    <option value="tshirt">Custom T-Shirt</option>
                                    <option value="mug">Custom Mug</option>
                                    <option value="bottle">Custom Bottle</option>
                                    <option value="bag">Custom Bag</option>
                                    <option value="other">Other (Please Specify)</option>
                                </select>
                            </div>
                        </div>
                        
                        <div id="other-product-container" class="hidden">
                            <label for="other-product" class="block text-sm font-medium mb-1">Please Specify Product</label>
                            <input type="text" id="other-product" name="other-product" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none">
                        </div>
                        
                        <div>
                            <label for="description" class="block text-sm font-medium mb-1">Project Description</label>
                            <textarea id="description" name="description" rows="4" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none"></textarea>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium mb-1">Upload Reference Image (Optional)</label>
                            <div class="border-2 border-dashed border-gray-300 dark:border-gray-600 rounded-lg p-4 text-center">
                                <i class="fas fa-cloud-upload-alt text-2xl text-gray-400 mb-2"></i>
                                <p class="text-sm text-gray-500 dark:text-gray-400">Drag & drop your image here or click to browse</p>
                                <input type="file" id="reference-image" name="reference-image" class="hidden" accept="image/*">
                                <button type="button" id="browse-btn" class="mt-2 bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 px-4 py-2 rounded text-sm">Browse Files</button>
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="budget" class="block text-sm font-medium mb-1">Estimated Budget (Optional)</label>
                                <input type="text" id="budget" name="budget" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" placeholder="₹ Amount">
                            </div>
                            <div>
                                <label for="timeline" class="block text-sm font-medium mb-1">Desired Timeline (Optional)</label>
                                <input type="text" id="timeline" name="timeline" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" placeholder="e.g., 2 weeks">
                            </div>
                        </div>
                        
                        <div class="text-center">
                            <button type="submit" class="bg-accent hover:bg-accentDark text-dark px-8 py-3 rounded-full font-medium transition-colors">
                                Submit Request
                            </button>
                        </div>
                    </form>
                    
                    <div id="form-success" class="hidden mt-6 p-4 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-lg text-center">
                        <p class="font-medium">Your request has been submitted! We'll contact you soon.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-16 bg-lightGray dark:bg-darkGray">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold mb-4 text-primary dark:text-primary">Contact Us</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">Have questions or want to discuss your project? Reach out to us!</p>
                </div>
                
                <div class="max-w-5xl mx-auto">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <!-- Contact Info -->
                        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8" id="contact-info-section">
                            <h3 class="text-xl font-bold mb-6 text-primary">Get In Touch</h3>
                            
                            <div class="space-y-4">
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent flex items-center justify-center">
                                        <i class="fas fa-map-marker-alt text-dark"></i>
                                    </div>
                                    <div class="ml-4">
                                        <p class="font-medium">Visit Our Workshop</p>
                                        <p class="text-gray-600 dark:text-gray-400" id="address-display">123 Creative Lane, Artisan District<br>Your City, State 12345</p>
                                    </div>
                                </div>
                                
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-primary flex items-center justify-center">
                                        <i class="fas fa-envelope text-dark"></i>
                                    </div>
                                    <div class="ml-4">
                                        <p class="font-medium">Email Us</p>
                                        <p class="text-gray-600 dark:text-gray-400" id="email-display">info@koyalart.com</p>
                                    </div>
                                </div>
                                
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-secondary flex items-center justify-center">
                                        <i class="fas fa-phone text-white"></i>
                                    </div>
                                    <div class="ml-4">
                                        <p class="font-medium">Call Us</p>
                                        <p class="text-gray-600 dark:text-gray-400" id="phone-display">+91 8397070341</p>
                                    </div>
                                </div>
                                
                                <div class="flex items-start">
                                    <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent flex items-center justify-center">
                                        <i class="fas fa-clock text-dark"></i>
                                    </div>
                                    <div class="ml-4">
                                        <p class="font-medium">Business Hours</p>
                                        <p class="text-gray-600 dark:text-gray-400" id="hours-display">Monday - Saturday: 10 AM - 7 PM<br>Sunday: Closed</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="mt-8">
                                <h4 class="font-medium mb-4">Follow Us</h4>
                                <div class="flex space-x-4">
                                    <a href="#" class="h-10 w-10 rounded-full bg-primary flex items-center justify-center text-dark hover:bg-primaryDark transition-colors">
                                        <i class="fab fa-facebook-f"></i>
                                    </a>
                                    <a href="#" class="h-10 w-10 rounded-full bg-secondary flex items-center justify-center text-white hover:bg-secondaryDark transition-colors">
                                        <i class="fab fa-instagram"></i>
                                    </a>
                                    <a href="#" class="h-10 w-10 rounded-full bg-accent flex items-center justify-center text-dark hover:bg-accentDark transition-colors">
                                        <i class="fab fa-whatsapp"></i>
                                    </a>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Quick Contact Form -->
                        <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-6 md:p-8">
                            <h3 class="text-xl font-bold mb-6 text-primary">Quick Message</h3>
                            
                            <form id="contact-form" class="space-y-4">
                                <div>
                                    <label for="contact-name" class="block text-sm font-medium mb-1">Your Name</label>
                                    <input type="text" id="contact-name" name="contact-name" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                                </div>
                                
                                <div>
                                    <label for="contact-email" class="block text-sm font-medium mb-1">Email Address</label>
                                    <input type="email" id="contact-email" name="contact-email" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                                </div>
                                
                                <div>
                                    <label for="contact-message" class="block text-sm font-medium mb-1">Message</label>
                                    <textarea id="contact-message" name="contact-message" rows="4" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required></textarea>
                                </div>
                                
                                <button type="submit" class="w-full bg-accent hover:bg-accentDark text-dark px-6 py-3 rounded-lg font-medium transition-colors">
                                    Send Message
                                </button>
                            </form>
                            
                            <div id="contact-success" class="hidden mt-4 p-3 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-lg text-center">
                                <p>Your message has been sent! We'll get back to you soon.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="mb-4">
                        <img src="https://pfst.cf2.poecdn.net/base/image/f13c1583bc049c44c3588c057dc64e67309f1f35026c1e219a9e743281b8cb6a?w=200&h=auto" alt="Koyal Art Laser Zone" class="w-40 logo-glow">
                    </div>
                    <p class="text-gray-400">You Think, We Create. Transforming ideas into custom gifts with laser precision.</p>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4 text-primary">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#home" class="text-gray-400 hover:text-white transition-colors">Home</a></li>
                        <li><a href="#services" class="text-gray-400 hover:text-white transition-colors">Services</a></li>
                        <li><a href="#shop" class="text-gray-400 hover:text-white transition-colors">Shop</a></li>
                        <li><a href="#gallery" class="text-gray-400 hover:text-white transition-colors">Gallery</a></li>
                        <li><a href="#custom-order" class="text-gray-400 hover:text-white transition-colors">Custom Order</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition-colors">Contact</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4 text-primary">Services</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Laser Cutting</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Neon Signs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">T-Shirt Printing</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Mug Customization</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Bag Printing</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Custom Gifts</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="font-bold text-lg mb-4 text-primary">Newsletter</h4>
                    <p class="text-gray-400 mb-4">Subscribe to receive updates on new products and special offers.</p>
                    <form id="newsletter-form" class="space-y-3">
                        <input type="email" placeholder="Your email address" class="w-full px-4 py-2 rounded-lg bg-gray-800 border border-gray-700 text-white text-base focus:outline-none focus:border-primary">
                        <button type="submit" class="w-full bg-accent hover:bg-accentDark text-dark px-4 py-2 rounded-lg transition-colors">
                            Subscribe
                        </button>
                    </form>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-500">
                <p>&copy; 2023 Koyal Art Laser Zone. All rights reserved. | <span class="text-primary">YOU THINK, WE CREATE</span></p>
            </div>
        </div>
    </footer>

    <!-- Shopping Cart Modal -->
    <div id="cart-modal" class="modal">
        <div class="modal-content max-w-md p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-primary">Your Cart</h3>
                <button id="close-cart" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <div id="cart-items" class="space-y-4 max-h-80 overflow-y-auto mb-6">
                <!-- Cart items will be added here dynamically -->
                <div class="text-center py-8 text-gray-500 dark:text-gray-400" id="empty-cart-message">
                    <i class="fas fa-shopping-cart text-3xl mb-3"></i>
                    <p>Your cart is empty</p>
                </div>
            </div>
            
            <div id="cart-total" class="py-4 border-t border-gray-200 dark:border-gray-700 mb-6">
                <div class="flex justify-between items-center">
                    <span class="font-medium">Subtotal:</span>
                    <span class="font-bold text-lg">₹0.00</span>
                </div>
            </div>
            
            <div class="space-y-3">
                <button id="checkout-btn" class="w-full bg-accent hover:bg-accentDark text-dark py-3 rounded-lg font-medium transition-colors">
                    Proceed to Checkout
                </button>
                <button id="continue-shopping" class="w-full bg-transparent border border-gray-300 dark:border-gray-600 hover:bg-gray-100 dark:hover:bg-gray-700 py-3 rounded-lg font-medium transition-colors">
                    Continue Shopping
                </button>
            </div>
        </div>
    </div>

    <!-- Checkout Modal -->
    <div id="checkout-modal" class="modal">
        <div class="modal-content max-w-xl p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-primary">Checkout</h3>
                <button id="close-checkout" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <form id="checkout-form" class="space-y-6">
                <div>
                    <h4 class="font-medium text-lg mb-3">Order Summary</h4>
                    <div id="checkout-items" class="space-y-3 max-h-40 overflow-y-auto border border-gray-200 dark:border-gray-700 rounded-lg p-3 mb-3">
                        <!-- Checkout items will be added here dynamically -->
                    </div>
                    <div class="flex justify-between items-center font-bold text-lg">
                        <span>Total:</span>
                        <span id="checkout-total">₹0.00</span>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-medium text-lg mb-3">Shipping Information</h4>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div>
                            <label for="checkout-name" class="block text-sm font-medium mb-1">Full Name</label>
                            <input type="text" id="checkout-name" name="checkout-name" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        </div>
                        <div>
                            <label for="checkout-phone" class="block text-sm font-medium mb-1">Phone Number</label>
                            <input type="tel" id="checkout-phone" name="checkout-phone" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        </div>
                        <div class="md:col-span-2">
                            <label for="checkout-email" class="block text-sm font-medium mb-1">Email Address</label>
                            <input type="email" id="checkout-email" name="checkout-email" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        </div>
                        <div class="md:col-span-2">
                            <label for="checkout-address" class="block text-sm font-medium mb-1">Full Address</label>
                            <textarea id="checkout-address" name="checkout-address" rows="3" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required></textarea>
                        </div>
                        <div>
                            <label for="checkout-city" class="block text-sm font-medium mb-1">City</label>
                            <input type="text" id="checkout-city" name="checkout-city" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        </div>
                        <div>
                            <label for="checkout-pincode" class="block text-sm font-medium mb-1">PIN Code</label>
                            <input type="text" id="checkout-pincode" name="checkout-pincode" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h4 class="font-medium text-lg mb-3">Payment Method</h4>
                    <div class="space-y-3">
                        <div class="flex items-center">
                            <input type="radio" id="payment-cash" name="payment-method" value="cash" class="h-4 w-4 text-primary" checked>
                            <label for="payment-cash" class="ml-2">Cash on Delivery</label>
                        </div>
                        <div class="flex items-center">
                            <input type="radio" id="payment-upi" name="payment-method" value="upi" class="h-4 w-4 text-primary">
                            <label for="payment-upi" class="ml-2">UPI / Bank Transfer (Details will be sent via email)</label>
                        </div>
                    </div>
                </div>
                
                <div class="border-t border-gray-200 dark:border-gray-700 pt-6">
                    <button type="submit" class="w-full bg-accent hover:bg-accentDark text-dark py-3 rounded-lg font-medium transition-colors">
                        Place Order
                    </button>
                </div>
            </form>
            
            <div id="checkout-success" class="hidden mt-6 p-4 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-lg text-center">
                <p class="font-medium">Your order has been placed successfully! We'll contact you soon.</p>
            </div>
        </div>
    </div>

    <!-- Product Detail Modal -->
    <div id="product-modal" class="modal">
        <div class="modal-content max-w-4xl p-0">
            <div class="relative">
                <button id="close-product-modal" class="absolute top-4 right-4 text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200 bg-white dark:bg-gray-800 rounded-full h-8 w-8 flex items-center justify-center">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            
            <div class="flex flex-col md:flex-row">
                <div class="w-full md:w-1/2 bg-gray-100 dark:bg-gray-700 p-8 flex items-center justify-center">
                    <img id="modal-product-image" src="" alt="Product Image" class="max-h-80 object-contain">
                </div>
                
                <div class="w-full md:w-1/2 p-8">
                    <h3 id="modal-product-name" class="text-2xl font-bold text-primary mb-2"></h3>
                    <p id="modal-product-price" class="text-xl font-bold mb-4"></p>
                    <div id="modal-product-description" class="text-gray-600 dark:text-gray-400 mb-6"></div>
                    
                    <div class="mb-6">
                        <label for="modal-product-quantity" class="block text-sm font-medium mb-2">Quantity</label>
                        <div class="flex items-center">
                            <button id="decrease-quantity" class="h-10 w-10 bg-gray-200 dark:bg-gray-700 flex items-center justify-center rounded-l-lg">
                                <i class="fas fa-minus"></i>
                            </button>
                            <input type="number" id="modal-product-quantity" value="1" min="1" max="10" class="h-10 w-16 text-center border-y border-gray-300 dark:border-gray-600 bg-white dark:bg-gray-800">
                            <button id="increase-quantity" class="h-10 w-10 bg-gray-200 dark:bg-gray-700 flex items-center justify-center rounded-r-lg">
                                <i class="fas fa-plus"></i>
                            </button>
                        </div>
                    </div>
                    
                    <button id="add-to-cart-modal" class="w-full bg-accent hover:bg-accentDark text-dark py-3 rounded-lg font-medium transition-colors mb-3">
                        Add to Cart
                    </button>
                    
                    <button id="buy-now-modal" class="w-full bg-primary hover:bg-primaryDark text-dark py-3 rounded-lg font-medium transition-colors">
                        Buy Now
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Admin Login Modal -->
    <div id="admin-login-modal" class="modal">
        <div class="modal-content max-w-md p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-primary">Admin Login</h3>
                <button id="close-admin-login" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <form id="admin-login-form" class="space-y-6">
                <div>
                    <label for="admin-password" class="block text-sm font-medium mb-1">Password</label>
                    <input type="password" id="admin-password" name="admin-password" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                </div>
                
                <div id="admin-login-error" class="hidden p-3 bg-red-100 dark:bg-red-900 text-red-800 dark:text-red-200 rounded-lg text-center">
                    <p>Incorrect password. Please try again.</p>
                </div>
                
                <button type="submit" class="w-full bg-primary hover:bg-primaryDark text-dark py-3 rounded-lg font-medium transition-colors">
                    Login
                </button>
            </form>
        </div>
    </div>

    <!-- Admin Panel Sidebar -->
    <div id="admin-overlay" class="admin-overlay"></div>
    <div id="admin-panel" class="admin-panel bg-white dark:bg-gray-800 shadow-lg overflow-y-auto">
        <div class="p-4 border-b border-gray-200 dark:border-gray-700 flex justify-between items-center">
            <h3 class="font-bold text-xl text-primary">Admin Panel</h3>
            <button id="close-admin-panel" class="text-gray-500 dark:text-gray-400 hover:text-primary dark:hover:text-primary">
                <i class="fas fa-times text-xl"></i>
            </button>
        </div>
        
        <div class="p-4 space-y-6">
            <!-- Products Management Section -->
            <div>
                <h4 class="font-bold text-lg mb-3">Products Management</h4>
                <button id="add-product-btn" class="w-full bg-primary hover:bg-primaryDark text-dark py-2 rounded-lg font-medium transition-colors mb-3">
                    <i class="fas fa-plus mr-2"></i> Add New Product
                </button>
                <div>
                    <h5 class="font-medium mb-2">Current Products</h5>
                    <div id="admin-products-list" class="space-y-2 max-h-60 overflow-y-auto border border-gray-200 dark:border-gray-700 rounded p-2">
                        <!-- Product list will be generated here -->
                    </div>
                </div>
            </div>
            
            <!-- Orders Management Section -->
            <div>
                <h4 class="font-bold text-lg mb-3">Orders Management</h4>
                <div>
                    <h5 class="font-medium mb-2">Recent Orders</h5>
                    <div id="admin-orders-list" class="space-y-2 max-h-60 overflow-y-auto border border-gray-200 dark:border-gray-700 rounded p-2">
                        <!-- Order list will be generated here -->
                        <div class="text-center py-4 text-gray-500 dark:text-gray-400" id="empty-orders-message">
                            <p>No orders yet</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Contact Information Section -->
            <div>
                <h4 class="font-bold text-lg mb-3">Contact Information</h4>
                <form id="contact-info-form" class="space-y-3">
                    <div>
                        <label for="admin-address" class="block text-sm font-medium mb-1">Address</label>
                        <textarea id="admin-address" name="admin-address" rows="2" class="custom-input w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">123 Creative Lane, Artisan District
Your City, State 12345</textarea>
                    </div>
                    <div>
                        <label for="admin-email" class="block text-sm font-medium mb-1">Email</label>
                        <input type="email" id="admin-email" name="admin-email" value="info@koyalart.com" class="custom-input w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">
                    </div>
                    <div>
                        <label for="admin-phone" class="block text-sm font-medium mb-1">Phone</label>
                        <input type="tel" id="admin-phone" name="admin-phone" value="+91 8397070341" class="custom-input w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">
                    </div>
                    <div>
                        <label for="admin-hours" class="block text-sm font-medium mb-1">Business Hours</label>
                        <textarea id="admin-hours" name="admin-hours" rows="2" class="custom-input w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">Monday - Saturday: 10 AM - 7 PM
Sunday: Closed</textarea>
                    </div>
                    <button type="submit" class="w-full bg-accent hover:bg-accentDark text-dark py-2 rounded-lg font-medium transition-colors">
                        Update Contact Info
                    </button>
                </form>
            </div>
            
            <!-- Theme Customization -->
            <div>
                <h4 class="font-bold text-lg mb-3">Theme Settings</h4>
                <div class="space-y-3">
                    <div>
                        <label for="primary-color" class="block text-sm font-medium mb-1">Primary Color</label>
                        <div class="flex items-center">
                            <input type="color" id="primary-color" value="#00E5E5" class="h-10 w-12 border-0 p-0">
                            <input type="text" id="primary-color-hex" value="#00E5E5" class="custom-input flex-1 ml-2 px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">
                        </div>
                    </div>
                    <div>
                        <label for="accent-color" class="block text-sm font-medium mb-1">Accent Color</label>
                        <div class="flex items-center">
                            <input type="color" id="accent-color" value="#FFE000" class="h-10 w-12 border-0 p-0">
                            <input type="text" id="accent-color-hex" value="#FFE000" class="custom-input flex-1 ml-2 px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">
                        </div>
                    </div>
                    <div>
                        <label for="secondary-color" class="block text-sm font-medium mb-1">Secondary Color</label>
                        <div class="flex items-center">
                            <input type="color" id="secondary-color" value="#FF3378" class="h-10 w-12 border-0 p-0">
                            <input type="text" id="secondary-color-hex" value="#FF3378" class="custom-input flex-1 ml-2 px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-sm focus:outline-none">
                        </div>
                    </div>
                    <button id="apply-theme" class="w-full bg-accent hover:bg-accentDark text-dark py-2 rounded-lg font-medium transition-colors">
                        Apply Theme Changes
                    </button>
                </div>
            </div>
            
            <div class="pt-4 border-t border-gray-200 dark:border-gray-700 text-center">
                <button id="admin-logout" class="px-6 py-2 bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 rounded-lg font-medium transition-colors">
                    Logout
                </button>
            </div>
        </div>
    </div>

    <!-- Add/Edit Product Modal -->
    <div id="product-edit-modal" class="modal">
        <div class="modal-content max-w-2xl p-6">
            <div class="flex justify-between items-center mb-6">
                <h3 id="product-edit-title" class="text-xl font-bold text-primary">Add New Product</h3>
                <button id="close-product-edit" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <form id="product-edit-form" class="space-y-6">
                <input type="hidden" id="product-edit-id">
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label for="product-edit-name" class="block text-sm font-medium mb-1">Product Name</label>
                        <input type="text" id="product-edit-name" name="product-edit-name" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                    </div>
                    <div>
                        <label for="product-edit-price" class="block text-sm font-medium mb-1">Price (₹)</label>
                        <input type="number" id="product-edit-price" name="product-edit-price" min="0" step="0.01" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                    </div>
                </div>
                
                <div>
                    <label for="product-edit-category" class="block text-sm font-medium mb-1">Category</label>
                    <select id="product-edit-category" name="product-edit-category" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" required>
                        <option value="clock">Clocks</option>
                        <option value="light">LED & Neon</option>
                        <option value="frames">Frames</option>
                        <option value="accessories">Accessories</option>
                    </select>
                </div>
                
                <div>
                    <label for="product-edit-description" class="block text-sm font-medium mb-1">Description</label>
                    <textarea id="product-edit-description" name="product-edit-description" rows="3" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none"></textarea>
                </div>
                
                <div>
                    <label for="product-edit-image" class="block text-sm font-medium mb-1">Image URL</label>
                    <input type="text" id="product-edit-image" name="product-edit-image" class="custom-input w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 text-base focus:outline-none" placeholder="https://example.com/image.jpg">
                    <p class="mt-1 text-xs text-gray-500 dark:text-gray-400">Enter a URL or leave blank to use a generated image</p>
                </div>
                
                <div id="product-edit-image-preview" class="hidden mt-4">
                    <p class="text-sm font-medium mb-1">Image Preview</p>
                    <div class="flex justify-center border border-gray-300 dark:border-gray-600 rounded-lg p-4 bg-gray-100 dark:bg-gray-700">
                        <img id="preview-image" src="" alt="Product Preview" class="max-h-32 object-contain">
                    </div>
                </div>
                
                <div class="pt-4 border-t border-gray-200 dark:border-gray-700 flex justify-end space-x-3">
                    <button type="button" id="product-edit-cancel" class="px-6 py-2 bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 rounded-lg font-medium transition-colors">
                        Cancel
                    </button>
                    <button type="submit" class="px-6 py-2 bg-accent hover:bg-accentDark text-dark rounded-lg font-medium transition-colors">
                        Save Product
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="toast bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg">
        <div class="flex items-center">
            <i id="toast-icon" class="fas fa-check-circle mr-3 text-xl"></i>
            <p id="toast-message">Item added to cart!</p>
        </div>
    </div>

    <script>
        // Initial data
        const productsData = [
            {
                id: 1,
                name: "Customized Wall Clock",
                price: 899,
                category: "clock",
                image: "https://via.placeholder.com/300x300.png?text=Wall+Clock",
                description: "Personalized wall clock with custom photos. Perfect for gifting to loved ones."
            },
            {
                id: 2,
                name: "Keychains",
                price: 149,
                category: "accessories",
                image: "https://via.placeholder.com/300x300.png?text=Keychains",
                description: "Customized keychains with names or designs of your choice."
            },
            {
                id: 3,
                name: "Customized LED Wall Hanging",
                price: 1299,
                category: "light",
                image: "https://via.placeholder.com/300x300.png?text=LED+Wall+Hanging",
                description: "LED illuminated wall hangings for a stunning visual display."
            },
            {
                id: 4,
                name: "Wooden Clock",
                price: 799,
                category: "clock",
                image: "https://via.placeholder.com/300x300.png?text=Wooden+Clock",
                description: "Elegant wooden clock with laser-cut designs."
            },
            {
                id: 5,
                name: "Mug + Magic Mirror + Cushion Combo",
                price: 999,
                category: "accessories",
                image: "https://via.placeholder.com/300x300.png?text=Gift+Combo",
                description: "Complete gift combo with custom printed mug, magic mirror, and cushion."
            },
            {
                id: 6,
                name: "Baby Birth Frame",
                price: 1499,
                category: "frames",
                image: "https://via.placeholder.com/300x300.png?text=Baby+Frame",
                description: "Commemorate your baby's birth with this beautiful customized frame."
            },
            {
                id: 7,
                name: "Wooden Logo Light",
                price: 1000,
                category: "light",
                image: "https://via.placeholder.com/300x300.png?text=Logo+Light",
                description: "Custom wooden light with your logo or design engraved."
            },
            {
                id: 8,
                name: "LED Alphabet",
                price: 499,
                category: "light",
                image: "https://via.placeholder.com/300x300.png?text=LED+Alphabet",
                description: "Light up your space with custom LED alphabet signs."
            },
            {
                id: 9,
                name: "Table Top",
                price: 450,
                category: "accessories",
                image: "https://via.placeholder.com/300x300.png?text=Table+Top",
                description: "Customized table top with photos of your choice."
            },
            {
                id: 10,
                name: "Customised Wooden Frame",
                price: 700,
                category: "frames",
                image: "https://via.placeholder.com/300x300.png?text=Wooden+Frame",
                description: "Beautiful wooden frames customized with your designs or photos."
            },
            {
                id: 11,
                name: "Neon Sign",
                price: 600,
                category: "light",
                image: "https://via.placeholder.com/300x300.png?text=Neon+Sign",
                description: "Personalized neon signs for a vibrant addition to your space. Price varies by size."
            }
        ];
        
        let cart = [];
        let orders = [];
        const ADMIN_PASSWORD = "admin123"; // Simple password for demo purposes
        let isAdminLoggedIn = false;
        
        // DOM Elements
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize products
            renderProducts();
            renderAdminProductsList();
            
            // Mobile Menu
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const closeMobileMenuButton = document.getElementById('close-mobile-menu');
            const mobileMenu = document.getElementById('mobile-menu');
            const mobileNavItems = document.querySelectorAll('.mobile-nav-item');
            
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.add('open');
            });
            
            closeMobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.remove('open');
            });
            
            mobileNavItems.forEach(item => {
                item.addEventListener('click', () => {
                    mobileMenu.classList.remove('open');
                });
            });
            
            // Cart Modal
            const cartButton = document.getElementById('cart-button');
            const cartModal = document.getElementById('cart-modal');
            const closeCart = document.getElementById('close-cart');
            const continueShoppingBtn = document.getElementById('continue-shopping');
            
            cartButton.addEventListener('click', () => {
                updateCartDisplay();
                cartModal.classList.add('show');
            });
            
            closeCart.addEventListener('click', () => {
                cartModal.classList.remove('show');
            });
            
            continueShoppingBtn.addEventListener('click', () => {
                cartModal.classList.remove('show');
            });
            
            // Checkout
            const checkoutBtn = document.getElementById('checkout-btn');
            const checkoutModal = document.getElementById('checkout-modal');
            const closeCheckout = document.getElementById('close-checkout');
            
            checkoutBtn.addEventListener('click', () => {
                if (cart.length === 0) {
                    showToast('Your cart is empty!', 'error');
                    return;
                }
                
                updateCheckoutDisplay();
                cartModal.classList.remove('show');
                checkoutModal.classList.add('show');
            });
            
            closeCheckout.addEventListener('click', () => {
                checkoutModal.classList.remove('show');
            });
            
            // Product Modal
            const productModal = document.getElementById('product-modal');
            const closeProductModal = document.getElementById('close-product-modal');
            const decreaseQuantity = document.getElementById('decrease-quantity');
            const increaseQuantity = document.getElementById('increase-quantity');
            const quantityInput = document.getElementById('modal-product-quantity');
            const addToCartModalBtn = document.getElementById('add-to-cart-modal');
            const buyNowModalBtn = document.getElementById('buy-now-modal');
            
            closeProductModal.addEventListener('click', () => {
                productModal.classList.remove('show');
            });
            
            decreaseQuantity.addEventListener('click', () => {
                let value = parseInt(quantityInput.value);
                if (value > 1) {
                    quantityInput.value = value - 1;
                }
            });
            
            increaseQuantity.addEventListener('click', () => {
                let value = parseInt(quantityInput.value);
                if (value < 10) {
                    quantityInput.value = value + 1;
                }
            });
            
            addToCartModalBtn.addEventListener('click', () => {
                const productId = parseInt(addToCartModalBtn.dataset.productId);
                const quantity = parseInt(quantityInput.value);
                addToCart(productId, quantity);
                productModal.classList.remove('show');
            });
            
            buyNowModalBtn.addEventListener('click', () => {
                const productId = parseInt(buyNowModalBtn.dataset.productId);
                const quantity = parseInt(quantityInput.value);
                addToCart(productId, quantity);
                productModal.classList.remove('show');
                updateCheckoutDisplay();
                checkoutModal.classList.add('show');
            });
            
            // Admin Login
            const adminLoginButton = document.getElementById('admin-login-button');
            const adminLoginModal = document.getElementById('admin-login-modal');
            const closeAdminLogin = document.getElementById('close-admin-login');
            const adminLoginForm = document.getElementById('admin-login-form');
            const adminPanel = document.getElementById('admin-panel');
            const adminOverlay = document.getElementById('admin-overlay');
            const closeAdminPanel = document.getElementById('close-admin-panel');
            const adminLogout = document.getElementById('admin-logout');
            
            adminLoginButton.addEventListener('click', () => {
                if (isAdminLoggedIn) {
                    adminPanel.classList.add('open');
                    adminOverlay.classList.add('show');
                } else {
                    adminLoginModal.classList.add('show');
                }
            });
            
            closeAdminLogin.addEventListener('click', () => {
                adminLoginModal.classList.remove('show');
            });
            
            adminLoginForm.addEventListener('submit', (e) => {
                e.preventDefault();
                const password = document.getElementById('admin-password').value;
                
                if (password === ADMIN_PASSWORD) {
                    isAdminLoggedIn = true;
                    adminLoginModal.classList.remove('show');
                    adminPanel.classList.add('open');
                    adminOverlay.classList.add('show');
                    document.getElementById('admin-password').value = '';
                    document.getElementById('admin-login-error').classList.add('hidden');
                } else {
                    document.getElementById('admin-login-error').classList.remove('hidden');
                }
            });
            
            closeAdminPanel.addEventListener('click', () => {
                adminPanel.classList.remove('open');
                adminOverlay.classList.remove('show');
            });
            
            adminOverlay.addEventListener('click', () => {
                adminPanel.classList.remove('open');
                adminOverlay.classList.remove('show');
            });
            
            adminLogout.addEventListener('click', () => {
                isAdminLoggedIn = false;
                adminPanel.classList.remove('open');
                adminOverlay.classList.remove('show');
                showToast('Logged out successfully', 'success');
            });
            
            // Product Edit Modal
            const addProductBtn = document.getElementById('add-product-btn');
            const productEditModal = document.getElementById('product-edit-modal');
            const closeProductEdit = document.getElementById('close-product-edit');
            const productEditForm = document.getElementById('product-edit-form');
            const productEditCancel = document.getElementById('product-edit-cancel');
            const productEditImageInput = document.getElementById('product-edit-image');
            const productEditImagePreview = document.getElementById('product-edit-image-preview');
            const previewImage = document.getElementById('preview-image');
            
            addProductBtn.addEventListener('click', () => {
                document.getElementById('product-edit-title').textContent = 'Add New Product';
                document.getElementById('product-edit-id').value = '';
                document.getElementById('product-edit-name').value = '';
                document.getElementById('product-edit-price').value = '';
                document.getElementById('product-edit-category').value = 'clock';
                document.getElementById('product-edit-description').value = '';
                document.getElementById('product-edit-image').value = '';
                productEditImagePreview.classList.add('hidden');
                
                productEditModal.classList.add('show');
            });
            
            closeProductEdit.addEventListener('click', () => {
                productEditModal.classList.remove('show');
            });
            
            productEditCancel.addEventListener('click', () => {
                productEditModal.classList.remove('show');
            });
            
            productEditImageInput.addEventListener('input', () => {
                const imageUrl = productEditImageInput.value.trim();
                if (imageUrl) {
                    previewImage.src = imageUrl;
                    productEditImagePreview.classList.remove('hidden');
                } else {
                    productEditImagePreview.classList.add('hidden');
                }
            });
            
            productEditForm.addEventListener('submit', (e) => {
                e.preventDefault();
                
                const productId = document.getElementById('product-edit-id').value;
                const name = document.getElementById('product-edit-name').value;
                const price = parseFloat(document.getElementById('product-edit-price').value);
                const category = document.getElementById('product-edit-category').value;
                const description = document.getElementById('product-edit-description').value;
                let image = document.getElementById('product-edit-image').value;
                
                if (!image) {
                    image = `https://via.placeholder.com/300x300.png?text=${encodeURIComponent(name)}`;
                }
                
                if (productId) {
                    // Update existing product
                    const index = productsData.findIndex(p => p.id === parseInt(productId));
                    if (index !== -1) {
                        productsData[index] = {
                            ...productsData[index],
                            name,
                            price,
                            category,
                            description,
                            image
                        };
                        
                        showToast('Product updated successfully', 'success');
                    }
                } else {
                    // Add new product
                    const newId = Math.max(...productsData.map(p => p.id), 0) + 1;
                    const newProduct = {
                        id: newId,
                        name,
                        price,
                        category,
                        description,
                        image
                    };
                    
                    productsData.push(newProduct);
                    showToast('Product added successfully', 'success');
                }
                
                renderProducts();
                renderAdminProductsList();
                productEditModal.classList.remove('show');
            });
            
            // Contact info form
            const contactInfoForm = document.getElementById('contact-info-form');
            
            contactInfoForm.addEventListener('submit', (e) => {
                e.preventDefault();
                
                const address = document.getElementById('admin-address').value;
                const email = document.getElementById('admin-email').value;
                const phone = document.getElementById('admin-phone').value;
                const hours = document.getElementById('admin-hours').value;
                
                document.getElementById('address-display').innerHTML = address.replace(/\n/g, '<br>');
                document.getElementById('email-display').textContent = email;
                document.getElementById('phone-display').textContent = phone;
                document.getElementById('hours-display').innerHTML = hours.replace(/\n/g, '<br>');
                
                showToast('Contact information updated', 'success');
            });
            
            // Theme settings
            const applyThemeBtn = document.getElementById('apply-theme');
            const primaryColorInput = document.getElementById('primary-color');
            const primaryColorHex = document.getElementById('primary-color-hex');
            const accentColorInput = document.getElementById('accent-color');
            const accentColorHex = document.getElementById('accent-color-hex');
            const secondaryColorInput = document.getElementById('secondary-color');
            const secondaryColorHex = document.getElementById('secondary-color-hex');
            
            // Sync color inputs
            primaryColorInput.addEventListener('input', () => {
                primaryColorHex.value = primaryColorInput.value;
            });
            
            primaryColorHex.addEventListener('input', () => {
                if (/^#[0-9A-F]{6}$/i.test(primaryColorHex.value)) {
                    primaryColorInput.value = primaryColorHex.value;
                }
            });
            
            accentColorInput.addEventListener('input', () => {
                accentColorHex.value = accentColorInput.value;
            });
            
            accentColorHex.addEventListener('input', () => {
                if (/^#[0-9A-F]{6}$/i.test(accentColorHex.value)) {
                    accentColorInput.value = accentColorHex.value;
                }
            });
            
            secondaryColorInput.addEventListener('input', () => {
                secondaryColorHex.value = secondaryColorInput.value;
            });
            
            secondaryColorHex.addEventListener('input', () => {
                if (/^#[0-9A-F]{6}$/i.test(secondaryColorHex.value)) {
                    secondaryColorInput.value = secondaryColorHex.value;
                }
            });
            
            applyThemeBtn.addEventListener('click', () => {
                const primaryColor = primaryColorInput.value;
                const accentColor = accentColorInput.value;
                const secondaryColor = secondaryColorInput.value;
                
                // Create a style element to override Tailwind colors
                let styleElement = document.getElementById('custom-theme');
                if (!styleElement) {
                    styleElement = document.createElement('style');
                    styleElement.id = 'custom-theme';
                    document.head.appendChild(styleElement);
                }
                
                // Calculate darker variants
                const primaryDark = adjustColor(primaryColor, -30);
                const accentDark = adjustColor(accentColor, -30);
                const secondaryDark = adjustColor(secondaryColor, -30);
                
                styleElement.textContent = `
                    .text-primary { color: ${primaryColor} !important; }
                    .bg-primary { background-color: ${primaryColor} !important; }
                    .border-primary { border-color: ${primaryColor} !important; }
                    .hover\\:bg-primaryDark:hover { background-color: ${primaryDark} !important; }
                    .hover\\:text-primary:hover { color: ${primaryColor} !important; }
                    .hover\\:border-primary:hover { border-color: ${primaryColor} !important; }
                    
                    .text-accent { color: ${accentColor} !important; }
                    .bg-accent { background-color: ${accentColor} !important; }
                    .border-accent { border-color: ${accentColor} !important; }
                    .hover\\:bg-accentDark:hover { background-color: ${accentDark} !important; }
                    
                    .text-secondary { color: ${secondaryColor} !important; }
                    .bg-secondary { background-color: ${secondaryColor} !important; }
                    .border-secondary { border-color: ${secondaryColor} !important; }
                    .hover\\:bg-secondaryDark:hover { background-color: ${secondaryDark} !important; }
                    
                    .from-primary { --tw-gradient-from: ${primaryColor} !important; }
                    .to-primary { --tw-gradient-to: ${primaryColor} !important; }
                    .from-accent { --tw-gradient-from: ${accentColor} !important; }
                    .to-accent { --tw-gradient-to: ${accentColor} !important; }
                    .from-secondary { --tw-gradient-from: ${secondaryColor} !important; }
                    .to-secondary { --tw-gradient-to: ${secondaryColor} !important; }
                `;
                
                showToast('Theme updated successfully', 'success');
            });
            
            // Checkout form
            const checkoutForm = document.getElementById('checkout-form');
            
            checkoutForm.addEventListener('submit', (e) => {
                e.preventDefault();
                
                if (cart.length === 0) {
                    showToast('Your cart is empty!', 'error');
                    return;
                }
                
                const name = document.getElementById('checkout-name').value;
                const phone = document.getElementById('checkout-phone').value;
                const email = document.getElementById('checkout-email').value;
                const address = document.getElementById('checkout-address').value;
                const city = document.getElementById('checkout-city').value;
                const pincode = document.getElementById('checkout-pincode').value;
                const paymentMethod = document.querySelector('input[name="payment-method"]:checked').value;
                
                const order = {
                    id: Date.now(),
                    date: new Date().toISOString(),
                    customer: {
                        name,
                        phone,
                        email,
                        address,
                        city,
                        pincode
                    },
                    items: [...cart],
                    total: calculateTotal(),
                    paymentMethod,
                    status: 'Pending'
                };
                
                orders.push(order);
                renderAdminOrdersList();
                
                // Reset cart
                cart = [];
                updateCartCount();
                
                // Show success message
                document.getElementById('checkout-success').classList.remove('hidden');
                setTimeout(() => {
                    document.getElementById('checkout-success').classList.add('hidden');
                    checkoutModal.classList.remove('show');
                    checkoutForm.reset();
                    showToast('Order placed successfully!', 'success');
                }, 3000);
            });
            
            // Category filters
            const categoryFilters = document.querySelectorAll('.category-filter');
            
            categoryFilters.forEach(filter => {
                filter.addEventListener('click', () => {
                    // Update active state
                    categoryFilters.forEach(f => {
                        f.classList.remove('bg-primary', 'text-dark');
                        f.classList.add('text-gray-700', 'dark:text-gray-300', 'hover:bg-gray-200', 'dark:hover:bg-gray-700');
                    });
                    
                    filter.classList.remove('text-gray-700', 'dark:text-gray-300', 'hover:bg-gray-200', 'dark:hover:bg-gray-700');
                    filter.classList.add('bg-primary', 'text-dark');
                    
                    // Filter products
                    const category = filter.dataset.category;
                    renderProducts(category);
                });
            });
            
            // File upload handling
            const browseBtn = document.getElementById('browse-btn');
            const fileInput = document.getElementById('reference-image');
            
            browseBtn.addEventListener('click', () => {
                fileInput.click();
            });
            
            // Form submissions
            const orderForm = document.getElementById('order-form');
            const formSuccess = document.getElementById('form-success');
            
            orderForm.addEventListener('submit', (e) => {
                e.preventDefault();
                formSuccess.classList.remove('hidden');
                orderForm.reset();
                setTimeout(() => {
                    formSuccess.classList.add('hidden');
                    showToast('Custom order request submitted!', 'success');
                }, 3000);
            });
            
            const contactForm = document.getElementById('contact-form');
            const contactSuccess = document.getElementById('contact-success');
            
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                contactSuccess.classList.remove('hidden');
                contactForm.reset();
                setTimeout(() => {
                    contactSuccess.classList.add('hidden');
                    showToast('Message sent successfully!', 'success');
                }, 3000);
            });
            
            const newsletterForm = document.getElementById('newsletter-form');
            
            newsletterForm.addEventListener('submit', (e) => {
                e.preventDefault();
                newsletterForm.reset();
                showToast('Subscribed to newsletter!', 'success');
            });
            
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        window.scrollTo({
                            top: target.offsetTop - 80, // Account for fixed header
                            behavior: 'smooth'
                        });
                        
                        // Close mobile menu if open
                        if (mobileMenu.classList.contains('open')) {
                            mobileMenu.classList.remove('open');
                        }
                    }
                });
            });
        });
        
        // Functions
        function renderProducts(category = 'all') {
            const productGrid = document.getElementById('product-grid');
            productGrid.innerHTML = '';
            
            const filteredProducts = category === 'all' 
                ? productsData 
                : productsData.filter(product => product.category === category);
            
            filteredProducts.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'bg-white dark:bg-gray-800 rounded-xl shadow-lg overflow-hidden transition-transform hover:-translate-y-1';
                
                productCard.innerHTML = `
                    <div class="relative product-img-container">
                        <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover">
                        <div class="absolute bottom-0 right-0 m-2">
                            <span class="inline-block bg-accent text-dark px-2 py-1 rounded text-sm font-medium">₹${product.price.toFixed(2)}</span>
                        </div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-lg mb-1 text-gray-800 dark:text-white">${product.name}</h3>
                        <div class="flex justify-between items-center mt-4">
                            <button class="view-product bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 text-gray-800 dark:text-white px-3 py-1 rounded" data-id="${product.id}">
                                View Details
                            </button>
                            <button class="add-to-cart bg-primary hover:bg-primaryDark text-dark px-3 py-1 rounded" data-id="${product.id}">
                                <i class="fas fa-cart-plus"></i>
                            </button>
                        </div>
                    </div>
                `;
                
                productGrid.appendChild(productCard);
                
                // Add event listeners
                const viewBtn = productCard.querySelector('.view-product');
                const addToCartBtn = productCard.querySelector('.add-to-cart');
                
                viewBtn.addEventListener('click', () => {
                    openProductModal(product.id);
                });
                
                addToCartBtn.addEventListener('click', () => {
                    addToCart(product.id, 1);
                });
            });
        }
        
        function renderAdminProductsList() {
            const adminProductsList = document.getElementById('admin-products-list');
            adminProductsList.innerHTML = '';
            
            productsData.forEach(product => {
                const productItem = document.createElement('div');
                productItem.className = 'flex items-center justify-between p-2 border-b border-gray-200 dark:border-gray-700 last:border-0';
                
                productItem.innerHTML = `
                    <div class="flex items-center">
                        <div class="w-8 h-8 bg-gray-200 dark:bg-gray-700 rounded overflow-hidden mr-2">
                            <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover">
                        </div>
                        <div>
                            <p class="font-medium text-sm">${product.name}</p>
                            <p class="text-xs text-gray-500 dark:text-gray-400">₹${product.price.toFixed(2)}</p>
                        </div>
                    </div>
                    <div class="flex space-x-1">
                        <button class="edit-product-btn p-1 text-primary hover:text-primaryDark" data-id="${product.id}">
                            <i class="fas fa-edit"></i>
                        </button>
                        <button class="delete-product-btn p-1 text-secondary hover:text-secondaryDark" data-id="${product.id}">
                            <i class="fas fa-trash"></i>
                        </button>
                    </div>
                `;
                
                adminProductsList.appendChild(productItem);
                
                // Add event listeners
                const editBtn = productItem.querySelector('.edit-product-btn');
                const deleteBtn = productItem.querySelector('.delete-product-btn');
                
                editBtn.addEventListener('click', () => {
                    editProduct(product.id);
                });
                
                deleteBtn.addEventListener('click', () => {
                    if (confirm(`Are you sure you want to delete ${product.name}?`)) {
                        deleteProduct(product.id);
                    }
                });
            });
        }
        
        function renderAdminOrdersList() {
            const adminOrdersList = document.getElementById('admin-orders-list');
            const emptyOrdersMessage = document.getElementById('empty-orders-message');
            
            adminOrdersList.innerHTML = '';
            
            if (orders.length === 0) {
                emptyOrdersMessage.classList.remove('hidden');
                return;
            }
            
            emptyOrdersMessage.classList.add('hidden');
            
            orders.forEach(order => {
                const orderItem = document.createElement('div');
                orderItem.className = 'p-2 border border-gray-200 dark:border-gray-700 rounded mb-2';
                
                const date = new Date(order.date).toLocaleDateString();
                const items = order.items.map(item => `${item.name} (${item.quantity})`).join(', ');
                
                orderItem.innerHTML = `
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="font-medium text-sm">Order #${order.id}</p>
                            <p class="text-xs text-gray-500 dark:text-gray-400">${date}</p>
                        </div>
                        <span class="inline-block bg-accent text-dark px-2 py-1 rounded-full text-xs font-medium">₹${order.total.toFixed(2)}</span>
                    </div>
                    <p class="text-xs mt-1"><span class="font-medium">Customer:</span> ${order.customer.name}</p>
                    <p class="text-xs mt-1"><span class="font-medium">Items:</span> ${items}</p>
                    <div class="flex justify-between items-center mt-2">
                        <span class="inline-block bg-gray-200 dark:bg-gray-700 text-gray-800 dark:text-white px-2 py-1 rounded text-xs">${order.status}</span>
                        <button class="view-order-btn text-primary hover:text-primaryDark text-xs font-medium" data-id="${order.id}">
                            View Details
                        </button>
                    </div>
                `;
                
                adminOrdersList.appendChild(orderItem);
                
                // Add event listener
                const viewBtn = orderItem.querySelector('.view-order-btn');
                
                viewBtn.addEventListener('click', () => {
                    alert(`Order details for #${order.id} - Feature coming soon!`);
                });
            });
        }
        
        function openProductModal(productId) {
            const product = productsData.find(p => p.id === productId);
            if (!product) return;
            
            document.getElementById('modal-product-image').src = product.image;
            document.getElementById('modal-product-name').textContent = product.name;
            document.getElementById('modal-product-price').textContent = `₹${product.price.toFixed(2)}`;
            document.getElementById('modal-product-description').textContent = product.description || 'No description available';
            document.getElementById('modal-product-quantity').value = 1;
            document.getElementById('add-to-cart-modal').dataset.productId = product.id;
            document.getElementById('buy-now-modal').dataset.productId = product.id;
            
            document.getElementById('product-modal').classList.add('show');
        }
        
        function editProduct(productId) {
            const product = productsData.find(p => p.id === productId);
            if (!product) return;
            
            document.getElementById('product-edit-title').textContent = 'Edit Product';
            document.getElementById('product-edit-id').value = product.id;
            document.getElementById('product-edit-name').value = product.name;
            document.getElementById('product-edit-price').value = product.price;
            document.getElementById('product-edit-category').value = product.category;
            document.getElementById('product-edit-description').value = product.description || '';
            document.getElementById('product-edit-image').value = product.image;
            
            // Show image preview
            document.getElementById('preview-image').src = product.image;
            document.getElementById('product-edit-image-preview').classList.remove('hidden');
            
            document.getElementById('product-edit-modal').classList.add('show');
        }
        
        function deleteProduct(productId) {
            const index = productsData.findIndex(p => p.id === productId);
            if (index !== -1) {
                productsData.splice(index, 1);
                renderProducts();
                renderAdminProductsList();
                showToast('Product deleted successfully', 'success');
            }
        }
        
        function addToCart(productId, quantity) {
            const product = productsData.find(p => p.id === productId);
            if (!product) return;
            
            // Check if product already in cart
            const existingItem = cart.find(item => item.id === productId);
            
            if (existingItem) {
                existingItem.quantity += quantity;
            } else {
                cart.push({
                    id: product.id,
                    name: product.name,
                    price: product.price,
                    image: product.image,
                    quantity
                });
            }
            
            updateCartCount();
            showToast('Item added to cart!', 'success');
        }
        
        function updateCartCount() {
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            document.getElementById('cart-count').textContent = totalItems;
        }
        
        function updateCartDisplay() {
            const cartItems = document.getElementById('cart-items');
            const emptyCartMessage = document.getElementById('empty-cart-message');
            const cartTotal = document.getElementById('cart-total');
            
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                emptyCartMessage.classList.remove('hidden');
                cartTotal.querySelector('span:last-child').textContent = '₹0.00';
                return;
            }
            
            emptyCartMessage.classList.add('hidden');
            
            cart.forEach(item => {
                const cartItem = document.createElement('div');
                cartItem.className = 'flex items-center border-b border-gray-200 dark:border-gray-700 pb-3';
                
                cartItem.innerHTML = `
                    <div class="w-16 h-16 bg-gray-200 dark:bg-gray-700 rounded overflow-hidden mr-3">
                        <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover">
                    </div>
                    <div class="flex-1">
                        <h4 class="font-medium text-gray-800 dark:text-white">${item.name}</h4>
                        <div class="flex justify-between items-center mt-1">
                            <div class="flex items-center">
                                <button class="cart-decrease h-6 w-6 bg-gray-200 dark:bg-gray-700 flex items-center justify-center rounded" data-id="${item.id}">
                                    <i class="fas fa-minus text-xs"></i>
                                </button>
                                <span class="mx-2">${item.quantity}</span>
                                <button class="cart-increase h-6 w-6 bg-gray-200 dark:bg-gray-700 flex items-center justify-center rounded" data-id="${item.id}">
                                    <i class="fas fa-plus text-xs"></i>
                                </button>
                            </div>
                            <span class="font-medium">₹${(item.price * item.quantity).toFixed(2)}</span>
                        </div>
                    </div>
                    <button class="cart-remove ml-2 text-gray-500 hover:text-secondary" data-id="${item.id}">
                        <i class="fas fa-trash"></i>
                    </button>
                `;
                
                cartItems.appendChild(cartItem);
                
                // Add event listeners
                const decreaseBtn = cartItem.querySelector('.cart-decrease');
                const increaseBtn = cartItem.querySelector('.cart-increase');
                const removeBtn = cartItem.querySelector('.cart-remove');
                
                decreaseBtn.addEventListener('click', () => {
                    decreaseCartItemQuantity(item.id);
                });
                
                increaseBtn.addEventListener('click', () => {
                    increaseCartItemQuantity(item.id);
                });
                
                removeBtn.addEventListener('click', () => {
                    removeCartItem(item.id);
                });
            });
            
            cartTotal.querySelector('span:last-child').textContent = `₹${calculateTotal().toFixed(2)}`;
        }
        
        function updateCheckoutDisplay() {
            const checkoutItems = document.getElementById('checkout-items');
            const checkoutTotal = document.getElementById('checkout-total');
            
            checkoutItems.innerHTML = '';
            
            cart.forEach(item => {
                const checkoutItem = document.createElement('div');
                checkoutItem.className = 'flex justify-between items-center mb-2';
                
                checkoutItem.innerHTML = `
                    <div>
                        <p class="font-medium">${item.name}</p>
                        <p class="text-sm text-gray-500 dark:text-gray-400">₹${item.price.toFixed(2)} x ${item.quantity}</p>
                    </div>
                    <span class="font-medium">₹${(item.price * item.quantity).toFixed(2)}</span>
                `;
                
                checkoutItems.appendChild(checkoutItem);
            });
            
            checkoutTotal.textContent = `₹${calculateTotal().toFixed(2)}`;
        }
        
        function decreaseCartItemQuantity(productId) {
            const index = cart.findIndex(item => item.id === productId);
            if (index !== -1) {
                if (cart[index].quantity > 1) {
                    cart[index].quantity--;
                } else {
                    cart.splice(index, 1);
                }
                
                updateCartCount();
                updateCartDisplay();
            }
        }
        
        function increaseCartItemQuantity(productId) {
            const index = cart.findIndex(item => item.id === productId);
            if (index !== -1) {
                cart[index].quantity++;
                updateCartCount();
                updateCartDisplay();
            }
        }
        
        function removeCartItem(productId) {
            const index = cart.findIndex(item => item.id === productId);
            if (index !== -1) {
                cart.splice(index, 1);
                updateCartCount();
                updateCartDisplay();
            }
        }
        
        function calculateTotal() {
            return cart.reduce((total, item) => total + (item.price * item.quantity), 0);
        }
        
        function showToast(message, type = 'success') {
            const toast = document.getElementById('toast');
            const toastIcon = document.getElementById('toast-icon');
            const toastMessage = document.getElementById('toast-message');
            
            // Set toast content
            toastMessage.textContent = message;
            
            // Set toast style based on type
            if (type === 'success') {
                toast.className = 'toast bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg';
                toastIcon.className = 'fas fa-check-circle mr-3 text-xl';
            } else if (type === 'error') {
                toast.className = 'toast bg-red-500 text-white px-6 py-3 rounded-lg shadow-lg';
                toastIcon.className = 'fas fa-exclamation-circle mr-3 text-xl';
            } else if (type === 'warning') {
                toast.className = 'toast bg-yellow-500 text-white px-6 py-3 rounded-lg shadow-lg';
                toastIcon.className = 'fas fa-exclamation-triangle mr-3 text-xl';
            }
            
            // Show toast
            toast.classList.add('show');
            
            // Hide toast after 3 seconds
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }
        
        function adjustColor(hex, amount) {
            // Convert hex to RGB
            let r = parseInt(hex.substring(1, 3), 16);
            let g = parseInt(hex.substring(3, 5), 16);
            let b = parseInt(hex.substring(5, 7), 16);
            
            // Adjust color
            r = Math.max(0, Math.min(255, r + amount));
            g = Math.max(0, Math.min(255, g + amount));
            b = Math.max(0, Math.min(255, b + amount));
            
            // Convert back to hex
            return `#${r.toString(16).padStart(2, '0')}${g.toString(16).padStart(2, '0')}${b.toString(16).padStart(2, '0')}`;
        }
    </script>
</body>
</html>
