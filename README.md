<!DOCTYPE html> 
<html lang="ar"> 
<head>     
    <meta charset="UTF-8">     
    <meta name="viewport" content="width=device-width, initial-scale=1.0">     
    <title>For My Nourtii 💗</title>     
    <style>         
        * {             
            box-sizing: border-box;         
        }         
        body {              
            background-color: #ffd1dc;             
            /* صورة الخلفية المباشرة */             
            background: linear-gradient(rgba(255, 182, 193, 0.3), rgba(255, 182, 193, 0.3)), url('https://i.ibb.co/whp09bH7/image.jpg') no-repeat center center/cover;              
            min-height: 100vh;              
            display: flex;              
            align-items: center;              
            justify-content: center;              
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;             
            margin: 0;             
            padding: 20px;             
            overflow-x: hidden;              
            position: relative;         
        }          
        
        .hearts-container {             
            position: absolute;             
            top: 0;             
            left: 0;             
            width: 100%;             
            height: 100%;             
            z-index: 0;              
            pointer-events: none;          
        }          
        
        /* الكارت الرئيسي بتأثير زجاجي مدمج مع أنيميشن دخول */
        .card {              
            background: rgba(255, 255, 255, 0.94);              
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            padding: 30px;              
            border-radius: 24px;              
            text-align: center;              
            width: 100%;              
            max-width: 440px;              
            box-shadow: 0 15px 35px rgba(255, 105, 180, 0.25);              
            border: 2px solid rgba(255, 210, 220, 0.6);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;             
            z-index: 10;          
            animation: cardEntrance 0.8s ease-out;
        }          

        @keyframes cardEntrance {
            from { opacity: 0; transform: translateY(30px) scale(0.96); }
            to { opacity: 1; transform: translateY(0) scale(1); }
        }

        /* أنيميشن الاهتزاز عند الخطأ */
        .shake {
            animation: shakeAnim 0.4s ease-in-out;
        }
        @keyframes shakeAnim {
            0%, 100% { transform: translateX(0); }
            20%, 60% { transform: translateX(-10px); }
            40%, 80% { transform: translateX(10px); }
        }

        .avatar {              
            width: 120px;              
            height: 120px;              
            border-radius: 50%;              
            margin-bottom: 20px;              
            object-fit: cover;             
            border: 4px solid #ff85a1;          
            box-shadow: 0 8px 20px rgba(255, 133, 161, 0.3);
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .avatar:hover {
            transform: scale(1.06) rotate(3deg);
        }

        .input-box {              
            padding: 14px;              
            font-size: 16px;              
            margin-bottom: 18px;              
            width: 85%;              
            border: 2px solid #ffd1dc;              
            border-radius: 25px;             
            text-align: center;             
            outline: none;             
            color: #d81b60;          
            transition: all 0.3s ease;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.02);
        }          
        .input-box:focus { 
            border-color: #ff85a1; 
            box-shadow: 0 0 8px rgba(255, 133, 161, 0.3);
        }          

        .btn {              
            padding: 12px 30px;              
            cursor: pointer;              
            background: #ff85a1;              
            color: white;              
            border: none;              
            border-radius: 25px;              
            font-size: 16px;             
            font-weight: bold;             
            box-shadow: 0 4px 12px rgba(255, 133, 161, 0.3);
            transition: all 0.2s ease;
            -webkit-user-select: none;
            user-select: none;
        }         
        .btn:hover { 
            background: #ff6b8e; 
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 107, 142, 0.4);
        }         
        .btn:active {
            transform: scale(0.95);
        }

        .btn-group {             
            display: flex;             
            justify-content: center;             
            gap: 10px;             
            margin: 20px 0;          
            background: #fff0f5;
            padding: 5px;
            border-radius: 15px;
        }          
        
        .btn-sub {             
            flex: 1;
            padding: 10px 18px;             
            cursor: pointer;             
            background: transparent;              
            color: #d81b60;              
            border: none;             
            border-radius: 12px;             
            font-size: 14px;             
            font-weight: bold;         
            transition: all 0.3s ease;
        }         
        .btn-sub.active { 
            background: #ff85a1; 
            color: white; 
            box-shadow: 0 4px 10px rgba(255, 133, 161, 0.2);
        }
        .btn-sub:active {
            transform: scale(0.95);
        }

        .hidden { display: none !important; }          
        
        .content-text {              
            text-align: justify;              
            line-height: 1.7;              
            color: #555;             
            font-size: 15px;         
            animation: fadeInTab 0.4s ease-out;
        }          
        
        @keyframes fadeInTab {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .gallery {             
            display: grid;             
            grid-template-columns: repeat(2, 1fr);             
            gap: 12px;             
            margin-top: 15px;         
        }         
        
        .grid-item {
            border-radius: 12px;             
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(255, 105, 180, 0.15);             
            border: 2px solid #fff;         
            opacity: 0;
            transform: scale(0.95) translateY(10px);
            animation: imgEntrance 0.5s cubic-bezier(0.165, 0.84, 0.44, 1) forwards;
        }

        @keyframes imgEntrance {
            to { opacity: 1; transform: scale(1) translateY(0); }
        }

        /* أنيميشن تتابعي لظهور الصور */
        .grid-item:nth-child(1) { animation-delay: 0.05s; }
        .grid-item:nth-child(2) { animation-delay: 0.12s; }
        .grid-item:nth-child(3) { animation-delay: 0.19s; }
        .grid-item:nth-child(4) { animation-delay: 0.26s; }
        .grid-item:nth-child(5) { animation-delay: 0.33s; }

        .gallery .grid-item img {             
            width: 100%;             
            height: 140px;             
            object-fit: cover;             
            display: block;
            image-rendering: -webkit-optimize-contrast;
            transition: transform 0.5s cubic-bezier(0.165, 0.84, 0.44, 1);
        }         
        
        /* ضبط كادر الصورة الخامسة الكبيرة تلقائياً */
        .gallery .grid-item:first-child:nth-last-child(5),         
        .gallery .grid-item:first-child:nth-last-child(5) ~ .grid-item:nth-child(5) {             
            grid-column: span 2;             
        }          
        .gallery .grid-item:first-child:nth-last-child(5) ~ .grid-item:nth-child(5) img {
            height: 180px;
        }

        /* تأثير الحركة للصور عند التمرير */
        .grid-item:hover img {
            transform: scale(1.07);
        }

        .poem-box {             
            background: #fff0f5;              
            padding: 15px;             
            border-radius: 12px;             
            border-right: 4px solid #ff85a1;             
            margin: 15px 0;             
            font-style: italic;             
            color: #444;             
            direction: rtl;             
            text-align: right;         
            font-weight: 500;
            line-height: 1.8;
            animation: fadeInTab 0.5s ease-out;
        }          
        
        .footer-text {             
            font-size: 14px;             
            color: #ff85a1;             
            margin-top: 18px;             
            font-weight: bold;         
            line-height: 1.4;
        }          
        
        /* تنسيق القلوب المتساقطة الجميل */
        .heart {             
            position: absolute;             
            background-color: #ffb6c1;              
            display: inline-block;             
            width: 10px;             
            height: 10px;             
            opacity: 0.7;             
            transform: rotate(-45deg);             
            animation: fall linear infinite;         
        }         
        .heart::after, .heart::before {             
            content: '';             
            position: absolute;             
            background-color: #ffb6c1;             
            border-radius: 50%;             
            width: 10px;             
            height: 10px;         
        }         
        .heart::after { top: 0px; left: 5px; }         
        .heart::before { top: -5px; left: 0px; }          
        
        @keyframes fall {             
            0% { top: -50px; transform: translateX(0px) rotate(-45deg); }             
            100% { top: 100vh; transform: translateX(80px) rotate(45deg); }         
        }     
    </style> 
</head> 
<body>      
    <div class="hearts-container" id="heartsContainer"></div>      
    
    <!-- شاشة القفل -->     
    <div id="lock" class="card">         
        <img src="https://i.ibb.co/DgSrLL5D/image.jpg" class="avatar" alt="Nourtii">         
        <br>         
        <input type="password" id="pass" class="input-box" placeholder="Enter Password">         
        <br>         
        <button class="btn" onclick="check()">Enter ✨</button>         
        <p id="msg" style="color:#d81b60; font-weight:bold; margin-top:12px; min-height: 20px;"></p>                     
        
        <div class="footer-text">             
            Made with love <br>             
            (Toto)         
        </div>     
    </div>      
    
    <!-- المحتوى الرئيسي للمفاجأة -->     
    <div id="gift" class="card hidden">         
        <h2 style="color: #d81b60; font-size: 26px;">Happy birthday, my fav Nour 💗</h2>                     
        
        <div class="btn-group">             
            <button id="tabBtnPro" class="btn-sub active" onclick="show('pro')">Profile</button>             
            <button id="tabBtnRead" class="btn-sub" onclick="show('read')">Read Me</button>         
        </div>                     
        
        <!-- قسم البروفايل -->         
        <div id="pro">             
            <h3 style="color:#ff85a1; margin-bottom: 8px;">A little about u</h3>             
            <p class="content-text">I spent a lot of time with you, but it's still like I'm learning something new about you. I'm still amazed by you, your success, your ambition, and your skill in making life more beautiful and sweeter. But now I know something important about you, you are everything💗.</p>                                       
            
            <h4 style="color:#d81b60; margin-top: 20px; margin-bottom: 10px;">Twenty two 💗</h4>             
            <div class="gallery">                 
                <div class="grid-item"><img src="https://i.ibb.co/997wGQHp/image.jpg" alt="Pic 1"></div>                 
                <div class="grid-item"><img src="https://i.ibb.co/GvJFMbcy/image.jpg" alt="Pic 2"></div>                 
                <div class="grid-item"><img src="https://i.ibb.co/jkyN5h1k/image.jpg" alt="Pic 3"></div>                 
                <div class="grid-item"><img src="https://i.ibb.co/Hp2M08Nr/image.jpg" alt="Pic 4"></div>                 
                <div class="grid-item"><img src="https://i.ibb.co/2Yyss0ZD/image.jpg" alt="Pic 5"></div>             
            </div>         
        </div>                     
        
        <!-- قسم Read Me -->         
        <div id="read" class="hidden">             
            <div id="readContent">                 
                <p class="content-text">Happy birthday, my love, my soul, my life, the most precious thing in the world. May those eyes always be with me. Happy birthday to the most brilliant doctor in the world.</p>                                   
                
                <div class="poem-box">                     
                    يا مَنْ سَكَنْتَ القَلْبَ مِنْ أَعْمَاقِهِ... يَوْمُ المِيْلادِ.. يَوْمُ سَعَادَتِي بِإِشْرَاقِهِ<br>                     
                    كُلُّ عَامٍ وَأَنْتَ الخَيْرُ فِي حَيَاتِنَا... وَكُلُّ عَمْرٍ تَقْضِيْهِ فِي أَمَلٍ وَرِوَاقِهِ                 
                </div>                                   
                
                <button class="btn" style="margin-top:10px;" onclick="finalLetter()">Read More ♥️</button>             
            </div>         
        </div>     
    </div>      
    
    <script>         
        const lockCard = document.getElementById('lock');
        const giftCard = document.getElementById('gift');
        const msgEl = document.getElementById('msg');

        function check() {             
            if(document.getElementById('pass').value === "1062004") {                 
                // أنيميشن الخروج والدخول السلس والاحترافي
                lockCard.style.opacity = "0";
                lockCard.style.transform = "scale(0.94) translateY(-15px)";
                
                setTimeout(() => {
                    lockCard.classList.add('hidden');                 
                    giftCard.classList.remove('hidden');                 
                }, 400);
            } else {                 
                // أنيميشن الاهتزاز الفوري المطور عند الخطأ
                lockCard.classList.remove("shake");
                void lockCard.offsetWidth; 
                lockCard.classList.add("shake");
                
                msgEl.innerText = "wrong ya nourtii ❌";             
                setTimeout(() => {
                    msgEl.innerText = "";
                    document.getElementById('pass').value = "";
                }, 1500);
            }         
        }          
        
        function show(id) {              
            document.getElementById('pro').classList.add('hidden');              
            document.getElementById('read').classList.add('hidden');              
            document.getElementById('tabBtnPro').classList.remove('active');
            document.getElementById('tabBtnRead').classList.remove('active');
            
            document.getElementById(id).classList.remove('hidden');          
            
            if(id === 'pro') document.getElementById('tabBtnPro').classList.add('active');
            if(id === 'read') document.getElementById('tabBtnRead').classList.add('active');
        }          
        
        function finalLetter() {             
            document.getElementById('readContent').innerHTML = `             
            <div style="direction:rtl; text-align:right; line-height:1.8; color:#333; animation: fadeInTab 0.5s ease-out;">                 
                لم تقدر اللغة الأجنبية أن تبوح عن ما في صدري وعن الكلمات التي أحملها .. معذروة هذه اللغة البائسة جماد مكونه من أحرف ليس لها القدرة على أي شيء حتى أنا معي من المعاني الكثير و من الجمل و الفصاحه ولكني أقف أمامك مكتوف اليدين ، هل أخبرك عن سبب حُبي لكِ أما عن قدر حُبي لكِ ؟                  
                <br><br>                 
                أريد أن أخبرك عن أشياء كثيره أهمها أن تكوني معي للأبد لأبقى أخبرك باقي حياتي كلها عن مقدار حبي ولكنه لن يكفي أيضاً                  
                <br><br>                 
                <div style="text-align:center; font-size: 22px; font-weight:bold; color:#d81b60; margin-top: 20px; animation: cardEntrance 0.6s ease-out;">أُحبك يا نور 💗</div>             
            </div>`;         
        }          
        
        function createHearts() {             
            const container = document.getElementById('heartsContainer');             
            const heartCount = 25;               
            for (let i = 0; i < heartCount; i++) {                 
                const heart = document.createElement('div');                 
                heart.classList.add('heart');                 
                heart.style.left = Math.random() * 100 + 'vw';                 
                const size = Math.random() * 8 + 8 + 'px';                 
                heart.style.width = size;                 
                heart.style.height = size;                 
                heart.style.animationDuration = Math.random() * 3 + 4 + 's';                  
                heart.style.animationDelay = Math.random() * 4 + 's';                 
                container.appendChild(heart);             
            }         
        }          
        
        window.onload = createHearts;     
    </script> 
</body> 
</html>
