<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pizzaria Sabor Italiano - As melhores pizzas da cidade</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1513104890138-7c749659a591?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            min-height: 90vh;
        }
        
        .pizza-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .pizza-card {
            transition: all 0.3s ease;
        }
        
        .ingredient-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background-color: #f8fafc;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }
        
        .testimonial-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
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
            background-color: #ef4444;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .menu-tab.active {
            background-color: #ef4444;
            color: white;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header/Navigation -->
    <header class="fixed w-full bg-white shadow-md z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <i class="fas fa-pizza-slice text-3xl text-red-500 mr-2"></i>
                <span class="text-2xl font-bold text-gray-800">Sabor Italiano</span>
            </div>
            
            <nav class="hidden md:flex space-x-8">
                <a href="#home" class="nav-link text-gray-700 hover:text-red-500 font-medium">Início</a>
                <a href="#menu" class="nav-link text-gray-700 hover:text-red-500 font-medium">Cardápio</a>
                <a href="#about" class="nav-link text-gray-700 hover:text-red-500 font-medium">Sobre</a>
                <a href="#testimonials" class="nav-link text-gray-700 hover:text-red-500 font-medium">Avaliações</a>
                <a href="#contact" class="nav-link text-gray-700 hover:text-red-500 font-medium">Contato</a>
            </nav>
            
            <div class="flex items-center space-x-4">
                <a href="#" class="text-gray-700 hover:text-red-500">
                    <i class="fas fa-shopping-cart text-xl"></i>
                </a>
                <button class="md:hidden text-gray-700" id="mobile-menu-button">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div class="md:hidden hidden bg-white w-full py-4 px-4 shadow-lg" id="mobile-menu">
            <div class="flex flex-col space-y-4">
                <a href="#home" class="text-gray-700 hover:text-red-500 font-medium">Início</a>
                <a href="#menu" class="text-gray-700 hover:text-red-500 font-medium">Cardápio</a>
                <a href="#about" class="text-gray-700 hover:text-red-500 font-medium">Sobre</a>
                <a href="#testimonials" class="text-gray-700 hover:text-red-500 font-medium">Avaliações</a>
                <a href="#contact" class="text-gray-700 hover:text-red-500 font-medium">Contato</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero flex items-center justify-center text-white pt-20" id="home">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-4xl md:text-6xl font-bold mb-6">As Melhores Pizzas da Cidade</h1>
            <p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto">Feitas com ingredientes frescos e receita tradicional italiana</p>
            <div class="flex flex-col sm:flex-row justify-center gap-4">
                <a href="#menu" class="bg-red-500 hover:bg-red-600 text-white font-bold py-3 px-8 rounded-full transition duration-300">Ver Cardápio</a>
                <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="bg-transparent hover:bg-white hover:text-gray-900 border-2 border-white text-white font-bold py-3 px-8 rounded-full transition duration-300">Faça seu Pedido</a>
            </div>
        </div>
    </section>

    <!-- Special Offers -->
    <section class="py-12 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Promoções Especiais</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Offer 1 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1381&q=80" alt="Pizza Margherita" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-red-500 text-white px-3 py-1 rounded-full font-bold">-20%</div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Margherita Especial</h3>
                        <p class="text-gray-600 mb-4">Molho de tomate, mussarela fresca, manjericão e azeite de oliva extra virgem.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-gray-500 line-through">R$ 59,90</span>
                            <span class="text-2xl font-bold text-red-500">R$ 47,90</span>
                        </div>
                        <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="mt-4 w-full block bg-red-500 hover:bg-red-600 text-white text-center font-bold py-2 rounded-lg transition duration-300">Pedir Agora</a>
                    </div>
                </div>
                
                <!-- Offer 2 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1541745537411-b8046dc6d66c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1376&q=80" alt="Pizza Pepperoni" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-red-500 text-white px-3 py-1 rounded-full font-bold">Combo</div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Combo Família</h3>
                        <p class="text-gray-600 mb-4">2 pizzas grandes + 1 refrigerante 2L + 1 sobremesa. Escolha seus sabores.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-gray-500 line-through">R$ 129,90</span>
                            <span class="text-2xl font-bold text-red-500">R$ 99,90</span>
                        </div>
                        <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="mt-4 w-full block bg-red-500 hover:bg-red-600 text-white text-center font-bold py-2 rounded-lg transition duration-300">Pedir Agora</a>
                    </div>
                </div>
                
                <!-- Offer 3 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1450&q=80" alt="Pizza Vegetariana" class="w-full h-48 object-cover">
                        <div class="absolute top-4 right-4 bg-red-500 text-white px-3 py-1 rounded-full font-bold">Novidade</div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Vegetariana Premium</h3>
                        <p class="text-gray-600 mb-4">Berinjela, abobrinha, pimentão, champignon, tomate seco e queijo de cabra.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-gray-500 line-through">R$ 64,90</span>
                            <span class="text-2xl font-bold text-red-500">R$ 54,90</span>
                        </div>
                        <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="mt-4 w-full block bg-red-500 hover:bg-red-600 text-white text-center font-bold py-2 rounded-lg transition duration-300">Pedir Agora</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section class="py-16 bg-white" id="menu">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-4 text-gray-800">Nosso Cardápio</h2>
            <p class="text-center text-gray-600 mb-12 max-w-2xl mx-auto">Temos mais de 50 sabores de pizza para você escolher. Todas feitas com massa artesanal e ingredientes selecionados.</p>
            
            <!-- Menu Tabs -->
            <div class="flex flex-wrap justify-center mb-8 gap-2">
                <button class="menu-tab px-4 py-2 rounded-full font-medium bg-gray-100 hover:bg-red-500 hover:text-white transition duration-300 active" data-category="all">Todas</button>
                <button class="menu-tab px-4 py-2 rounded-full font-medium bg-gray-100 hover:bg-red-500 hover:text-white transition duration-300" data-category="traditional">Tradicionais</button>
                <button class="menu-tab px-4 py-2 rounded-full font-medium bg-gray-100 hover:bg-red-500 hover:text-white transition duration-300" data-category="special">Especiais</button>
                <button class="menu-tab px-4 py-2 rounded-full font-medium bg-gray-100 hover:bg-red-500 hover:text-white transition duration-300" data-category="vegetarian">Vegetarianas</button>
                <button class="menu-tab px-4 py-2 rounded-full font-medium bg-gray-100 hover:bg-red-500 hover:text-white transition duration-300" data-category="dessert">Sobremesas</button>
            </div>
            
            <!-- Menu Items -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="menu-items">
                <!-- Pizza items will be loaded here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="py-16 bg-gray-100" id="about">
        <div class="container mx-auto px-4">
            <div class="flex flex-col lg:flex-row items-center gap-12">
                <div class="lg:w-1/2">
                    <img src="https://images.unsplash.com/photo-1593504049359-74330189a345?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1527&q=80" alt="Pizzaiolo preparando pizza" class="rounded-xl shadow-xl w-full">
                </div>
                <div class="lg:w-1/2">
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">Nossa História</h2>
                    <p class="text-gray-600 mb-4">Fundada em 1985 pelo mestre pizzaiolo italiano Giovanni Rossi, a Pizzaria Sabor Italiano traz para o Brasil a autêntica tradição da pizza napolitana.</p>
                    <p class="text-gray-600 mb-4">Nossa massa é preparada diariamente com farinha italiana tipo 00, fermentação natural e muito cuidado. O molho de tomate é feito com tomates San Marzano importados da Itália.</p>
                    <p class="text-gray-600 mb-6">Todos os nossos ingredientes são selecionados a dedo para garantir o melhor sabor e qualidade em cada pizza que sai do nosso forno a lenha.</p>
                    
                    <div class="grid grid-cols-2 gap-4 mb-8">
                        <div class="flex items-center">
                            <div class="ingredient-icon mr-3">
                                <i class="fas fa-wheat-awn text-red-500 text-xl"></i>
                            </div>
                            <span class="font-medium">Massa artesanal</span>
                        </div>
                        <div class="flex items-center">
                            <div class="ingredient-icon mr-3">
                                <i class="fas fa-fire text-red-500 text-xl"></i>
                            </div>
                            <span class="font-medium">Forno a lenha</span>
                        </div>
                        <div class="flex items-center">
                            <div class="ingredient-icon mr-3">
                                <i class="fas fa-leaf text-red-500 text-xl"></i>
                            </div>
                            <span class="font-medium">Ingredientes frescos</span>
                        </div>
                        <div class="flex items-center">
                            <div class="ingredient-icon mr-3">
                                <i class="fas fa-flag text-red-500 text-xl"></i>
                            </div>
                            <span class="font-medium">Receita tradicional</span>
                        </div>
                    </div>
                    
                    <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="inline-block bg-red-500 hover:bg-red-600 text-white font-bold py-3 px-8 rounded-full transition duration-300">Conheça nossa cozinha</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="py-16 bg-white" id="testimonials">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">O que nossos clientes dizem</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Testimonial 1 -->
                <div class="testimonial-card p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="Cliente" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Ana Carolina</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-700">"A melhor pizza que já comi na vida! A massa é perfeita, crocante por fora e macia por dentro. A pizza de pepperoni é minha favorita."</p>
                </div>
                
                <!-- Testimonial 2 -->
                <div class="testimonial-card p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Cliente" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Ricardo Almeida</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-700">"Sou italiano e posso afirmar que essa é a pizza mais autêntica que encontrei no Brasil. O sabor me transporta direto para Nápoles."</p>
                </div>
                
                <!-- Testimonial 3 -->
                <div class="testimonial-card p-6 rounded-xl">
                    <div class="flex items-center mb-4">
                        <img src="https://randomuser.me/api/portraits/women/63.jpg" alt="Cliente" class="w-12 h-12 rounded-full mr-4">
                        <div>
                            <h4 class="font-bold">Juliana Santos</h4>
                            <div class="flex text-yellow-400">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-700">"Adoro as opções vegetarianas! A pizza de abobrinha com queijo de cabra é divina. Sempre que recebo visitas em casa, peço da Sabor Italiano."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="py-16 bg-gray-100" id="contact">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Faça seu pedido</h2>
            
            <div class="flex flex-col lg:flex-row gap-12">
                <div class="lg:w-1/2">
                    <form class="bg-white p-8 rounded-xl shadow-lg">
                        <div class="mb-6">
                            <label for="name" class="block text-gray-700 font-medium mb-2">Nome</label>
                            <input type="text" id="name" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500">
                        </div>
                        
                        <div class="mb-6">
                            <label for="phone" class="block text-gray-700 font-medium mb-2">Telefone</label>
                            <input type="tel" id="phone" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500">
                        </div>
                        
                        <div class="mb-6">
                            <label for="address" class="block text-gray-700 font-medium mb-2">Endereço</label>
                            <input type="text" id="address" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500">
                        </div>
                        
                        <div class="mb-6">
                            <label for="order" class="block text-gray-700 font-medium mb-2">Seu Pedido</label>
                            <textarea id="order" rows="4" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500"></textarea>
                        </div>
                        
                        <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="w-full block bg-red-500 hover:bg-red-600 text-white text-center font-bold py-3 px-4 rounded-lg transition duration-300">Enviar Pedido</a>
                    </form>
                </div>
                
                <div class="lg:w-1/2">
                    <div class="bg-white p-8 rounded-xl shadow-lg h-full">
                        <h3 class="text-2xl font-bold mb-6 text-gray-800">Informações de Contato</h3>
                        
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="bg-red-100 p-3 rounded-full mr-4">
                                    <i class="fas fa-map-marker-alt text-red-500 text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-gray-800">Endereço</h4>
                                    <p class="text-gray-600">Rua das Pizzas, 123 - Centro<br>São Paulo - SP</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-red-100 p-3 rounded-full mr-4">
                                    <i class="fas fa-phone-alt text-red-500 text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-gray-800">Telefone</h4>
                                    <p class="text-gray-600">(11) 1234-5678<br>(11) 98765-4321 (WhatsApp)</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-red-100 p-3 rounded-full mr-4">
                                    <i class="fas fa-clock text-red-500 text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-gray-800">Horário de Funcionamento</h4>
                                    <p class="text-gray-600">Terça a Domingo<br>18:00 - 23:30</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="bg-red-100 p-3 rounded-full mr-4">
                                    <i class="fas fa-truck text-red-500 text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-gray-800">Delivery</h4>
                                    <p class="text-gray-600">Entregamos em toda a região<br>Taxa de entrega: R$ 8,00</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mt-8">
                            <h4 class="font-bold text-gray-800 mb-4">Siga-nos nas redes sociais</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="bg-gray-100 hover:bg-red-500 hover:text-white p-3 rounded-full transition duration-300">
                                    <i class="fab fa-facebook-f"></i>
                                </a>
                                <a href="#" class="bg-gray-100 hover:bg-red-500 hover:text-white p-3 rounded-full transition duration-300">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="bg-gray-100 hover:bg-red-500 hover:text-white p-3 rounded-full transition duration-300">
                                    <i class="fab fa-whatsapp"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center mb-4">
                        <i class="fas fa-pizza-slice text-3xl text-red-500 mr-2"></i>
                        <span class="text-2xl font-bold">Sabor Italiano</span>
                    </div>
                    <p class="text-gray-400">A autêntica pizza italiana na sua cidade. Massa artesanal, ingredientes selecionados e forno a lenha.</p>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Links Rápidos</h4>
                    <ul class="space-y-2">
                        <li><a href="#home" class="text-gray-400 hover:text-white transition duration-300">Início</a></li>
                        <li><a href="#menu" class="text-gray-400 hover:text-white transition duration-300">Cardápio</a></li>
                        <li><a href="#about" class="text-gray-400 hover:text-white transition duration-300">Sobre Nós</a></li>
                        <li><a href="#testimonials" class="text-gray-400 hover:text-white transition duration-300">Avaliações</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition duration-300">Contato</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Horário de Funcionamento</h4>
                    <ul class="space-y-2 text-gray-400">
                        <li class="flex justify-between"><span>Terça - Quinta</span> <span>18:00 - 23:00</span></li>
                        <li class="flex justify-between"><span>Sexta - Sábado</span> <span>18:00 - 00:00</span></li>
                        <li class="flex justify-between"><span>Domingo</span> <span>18:00 - 23:00</span></li>
                        <li class="flex justify-between"><span>Segunda</span> <span>Fechado</span></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Newsletter</h4>
                    <p class="text-gray-400 mb-4">Inscreva-se para receber nossas promoções e novidades.</p>
                    <div class="flex">
                        <input type="email" placeholder="Seu e-mail" class="px-4 py-2 rounded-l-lg focus:outline-none text-gray-900 w-full">
                        <button class="bg-red-500 hover:bg-red-600 px-4 py-2 rounded-r-lg transition duration-300">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
                <p>&copy; 2023 Pizzaria Sabor Italiano. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <a href="#home" class="fixed bottom-6 right-6 bg-red-500 text-white p-3 rounded-full shadow-lg hover:bg-red-600 transition duration-300" id="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </a>

    <script>
        // Mobile Menu Toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // Back to Top Button
        const backToTopButton = document.getElementById('back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.add('block');
                backToTopButton.classList.remove('hidden');
            } else {
                backToTopButton.classList.add('hidden');
                backToTopButton.classList.remove('block');
            }
        });
        
        // Menu Tab Filtering
        const menuTabs = document.querySelectorAll('.menu-tab');
        const menuItemsContainer = document.getElementById('menu-items');
        
        // Sample pizza data
        const pizzas = [
            {
                name: "Margherita",
                description: "Molho de tomate, mussarela fresca, manjericão e azeite de oliva extra virgem.",
                price: "49,90",
                category: "traditional",
                image: "https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1381&q=80"
            },
            {
                name: "Pepperoni",
                description: "Molho de tomate, mussarela, pepperoni e orégano.",
                price: "54,90",
                category: "traditional",
                image: "https://images.unsplash.com/photo-1541745537411-b8046dc6d66c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1376&q=80"
            },
            {
                name: "Quatro Queijos",
                description: "Molho de tomate, mussarela, provolone, parmesão e gorgonzola.",
                price: "59,90",
                category: "traditional",
                image: "https://images.unsplash.com/photo-1595854341625-f33ee10dbf94?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80"
            },
            {
                name: "Calabresa",
                description: "Molho de tomate, mussarela, calabresa fatiada e cebola.",
                price: "52,90",
                category: "traditional",
                image: "https://images.unsplash.com/photo-1588315028884-8f9697ab120b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80"
            },
            {
                name: "Vegetariana Premium",
                description: "Berinjela, abobrinha, pimentão, champignon, tomate seco e queijo de cabra.",
                price: "64,90",
                category: "vegetarian",
                image: "https://images.unsplash.com/photo-1571407970349-bc81e7e96d47?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1450&q=80"
            },
            {
                name: "Frango com Catupiry",
                description: "Molho de tomate, mussarela, frango desfiado e catupiry.",
                price: "57,90",
                category: "special",
                image: "https://images.unsplash.com/photo-1613564834361-9436948817d1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1433&q=80"
            },
            {
                name: "Portuguesa",
                description: "Molho de tomate, mussarela, presunto, ovos, cebola, azeitona e pimentão.",
                price: "59,90",
                category: "special",
                image: "https://images.unsplash.com/photo-1601924582970-9238bcb495d9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80"
            },
            {
                name: "Napolitana",
                description: "Molho de tomate, mussarela de búfala, tomate cereja, rúcula e parmesão.",
                price: "69,90",
                category: "special",
                image: "https://images.unsplash.com/photo-1593504049359-74330189a345?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1527&q=80"
            },
            {
                name: "Pizza Doce de Nutella",
                description: "Massa doce, nutella, morangos frescos e raspas de chocolate branco.",
                price: "49,90",
                category: "dessert",
                image: "https://images.unsplash.com/photo-1593246049226-ded77bf90326?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1450&q=80"
            }
        ];
        
        // Function to render menu items
        function renderMenuItems(category = 'all') {
            menuItemsContainer.innerHTML = '';
            
            const filteredPizzas = category === 'all' 
                ? pizzas 
                : pizzas.filter(pizza => pizza.category === category);
            
            filteredPizzas.forEach(pizza => {
                const pizzaCard = document.createElement('div');
                pizzaCard.className = 'pizza-card bg-white rounded-xl overflow-hidden shadow-lg';
                pizzaCard.innerHTML = `
                    <img src="${pizza.image}" alt="${pizza.name}" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">${pizza.name}</h3>
                        <p class="text-gray-600 mb-4">${pizza.description}</p>
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold text-red-500">R$ ${pizza.price}</span>
                            <a href="https://api.whatsapp.com/send/?phone=5516988596884&text=Ol%C3%A1%21%20Tenho%20interesse%20no%20conte%C3%BAdo%20do%20DominaComigo.&type=phone_number&app_absent=0" class="bg-red-500 hover:bg-red-600 text-white py-2 px-4 rounded-lg transition duration-300">Pedir</a>
                        </div>
                    </div>
                `;
                menuItemsContainer.appendChild(pizzaCard);
            });
        }
        
        // Initial render
        renderMenuItems();
        
        // Tab click event
        menuTabs.forEach(tab => {
            tab.addEventListener('click', () => {
                // Remove active class from all tabs
                menuTabs.forEach(t => t.classList.remove('active'));
                // Add active class to clicked tab
                tab.classList.add('active');
                // Filter menu items
                const category = tab.getAttribute('data-category');
                renderMenuItems(category);
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                mobileMenu.classList.add('hidden');
            });
        });
    </script>
</body>
</html>
