[Upl<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TEIKI ESPACES - Coworking à Pirae, Tahiti</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, rgba(22, 160, 133, 0.9) 0%, rgba(39, 174, 96, 0.9) 100%);
        }
        
        .btn-primary {
            background-color: #16a085;
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            background-color: #1abc9c;
            transform: translateY(-2px);
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .testimonial-card {
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover {
            transform: scale(1.02);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: #16a085;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .active-nav:after {
            width: 100%;
        }

        .cgv-container {
            max-height: 500px;
            overflow-y: auto;
            padding-right: 15px;
        }

        .cgv-container::-webkit-scrollbar {
            width: 8px;
        }

        .cgv-container::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }

        .cgv-container::-webkit-scrollbar-thumb {
            background: #16a085;
            border-radius: 10px;
        }

        .cgv-container::-webkit-scrollbar-thumb:hover {
            background: #1abc9c;
        }

        /* Styles pour le planning de réservation */
        .booking-calendar {
            background-color: #f8fafc;
            border-radius: 0.5rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }

        .time-slot {
            transition: all 0.2s ease;
        }

        .time-slot:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .time-slot.booked {
            background-color: #fecaca;
            cursor: not-allowed;
        }

        .time-slot.available {
            background-color: #d1fae5;
            cursor: pointer;
        }

        .time-slot.selected {
            background-color: #6ee7b7;
            transform: scale(1.05);
        }

        .room-option {
            transition: all 0.2s ease;
        }

        .room-option:hover {
            transform: translateY(-2px);
        }

        .room-option.selected {
            border-color: #10b981;
            box-shadow: 0 0 0 2px #6ee7b7;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Navigation -->
    <nav class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-6 py-3">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <div class="flex items-center">
                        <i class="fas fa-leaf text-2xl text-green-600 mr-2"></i>
                        <span class="text-xl font-bold text-gray-800">TEIKI <span class="text-green-600">ESPACES</span></span>
                    </div>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#accueil" class="nav-link active-nav text-gray-800 font-medium">Accueil</a>
                    <a href="#espaces" class="nav-link text-gray-800 font-medium">Nos espaces</a>
                    <a href="#services" class="nav-link text-gray-800 font-medium">Services</a>
                    <a href="#tarifs" class="nav-link text-gray-800 font-medium">Tarifs</a>
                    <a href="#reservation" class="nav-link text-gray-800 font-medium">Réservation</a>
                    <a href="#cgv" class="nav-link text-gray-800 font-medium">CGV</a>
                    <a href="#contact" class="nav-link text-gray-800 font-medium">Contact</a>
                </div>
                <div class="md:hidden">
                    <button class="text-gray-800 focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="accueil" class="hero-gradient text-white py-20">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-5xl font-bold mb-6">Votre espace de coworking à Tahiti</h1>
                    <p class="text-xl mb-8">TEIKI ESPACES vous offre un environnement de travail inspirant et connecté au cœur de Pirae, avec des espaces intérieurs et extérieurs.</p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <a href="#contact" class="btn-primary text-white font-bold py-3 px-6 rounded-lg text-center">Réserver une visite</a>
                        <a href="#tarifs" class="bg-white text-green-600 font-bold py-3 px-6 rounded-lg text-center">Voir nos tarifs</a>
                    </div>
                </div>
                <div class="md:w-1/2">
                    <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Espace de coworking" class="rounded-lg shadow-xl">
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Pourquoi choisir TEIKI ESPACES ?</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="feature-card bg-gray-50 p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-green-500 text-4xl mb-4">
                        <i class="fas fa-wifi"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Connexion haut débit</h3>
                    <p class="text-gray-600">Accès à une connexion internet fibre optique ultra rapide et sécurisée pour un travail sans interruption.</p>
                </div>
                <div class="feature-card bg-gray-50 p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-green-500 text-4xl mb-4">
                        <i class="fas fa-umbrella-beach"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Espaces extérieurs</h3>
                    <p class="text-gray-600">Profitez de nos espaces de travail en plein air avec vue sur le jardin tropical.</p>
                </div>
                <div class="feature-card bg-gray-50 p-8 rounded-lg shadow-md transition duration-300">
                    <div class="text-green-500 text-4xl mb-4">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3 class="text-xl font-bold text-gray-800 mb-3">Communauté dynamique</h3>
                    <p class="text-gray-600">Rejoignez une communauté de professionnels et entrepreneurs pour échanger et collaborer.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Spaces Section -->
    <section id="espaces" class="py-16 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Nos espaces de travail</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-white rounded-lg overflow-hidden shadow-md">
                    <img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80" alt="Salle de réunion" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Salle de réunion</h3>
                        <p class="text-gray-600 mb-4">Espace climatisé et équipé pour vos réunions d'affaires, présentations et formations.</p>
                        <div class="flex items-center text-green-500">
                            <i class="fas fa-user-friends mr-2"></i>
                            <span>Jusqu'à 8 personnes</span>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md">
                    <img src="https://images.unsplash.com/photo-1517502884422-41eaead166d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Places extérieures" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Places extérieures</h3>
                        <p class="text-gray-600 mb-4">Postes de travail individuels ou duo en plein air, ombragés et équipés de prises électriques.</p>
                        <div class="flex items-center text-green-500">
                            <i class="fas fa-user mr-2"></i>
                            <span>1 à 2 personnes par poste</span>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg overflow-hidden shadow-md">
                    <img src="https://images.unsplash.com/photo-1565538810643-b5bdb714032a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Salon extérieur" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Salon extérieur</h3>
                        <p class="text-gray-600 mb-4">Espace convivial avec mobilier confortable pour travailler ou se détendre dans un cadre naturel.</p>
                        <div class="flex items-center text-green-500">
                            <i class="fas fa-couch mr-2"></i>
                            <span>Jusqu'à 6 personnes</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Nos services inclus</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-print text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Impression et numérisation</h3>
                        <p class="text-gray-600">Accès à des imprimantes professionnelles et service de numérisation de documents.</p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-phone-alt text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Standard téléphonique</h3>
                        <p class="text-gray-600">Service de réception d'appels et prise de messages pour votre entreprise.</p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-parking text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Parking sécurisé</h3>
                        <p class="text-gray-600">Place de parking privée et sécurisée pour tous nos membres.</p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-lock text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Accès 24/7</h3>
                        <p class="text-gray-600">Accès à votre espace de travail 24 heures sur 24, 7 jours sur 7 avec badge sécurisé.</p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-concierge-bell text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Service de conciergerie</h3>
                        <p class="text-gray-600">Nous prenons en charge vos livraisons et colis pendant votre absence.</p>
                    </div>
                </div>
                <div class="flex items-start">
                    <div class="bg-green-100 p-3 rounded-full mr-4">
                        <i class="fas fa-fan text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Ventilateurs extérieurs</h3>
                        <p class="text-gray-600">Nos espaces extérieurs sont équipés de ventilateurs pour plus de confort.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="tarifs" class="py-16 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Nos formules d'abonnement</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white rounded-lg shadow-md overflow-hidden">
                    <div class="bg-gray-100 p-6 text-center">
                        <h3 class="text-xl font-bold text-gray-800">Flex</h3>
                        <div class="my-4">
                            <span class="text-4xl font-bold text-green-600">12 900 XPF</span>
                            <span class="text-gray-600">/jour</span>
                        </div>
                        <p class="text-gray-600">Accès occasionnel à l'espace</p>
                    </div>
                    <div class="p-6">
                        <ul class="space-y-3">
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Accès 8h-18h</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Place extérieure</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>WiFi haut débit</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Café & thé illimités</span>
                            </li>
                            <li class="flex items-center text-gray-600 opacity-50">
                                <i class="fas fa-times text-red-400 mr-2"></i>
                                <span>Accès 24/7</span>
                            </li>
                        </ul>
                        <button class="w-full mt-6 bg-gray-200 text-gray-800 font-bold py-2 px-4 rounded hover:bg-gray-300 transition">Choisir cette formule</button>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-lg overflow-hidden transform scale-105">
                    <div class="bg-green-500 p-6 text-center text-white">
                        <h3 class="text-xl font-bold">Pro</h3>
                        <div class="my-4">
                            <span class="text-4xl font-bold">89 900 XPF</span>
                            <span>/mois</span>
                        </div>
                        <p>Formule la plus populaire</p>
                    </div>
                    <div class="p-6">
                        <ul class="space-y-3">
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Accès 24/7</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Place attitrée extérieure</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>WiFi haut débit</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Café & thé illimités</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>5h de salle de réunion/mois</span>
                            </li>
                        </ul>
                        <button class="w-full mt-6 bg-green-500 text-white font-bold py-2 px-4 rounded hover:bg-green-600 transition">Choisir cette formule</button>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-md overflow-hidden">
                    <div class="bg-gray-100 p-6 text-center">
                        <h3 class="text-xl font-bold text-gray-800">Entreprise</h3>
                        <div class="my-4">
                            <span class="text-4xl font-bold text-green-600">249 900 XPF</span>
                            <span class="text-gray-600">/mois</span>
                        </div>
                        <p class="text-gray-600">Solution complète pour équipes</p>
                    </div>
                    <div class="p-6">
                        <ul class="space-y-3">
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Jusqu'à 4 postes</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Places extérieures attitrées</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>WiFi haut débit dédié</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>15h de salle de réunion/mois</span>
                            </li>
                            <li class="flex items-center text-gray-600">
                                <i class="fas fa-check text-green-500 mr-2"></i>
                                <span>Service de réception</span>
                            </li>
                        </ul>
                        <button class="w-full mt-6 bg-gray-200 text-gray-800 font-bold py-2 px-4 rounded hover:bg-gray-300 transition">Choisir cette formule</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reservation Section -->
    <section id="reservation" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Réservez votre espace</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            
            <div class="max-w-4xl mx-auto bg-white rounded-xl shadow-md overflow-hidden booking-calendar">
                <div class="md:flex">
                    <div class="p-8 md:w-1/2">
                        <h3 class="text-xl font-bold text-gray-800 mb-6">Choisissez votre espace</h3>
                        
                        <div class="space-y-4 mb-8">
                            <div class="room-option p-4 border-2 border-gray-200 rounded-lg cursor-pointer" onclick="selectRoom(this, 'salle-reunion')">
                                <div class="flex items-center">
                                    <div class="bg-green-100 p-2 rounded-full mr-4">
                                        <i class="fas fa-chalkboard text-green-600"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-gray-800">Salle de réunion</h4>
                                        <p class="text-gray-600 text-sm">Pour vos réunions et présentations (8 pers. max)</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="room-option p-4 border-2 border-gray-200 rounded-lg cursor-pointer" onclick="selectRoom(this, 'place-exterieure')">
                                <div class="flex items-center">
                                    <div class="bg-green-100 p-2 rounded-full mr-4">
                                        <i class="fas fa-umbrella-beach text-green-600"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-gray-800">Place extérieure</h4>
                                        <p class="text-gray-600 text-sm">Poste de travail en plein air (1-2 personnes)</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="room-option p-4 border-2 border-gray-200 rounded-lg cursor-pointer" onclick="selectRoom(this, 'salon-exterieur')">
                                <div class="flex items-center">
                                    <div class="bg-green-100 p-2 rounded-full mr-4">
                                        <i class="fas fa-couch text-green-600"></i>
                                    </div>
                                    <div>
                                        <h4 class="font-bold text-gray-800">Salon extérieur</h4>
                                        <p class="text-gray-600 text-sm">Espace détente pour travailler au calme (6 pers. max)</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-gray-700 font-bold mb-2" for="reservation-date">Date de réservation</label>
                            <input type="date" id="reservation-date" class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" min="">
                        </div>
                        
                        <div class="mb-6">
                            <label class="block text-gray-700 font-bold mb-2">Nombre de personnes</label>
                            <select class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="people-select">
                                <option>1 personne</option>
                                <option>2 personnes</option>
                                <option>3-4 personnes</option>
                                <option>5-6 personnes</option>
                                <option>7-8 personnes</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="p-8 bg-gray-50 md:w-1/2">
                        <h3 class="text-xl font-bold text-gray-800 mb-6">Disponibilités</h3>
                        
                        <div class="grid grid-cols-3 gap-2 mb-6">
                            <div class="time-slot booked p-3 rounded text-center text-sm font-medium">8h-10h</div>
                            <div class="time-slot available p-3 rounded text-center text-sm font-medium" onclick="selectTimeSlot(this)">10h-12h</div>
                            <div class="time-slot available p-3 rounded text-center text-sm font-medium" onclick="selectTimeSlot(this)">12h-14h</div>
                            <div class="time-slot available p-3 rounded text-center text-sm font-medium" onclick="selectTimeSlot(this)">14h-16h</div>
                            <div class="time-slot booked p-3 rounded text-center text-sm font-medium">16h-18h</div>
                            <div class="time-slot available p-3 rounded text-center text-sm font-medium" onclick="selectTimeSlot(this)">18h-20h</div>
                        </div>
                        
                        <div class="bg-white p-4 rounded-lg shadow-sm mb-6">
                            <h4 class="font-bold text-gray-800 mb-2">Récapitulatif</h4>
                            <div class="flex justify-between text-sm text-gray-600 mb-1">
                                <span>Espace:</span>
                                <span id="selected-room">Non sélectionné</span>
                            </div>
                            <div class="flex justify-between text-sm text-gray-600 mb-1">
                                <span>Date:</span>
                                <span id="selected-date">--/--/----</span>
                            </div>
                            <div class="flex justify-between text-sm text-gray-600 mb-1">
                                <span>Horaire:</span>
                                <span id="selected-time">--:-- - --:--</span>
                            </div>
                            <div class="flex justify-between text-sm text-gray-600 mb-1">
                                <span>Personnes:</span>
                                <span id="selected-people">--</span>
                            </div>
                            <div class="border-t border-gray-200 my-2"></div>
                            <div class="flex justify-between font-bold text-gray-800">
                                <span>Total:</span>
                                <span id="selected-price">0 XPF</span>
                            </div>
                        </div>
                        
                        <button id="confirm-booking" class="w-full bg-green-500 text-white font-bold py-3 px-4 rounded hover:bg-green-600 transition opacity-50 cursor-not-allowed" disabled>
                            Confirmer la réservation
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CGV Section -->
    <section id="cgv" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Conditions Générales de Vente</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="bg-gray-50 p-8 rounded-lg shadow-md cgv-container">
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 1 - Objet</h3>
                <p class="text-gray-600 mb-6">Les présentes conditions générales de vente (CGV) régissent les relations contractuelles entre TEIKI ESPACES, société de coworking située à Pirae, Tahiti, et ses clients pour la location d'espaces de travail et services associés.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 2 - Tarifs et modalités de paiement</h3>
                <p class="text-gray-600 mb-4">2.1 Les tarifs des abonnements et services sont indiqués en francs pacifiques (XPF) et sont hors taxes conformément à la réglementation en vigueur en Polynésie française.</p>
                <p class="text-gray-600 mb-4">2.2 Le paiement s'effectue par virement bancaire, carte bancaire ou chèque. Pour les abonnements mensuels, le prélèvement est effectué le premier jour de chaque mois.</p>
                <p class="text-gray-600 mb-6">2.3 Tout retard de paiement entraînera l'application de pénalités de retard au taux de 1,5% par mois de retard.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 3 - Engagements et résiliations</h3>
                <p class="text-gray-600 mb-4">3.1 Les abonnements mensuels sont souscrits pour une durée minimale de 3 mois. Passé ce délai, ils sont reconduits tacitement par périodes d'un mois.</p>
                <p class="text-gray-600 mb-4">3.2 La résiliation doit être notifiée par écrit au moins 15 jours avant la fin de la période en cours.</p>
                <p class="text-gray-600 mb-6">3.3 En cas de résiliation anticipée d'un engagement annuel, des frais équivalents à 50% du montant des mois restants seront dus.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 4 - Accès et utilisation des espaces</h3>
                <p class="text-gray-600 mb-4">4.1 L'accès aux espaces est soumis à la présentation d'un badge nominatif remis par TEIKI ESPACES.</p>
                <p class="text-gray-600 mb-4">4.2 Les espaces extérieurs sont accessibles selon les conditions météorologiques. TEIKI ESPACES se réserve le droit de fermer temporairement ces espaces pour raisons de sécurité.</p>
                <p class="text-gray-600 mb-6">4.3 La salle de réunion est réservable via notre plateforme en ligne, avec un délai minimum de 2 heures pour toute annulation sans frais.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 5 - Responsabilités</h3>
                <p class="text-gray-600 mb-4">5.1 TEIKI ESPACES décline toute responsabilité en cas de vol ou détérioration des effets personnels laissés dans les espaces communs ou extérieurs.</p>
                <p class="text-gray-600 mb-4">5.2 Le client est responsable du matériel qu'il utilise et des dommages qu'il pourrait causer aux installations.</p>
                <p class="text-gray-600 mb-6">5.3 En cas de pluie, les espaces extérieurs peuvent devenir inaccessibles sans remboursement possible.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 6 - Confidentialité et données personnelles</h3>
                <p class="text-gray-600 mb-6">Les données personnelles collectées sont traitées conformément à notre politique de confidentialité disponible sur demande. Elles ne seront en aucun cas transmises à des tiers sans consentement explicite.</p>
                
                <h3 class="text-xl font-bold text-gray-800 mb-4">Article 7 - Litiges et droit applicable</h3>
                <p class="text-gray-600 mb-6">En cas de litige, les parties s'efforceront de trouver une solution amiable. À défaut, les tribunaux compétents seront ceux de Papeete, Polynésie française, et le droit applicable sera le droit français.</p>
                
                <p class="text-gray-600 text-sm">Dernière mise à jour : 01/01/2023</p>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Ce que disent nos membres</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="testimonial-card bg-white p-8 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-yellow-400 mr-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-6">"Travailler dans le salon extérieur avec la brise marine est une expérience unique. La connexion wifi est excellente même en plein air."</p>
                    <div class="flex items-center">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah T." class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Sarah T.</h4>
                            <p class="text-gray-500">Graphiste freelance</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card bg-white p-8 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-yellow-400 mr-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-6">"La salle de réunion est parfaitement équipée pour nos brainstormings d'équipe. Et pouvoir ensuite travailler en extérieur est un vrai plus."</p>
                    <div class="flex items-center">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Marc L." class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Marc L.</h4>
                            <p class="text-gray-500">Co-fondateur de TahitiTech</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card bg-white p-8 rounded-lg shadow-md">
                    <div class="flex items-center mb-4">
                        <div class="text-yellow-400 mr-2">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                        </div>
                    </div>
                    <p class="text-gray-600 mb-6">"J'adore mon poste de travail extérieur ombragé. Les ventilateurs rendent le travail très agréable même en milieu de journée."</p>
                    <div class="flex items-center">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Hinano V." class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold text-gray-800">Hinano V.</h4>
                            <p class="text-gray-500">Développeuse web</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Contactez-nous</h2>
                <div class="w-20 h-1 bg-green-500 mx-auto"></div>
            </div>
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-10">
                    <h3 class="text-xl font-bold text-gray-800 mb-4">Nos coordonnées</h3>
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="bg-green-100 p-2 rounded-full mr-4">
                                <i class="fas fa-map-marker-alt text-green-600"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-800">Adresse</h4>
                                <p class="text-gray-600">123 Avenue du Prince Hinoi, Pirae 98716, Tahiti</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="bg-green-100 p-2 rounded-full mr-4">
                                <i class="fas fa-phone-alt text-green-600"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-800">Téléphone</h4>
                                <p class="text-gray-600">+689 40 123 456</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="bg-green-100 p-2 rounded-full mr-4">
                                <i class="fas fa-envelope text-green-600"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-800">Email</h4>
                                <p class="text-gray-600">contact@teikiespaces.pf</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="bg-green-100 p-2 rounded-full mr-4">
                                <i class="fas fa-clock text-green-600"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-gray-800">Horaires</h4>
                                <p class="text-gray-600">Lundi-Vendredi: 7h-19h<br>Samedi: 8h-12h<br>Dimanche: Fermé</p>
                            </div>
                        </div>
                    </div>
                    <div class="mt-8">
                        <h3 class="text-xl font-bold text-gray-800 mb-4">Suivez-nous</h3>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-green-100 text-green-600 p-3 rounded-full hover:bg-green-200 transition">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                            <a href="#" class="bg-green-100 text-green-600 p-3 rounded-full hover:bg-green-200 transition">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="#" class="bg-green-100 text-green-600 p-3 rounded-full hover:bg-green-200 transition">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2">
                    <form class="bg-gray-50 p-8 rounded-lg shadow-md">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-bold mb-2" for="name">Nom complet</label>
                            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="name" type="text" placeholder="Votre nom">
                        </div>
                        <div class="mb-4">
                            <label class="block text-gray-700 font-bold mb-2" for="email">Email</label>
                            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="email" type="email" placeholder="Votre email">
                        </div>
                        <div class="mb-4">
                            <label class="block text-gray-700 font-bold mb-2" for="phone">Téléphone</label>
                            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="phone" type="tel" placeholder="Votre numéro">
                        </div>
                        <div class="mb-4">
                            <label class="block text-gray-700 font-bold mb-2" for="subject">Sujet</label>
                            <select class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="subject">
                                <option>Demande d'information</option>
                                <option>Visite des locaux</option>
                                <option>Demande de devis</option>
                                <option>Autre</option>
                            </select>
                        </div>
                        <div class="mb-6">
                            <label class="block text-gray-700 font-bold mb-2" for="message">Message</label>
                            <textarea class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-green-500" id="message" rows="4" placeholder="Votre message"></textarea>
                        </div>
                        <button class="w-full bg-green-500 text-white font-bold py-2 px-4 rounded hover:bg-green-600 transition">Envoyer le message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <div class="h-96 w-full">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3825.011125618178!2d-149.5587889241711!3d-17.53599978341589!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x769a3e1b1d1e0aab%3A0x5a8c0c1b5e5b5e5b!2sPirae%2C%20French%20Polynesia!5e0!3m2!1sen!2sus!4v1689876543210!5m2!1sen!2sus" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-6">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center mb-4">
                        <i class="fas fa-leaf text-2xl text-green-400 mr-2"></i>
                        <span class="text-xl font-bold">TEIKI <span class="text-green-400">ESPACES</span></span>
                    </div>
                    <p class="text-gray-400">Votre espace de coworking professionnel au cœur de Tahiti.</p>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Liens rapides</h3>
                    <ul class="space-y-2">
                        <li><a href="#accueil" class="text-gray-400 hover:text-white transition">Accueil</a></li>
                        <li><a href="#espaces" class="text-gray-400 hover:text-white transition">Nos espaces</a></li>
                        <li><a href="#services" class="text-gray-400 hover:text-white transition">Services</a></li>
                        <li><a href="#tarifs" class="text-gray-400 hover:text-white transition">Tarifs</a></li>
                        <li><a href="#reservation" class="text-gray-400 hover:text-white transition">Réservation</a></li>
                        <li><a href="#cgv" class="text-gray-400 hover:text-white transition">CGV</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Services</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Salle de réunion</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Places extérieures</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Salon extérieur</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Événements</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition">Services aux entreprises</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-bold mb-4">Newsletter</h3>
                    <p class="text-gray-400 mb-4">Abonnez-vous pour recevoir nos actualités et offres spéciales.</p>
                    <div class="flex">
                        <input type="email" placeholder="Votre email" class="px-4 py-2 w-full rounded-l focus:outline-none text-gray-800">
                        <button class="bg-green-500 text-white px-4 py-2 rounded-r hover:bg-green-600 transition">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </div>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">© 2023 TEIKI ESPACES. Tous droits réservés.</p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-facebook-f"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-instagram"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-linkedin-in"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-twitter"></i>
                    </a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.md\\:hidden button').addEventListener('click', function() {
            // This would toggle a mobile menu - implementation depends on your needs
            alert('Menu mobile à implémenter');
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Update active nav link
                document.querySelectorAll('.nav-link').forEach(link => {
                    link.classList.remove('active-nav');
                });
                this.classList.add('active-nav');
            });
        });

        // Simple form validation
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            
            if(name && email) {
                alert('Merci pour votre message! Nous vous contacterons bientôt.');
                this.reset();
            } else {
                alert('Veuillez remplir tous les champs obligatoires.');
            }
        });

        // Set minimum date for reservation (today)
        document.addEventListener('DOMContentLoaded', function() {
            const today = new Date().toISOString().split('T')[0];
            document.getElementById('reservation-date').min = today;
        });

        // Room selection functionality
        function selectRoom(element, roomType) {
            // Remove selected class from all room options
            document.querySelectorAll('.room-option').forEach(room => {
                room.classList.remove('selected');
                room.classList.remove('border-green-500');
                room.classList.add('border-gray-200');
            });
            
            // Add selected class to clicked room
            element.classList.add('selected');
            element.classList.remove('border-gray-200');
            element.classList.add('border-green-500');
            
            // Update summary
            document.getElementById('selected-room').textContent = 
                roomType === 'salle-reunion' ? 'Salle de réunion' :
                roomType === 'place-exterieure' ? 'Place extérieure' : 'Salon extérieur';
            
            // Update price in summary
            updatePrice();
            checkReservationComplete();
        }

        // Time slot selection functionality
        function selectTimeSlot(element) {
            // Don't allow selection if already booked
            if (element.classList.contains('booked')) return;
            
            // Remove selected class from all time slots
            document.querySelectorAll('.time-slot').forEach(slot => {
                slot.classList.remove('selected');
            });
            
            // Add selected class to clicked time slot
            element.classList.add('selected');
            
            // Update summary
            document.getElementById('selected-time').textContent = element.textContent;
            
            // Update price in summary
            updatePrice();
            checkReservationComplete();
        }

        // Update price based on selection
        function updatePrice() {
            const roomElement = document.querySelector('.room-option.selected');
            const timeElement = document.querySelector('.time-slot.selected');
            
            if (roomElement && timeElement) {
                const roomType = 
                    roomElement.textContent.includes('réunion') ? 'reunion' :
                    roomElement.textContent.includes('extérieure') ? 'exterieur' : 'salon';
                
                let price = 0;
                
                switch(roomType) {
                    case 'reunion':
                        price = 24900;
                        break;
                    case 'exterieur':
                        price = 12900;
                        break;
                    case 'salon':
                        price = 15900;
                        break;
                }
                
                document.getElementById('selected-price').textContent = price.toLocaleString() + ' XPF';
            }
        }

        // Check if reservation is complete to enable confirm button
        function checkReservationComplete() {
            const roomSelected = document.querySelector('.room-option.selected');
            const timeSelected = document.querySelector('.time-slot.selected');
            const dateSelected = document.getElementById('reservation-date').value;
            const peopleSelected = document.getElementById('people-select').value;
            
            if (roomSelected && timeSelected && dateSelected && peopleSelected) {
                document.getElementById('confirm-booking').disabled = false;
                document.getElementById('confirm-booking').classList.remove('opacity-50', 'cursor-not-allowed');
                
                // Update summary with date and people
                document.getElementById('selected-date').textContent = formatDate(dateSelected);
                document.getElementById('selected-people').textContent = peopleSelected;
            } else {
                document.getElementById('confirm-booking').disabled = true;
                document.getElementById('confirm-booking').classList.add('opacity-50', 'cursor-not-allowed');
            }
        }

        // Format date for display
        function formatDate(dateString) {
            const options = { day: '2-digit', month: '2-digit', year: 'numeric' };
            return new Date(dateString).toLocaleDateString('fr-FR', options);
        }

        // Listen for date changes
        document.getElementById('reservation-date').addEventListener('change', function() {
            checkReservationComplete();
        });

        // Listen for people selection changes
        document.getElementById('people-select').addEventListener('change', function() {
            checkReservationComplete();
        });

        // Confirm booking button
        document.getElementById('confirm-booking').addEventListener('click', function() {
            const room = document.getElementById('selected-room').textContent;
            const date = document.getElementById('selected-date').textContent;
            const time = document.getElementById('selected-time').textContent;
            const people = document.getElementById('selected-people').textContent;
            const price = document.getElementById('selected-price').textContent;
            
            alert(`Réservation confirmée!\n\nEspace: ${room}\nDate: ${date}\nHoraire: ${time}\nPersonnes: ${people}\nTotal: ${price}\n\nMerci pour votre réservation!`);
        });
    </script>
</body>
</html>oading Teiki-espaces.html…]()
