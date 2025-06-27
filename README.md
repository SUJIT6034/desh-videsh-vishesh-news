<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>मुफ्त हिंदी समाचार</title>
    <link href="https://fonts.googleapis.com/css2?family=Hind:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Hind', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, #1a237e 0%, #311b92 100%);
            color: white;
            padding: 1rem 5%;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 2rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav li {
            margin-left: 1.5rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            transition: opacity 0.3s;
            padding: 0.5rem;
            border-radius: 4px;
        }
        
        nav a:hover, .active {
            background: rgba(255,255,255,0.15);
        }
        
        .search-container {
            display: flex;
            margin: 1rem 5%;
            max-width: 1200px;
            margin: 1rem auto;
            padding: 0 5%;
        }
        
        #search-input {
            flex: 1;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
        }
        
        #search-button {
            background: #1a237e;
            color: white;
            border: none;
            padding: 0 1.5rem;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s;
        }
        
        #search-button:hover {
            background: #311b92;
        }
        
        .categories {
            display: flex;
            overflow-x: auto;
            padding: 0.5rem 5%;
            background: white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .category-btn {
            background: #f0f4f8;
            border: none;
            padding: 0.6rem 1.2rem;
            margin: 0 0.5rem;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s;
            white-space: nowrap;
            font-size: 0.95rem;
        }
        
        .category-btn:hover, .category-btn.active {
            background: #1a237e;
            color: white;
        }
        
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 5%;
        }
        
        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 1.5rem;
        }
        
        .news-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .news-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .news-image {
            width: 100%;
            height: 180px;
            object-fit: cover;
            display: block;
        }
        
        .news-content {
            padding: 1.5rem;
        }
        
        .news-category {
            display: inline-block;
            background: #e8eaf6;
            color: #1a237e;
            padding: 0.3rem 0.8rem;
            border-radius: 4px;
            font-size: 0.85rem;
            margin-bottom: 0.8rem;
        }
        
        .news-title {
            font-size: 1.25rem;
            margin-bottom: 0.8rem;
            color: #1a237e;
            font-weight: 700;
        }
        
        .news-description {
            color: #555;
            margin-bottom: 1.2rem;
            font-size: 0.95rem;
        }
        
        .news-meta {
            display: flex;
            justify-content: space-between;
            color: #777;
            font-size: 0.85rem;
        }
        
        .read-more {
            display: inline-block;
            background: #1a237e;
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            margin-top: 0.5rem;
            transition: background 0.3s;
        }
        
        .read-more:hover {
            background: #311b92;
        }
        
        footer {
            background: #1a237e;
            color: white;
            text-align: center;
            padding: 2rem 5%;
            margin-top: 3rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
            }
            
            .logo {
                margin-bottom: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav li {
                margin: 0.5rem;
            }
            
            .news-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo">
                <span>📰</span> मुफ्त हिंदी समाचार
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active">होम</a></li>
                    <li><a href="#">देश</a></li>
                    <li><a href="#">विश्व</a></li>
                    <li><a href="#">राजनीति</a></li>
                    <li><a href="#">खेल</a></li>
                    <li><a href="#">मनोरंजन</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <div class="search-container">
        <input type="text" id="search-input" placeholder="समाचार खोजें...">
        <button id="search-button">खोजें</button>
    </div>
    
    <div class="categories">
        <button class="category-btn active">सभी</button>
        <button class="category-btn">राष्ट्रीय</button>
        <button class="category-btn">अंतर्राष्ट्रीय</button>
        <button class="category-btn">राज्य</button>
        <button class="category-btn">खेल</button>
        <button class="category-btn">व्यापार</button>
        <button class="category-btn">मनोरंजन</button>
        <button class="category-btn">स्वास्थ्य</button>
        <button class="category-btn">प्रौद्योगिकी</button>
    </div>
    
    <div class="container">
        <h2 style="color: #1a237e; margin-bottom: 1rem;">ताज़ा समाचार</h2>
        <div class="news-grid" id="news-container">
            <!-- समाचार यहां लोड होंगे -->
            <div class="loading">समाचार लोड हो रहे हैं...</div>
        </div>
    </div>
    
    <footer>
        <div class="footer-content">
            <h3>मुफ्त हिंदी समाचार</h3>
            <p>सभी के लिए निःशुल्क और सुलभ समाचार सेवा</p>
            <p style="margin-top: 1rem; font-size: 0.9rem;">&copy; 2024 सर्वाधिकार सुरक्षित</p>
        </div>
    </footer>

    <script>
        // API कुंजी और सेटिंग्स
        const API_KEY = "YOUR_API_KEY"; // यहाँ अपना API Key डालें
        const NEWS_URL = `https://gnews.io/api/v4/top-headlines?category=general&lang=hi&apikey=${API_KEY}`;
        
        // DOM तत्व
        const newsContainer = document.getElementById('news-container');
        const categoryButtons = document.querySelectorAll('.category-btn');
        const searchInput = document.getElementById('search-input');
        const searchButton = document.getElementById('search-button');
        
        // समाचार प्राप्त करें और प्रदर्शित करें
        async function fetchNews(category = 'general') {
            try {
                newsContainer.innerHTML = '<div class="loading">समाचार लोड हो रहे हैं...</div>';
                
                const url = `https://gnews.io/api/v4/top-headlines?category=${category}&lang=hi&apikey=${API_KEY}`;
                const response = await fetch(url);
                
                if (!response.ok) {
                    throw new Error('समाचार प्राप्त करने में समस्या');
                }
                
                const data = await response.json();
                displayNews(data.articles);
            } catch (error) {
                console.error("त्रुटि:", error);
                newsContainer.innerHTML = `<div class="error">समाचार लोड करने में असफल। कृपया बाद में पुनः प्रयास करें।<br>${error.message}</div>`;
            }
        }
        
        // समाचार प्रदर्शित करें
        function displayNews(articles) {
            if (!articles || articles.length === 0) {
                newsContainer.innerHTML = '<div class="no-news">कोई समाचार उपलब्ध नहीं है</div>';
                return;
            }
            
            newsContainer.innerHTML = '';
            
            articles.slice(0, 12).forEach(article => {
                const newsCard = document.createElement('div');
                newsCard.className = 'news-card';
                
                // तारीख को पढ़ने योग्य प्रारूप में बदलें
                const date = new Date(article.publishedAt);
                const formattedDate = date.toLocaleDateString('hi-IN', {
                    day: 'numeric',
                    month: 'long',
                    year: 'numeric'
                });
                
                newsCard.innerHTML = `
                    <img src="${article.image || 'https://via.placeholder.com/300x180?text=News+Image'}" alt="${article.title}" class="news-image">
                    <div class="news-content">
                        <span class="news-category">${article.source.name}</span>
                        <h3 class="news-title">${article.title}</h3>
                        <p class="news-description">${article.description || 'विवरण उपलब्ध नहीं'}</p>
                        <div class="news-meta">
                            <span>${formattedDate}</span>
                        </div>
                        <a href="${article.url}" target="_blank" class="read-more">पूरा पढ़ें</a>
                    </div>
                `;
                
                newsContainer.appendChild(newsCard);
            });
        }
        
        // श्रेणी बटन कार्यक्षमता
        categoryButtons.forEach(button => {
            button.addEventListener('click', () => {
                // सक्रिय वर्ग हटाएं
                categoryButtons.forEach(btn => btn.classList.remove('active'));
                // वर्तमान बटन को सक्रिय करें
                button.classList.add('active');
                
                // श्रेणी मान प्राप्त करें (अंग्रेजी में API आवश्यकताओं के लिए)
                const categoryMap = {
                    'सभी': 'general',
                    'राष्ट्रीय': 'national',
                    'अंतर्राष्ट्रीय': 'world',
                    'राज्य': 'general', // API में विशिष्ट श्रेणी नहीं
                    'खेल': 'sports',
                    'व्यापार': 'business',
                    'मनोरंजन': 'entertainment',
                    'स्वास्थ्य': 'health',
                    'प्रौद्योगिकी': 'technology'
                };
                
                const category = categoryMap[button.textContent] || 'general';
                fetchNews(category);
            });
        });
        
        // खोज कार्यक्षमता
        searchButton.addEventListener('click', performSearch);
        searchInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') performSearch();
        });
        
        function performSearch() {
            const query = searchInput.value.trim();
            if (query) {
                // सरल क्लाइंट-साइड खोज
                const cards = document.querySelectorAll('.news-card');
                let found = false;
                
                cards.forEach(card => {
                    const title = card.querySelector('.news-title').textContent.toLowerCase();
                    const description = card.querySelector('.news-description').textContent.toLowerCase();
                    
                    if (title.includes(query.toLowerCase()) || description.includes(query.toLowerCase())) {
                        card.style.display = 'block';
                        found = true;
                    } else {
                        card.style.display = 'none';
                    }
                });
                
                if (!found) {
                    newsContainer.innerHTML = `<div class="no-results">"${query}" के लिए कोई परिणाम नहीं मिला</div>`;
                }
            }
        }
        
        // पृष्ठ लोड होने पर समाचार प्राप्त करें
        window.onload = () => {
            fetchNews();
            
            // सभी भाइयों-बहनों के लिए सरल भाषा में निर्देश
            alert("आपकी न्यूज़ वेबसाइट तैयार है! अब आपको बस इतना करना है:\n\n1. YOUR_API_KEY को बदलें (gnews.io से मुफ्त API Key लें)\n2. इस फाइल को किसी भी होस्टिंग पर अपलोड करें");
        };
    </script>
</body>
</html>
