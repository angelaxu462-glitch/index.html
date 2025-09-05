# index.html<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GlobalConnect Solutions - Secure Business Networking</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            background: linear-gradient(135deg, #2c3e50, #1a2530);
            color: white;
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 28px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), url('https://images.unsplash.com/photo-1497215728101-856f4ea42174?ixlib=rb-1.2.1&auto=format&fit=crop&w=1500&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 80px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #3498db;
            color: white;
            padding: 12px 25px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #2980b9;
        }
        
        .features {
            padding: 70px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: #2c3e50;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: #7f8c8d;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .feature-card {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-card i {
            font-size: 40px;
            color: #3498db;
            margin-bottom: 20px;
        }
        
        .feature-card h3 {
            margin-bottom: 15px;
            color: #2c3e50;
        }
        
        .feature-card p {
            color: #7f8c8d;
        }
        
        .testimonials {
            background-color: #ecf0f1;
            padding: 70px 0;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-card p {
            font-style: italic;
            margin-bottom: 20px;
            color: #2c3e50;
        }
        
        .client {
            display: flex;
            align-items: center;
        }
        
        .client img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }
        
        .client-info h4 {
            color: #2c3e50;
        }
        
        .client-info p {
            font-style: normal;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        footer {
            background-color: #2c3e50;
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-section p {
            margin-bottom: 15px;
            color: #ecf0f1;
        }
        
        .footer-section a {
            color: #ecf0f1;
            text-decoration: none;
            display: block;
            margin-bottom: 10px;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: #3498db;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #ecf0f1;
            font-size: 0.9rem;
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            max-width: 500px;
            width: 90%;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }
        
        .modal-content h2 {
            color: #e74c3c;
            margin-bottom: 20px;
        }
        
        .modal-content p {
            margin-bottom: 25px;
            color: #2c3e50;
            line-height: 1.6;
        }
        
        .modal-btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .modal-btn:hover {
            background-color: #2980b9;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-shield-alt"></i>
                <span>GlobalConnect Solutions</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="nav-link">Home</a></li>
                    <li><a href="#" class="nav-link">Services</a></li>
                    <li><a href="#" class="nav-link">About</a></li>
                    <li><a href="#" class="nav-link">Contact</a></li>
                    <li><a href="#" class="nav-link">Login</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Secure Business Networking Solutions</h1>
            <p>Protecting your digital assets with cutting-edge security solutions and enterprise-grade network infrastructure.</p>
            <a href="#" class="btn demo-btn">Request a Demo</a>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>Comprehensive security solutions for businesses of all sizes</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-lock"></i>
                    <h3>Network Security</h3>
                    <p>Advanced firewall protection and intrusion detection systems to keep your network secure from threats.</p>
                    <a href="#" class="feature-link">Learn more →</a>
                </div>
                <div class="feature-card">
                    <i class="fas fa-cloud"></i>
                    <h3>Cloud Security</h3>
                    <p>Secure cloud infrastructure with encrypted data storage and secure access management.</p>
                    <a href="#" class="feature-link">Learn more →</a>
                </div>
                <div class="feature-card">
                    <i class="fas fa-user-shield"></i>
                    <h3>Identity Management</h3>
                    <p>Multi-factor authentication and identity verification systems to protect user accounts.</p>
                    <a href="#" class="feature-link">Learn more →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Clients Say</h2>
                <p>Trusted by businesses worldwide</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <p>"GlobalConnect Solutions transformed our network security. Their team is professional and responsive."</p>
                    <div class="client">
                        <img src="https://randomuser.me/api/portraits/women/65.jpg" alt="Client">
                        <div class="client-info">
                            <h4>Sarah Johnson</h4>
                            <p>CTO, TechCorp Inc.</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"The implementation was seamless and our security posture improved dramatically. Highly recommended!"</p>
                    <div class="client">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Client">
                        <div class="client-info">
                            <h4>Michael Chen</h4>
                            <p>IT Director, FinanceGlobal</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p>"Their cloud security solutions helped us achieve compliance with industry regulations without hassle."</p>
                    <div class="client">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Client">
                        <div class="client-info">
                            <
