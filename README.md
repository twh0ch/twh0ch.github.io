<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Свадебное приглашение</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Caveat:wght@400;600;700&family=Comfortaa:wght@300;400;500&display=swap');
        
        body {
            margin: 0;
            padding: 20px;
            font-family: 'Comfortaa', sans-serif;
            background: linear-gradient(135deg, #f5e6d3 0%, #e8d5c4 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .invitation {
            background: linear-gradient(135deg, #faf4f0 0%, #f0e6d8 100%);
            border-radius: 20px;
            padding: 30px;
            max-width: 650px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .invitation::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,192,203,0.1) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        .header {
            font-family: 'Caveat', cursive;
            font-size: 2.5em;
            color: #d4779b;
            margin-bottom: 20px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            position: relative;
            z-index: 1;
        }
        
        .dear {
            font-size: 1.1em;
            color: #8b4513;
            margin-bottom: 8px;
            font-weight: 300;
            position: relative;
            z-index: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .name-line {
            border-bottom: 2px solid #d4779b;
            width: 200px;
            position: relative;
            display: inline-block;
        }
        
        .name-on-line {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #faf4f0 0%, #f0e6d8 100%);
            padding: 2px 12px;
            font-size: 0.95em;
            color: #d4779b;
            font-weight: 500;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        .invitation-text {
            font-size: 1em;
            color: #8b4513;
            margin: 20px 0;
            line-height: 1.4;
            position: relative;
            z-index: 1;
        }
        
        .event-details {
            background: rgba(255,255,255,0.6);
            border-radius: 15px;
            padding: 20px;
            margin: 25px 0;
            position: relative;
            z-index: 1;
        }
        
        .date-time {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .date {
            font-size: 1.8em;
            color: #d4779b;
            font-weight: 600;
        }
        
        .time-venue {
            text-align: right;
        }
        
        .time {
            font-size: 1.3em;
            color: #d4779b;
            font-weight: 500;
        }
        
        .venue {
            font-size: 1.1em;
            color: #8b4513;
            margin-top: 5px;
        }
        
        .ceremony-time {
            font-size: 1.5em;
            color: #d4779b;
            font-weight: 600;
            margin-top: 10px;
        }
        
        .timeline {
            background: rgba(255,255,255,0.7);
            border-radius: 15px;
            padding: 20px;
            margin: 25px 0;
            position: relative;
            z-index: 1;
        }
        
        .timeline-title {
            font-size: 1.3em;
            color: #d4779b;
            font-weight: 600;
            margin-bottom: 15px;
            font-family: 'Caveat', cursive;
        }
        
        .timeline-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 10px 0;
            padding: 8px 15px;
            background: rgba(212, 119, 155, 0.1);
            border-radius: 10px;
            border-left: 4px solid #d4779b;
        }
        
        .timeline-event {
            font-size: 1.1em;
            color: #8b4513;
            font-weight: 500;
        }
        
        .timeline-time {
            font-size: 1.2em;
            color: #d4779b;
            font-weight: 600;
        }
        
        .timeline-photos {
            display: flex;
            justify-content: space-around;
            margin: 20px 0;
            gap: 20px;
        }
        
        .timeline-photo {
            width: 200px;
            height: 200px;
            border-radius: 15px;
            background: linear-gradient(135deg, #e8d5c4 0%, #d4779b 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9em;
            color: white;
            font-weight: 500;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
            transition: transform 0.3s ease;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
        
        .timeline-photo:hover {
            transform: scale(1.02);
        }
        
        .ceremony-label {
            font-size: 0.9em;
            color: #8b4513;
            margin-bottom: 5px;
        }
        
        .notes {
            font-size: 0.9em;
            color: #8b4513;
            margin: 20px 0;
            line-height: 1.5;
            position: relative;
            z-index: 1;
        }
        
        .note-item {
            margin-bottom: 10px;
            text-align: left;
        }
        
        .couple-photos {
            display: flex;
            justify-content: space-around;
            margin: 30px 0;
            position: relative;
            z-index: 1;
            gap: 30px;
        }
        
        .photo-container {
            position: relative;
            text-align: center;
        }
        
        .photo {
            width: 160px;
            height: 200px;
            border-radius: 15px;
            background: linear-gradient(135deg, #e8d5c4 0%, #d4779b 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.9em;
            color: white;
            font-weight: 500;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
            transition: transform 0.3s ease;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
        
        .photo:hover {
            transform: scale(1.05);
        }
        
        .name-tag {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: #d4779b;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-family: 'Caveat', cursive;
            font-size: 1.2em;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        .love-equation {
            font-family: 'Caveat', cursive;
            font-size: 1.5em;
            color: #d4779b;
            margin-top: 20px;
            font-weight: 600;
            position: relative;
            z-index: 1;
        }
        
        .heart {
            color: #ff6b8a;
            font-size: 1.2em;
            animation: heartbeat 1.5s ease-in-out infinite;
        }
        
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .footer-addresses {
            background: rgba(255,255,255,0.8);
            border-radius: 15px;
            padding: 25px;
            margin: 30px 0 0 0;
            position: relative;
            z-index: 1;
            border-top: 3px solid #d4779b;
        }
        
        .addresses-title {
            font-family: 'Caveat', cursive;
            font-size: 1.4em;
            color: #d4779b;
            font-weight: 600;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .address-section {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .address-item {
            flex: 1;
            background: rgba(212, 119, 155, 0.1);
            border-radius: 12px;
            padding: 15px;
            text-align: center;
            border: 2px solid rgba(212, 119, 155, 0.2);
            transition: all 0.3s ease;
        }
        
        .address-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-color: #d4779b;
        }
        
        .address-label {
            font-size: 1.1em;
            color: #d4779b;
            font-weight: 600;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }
        
        .address-text {
            font-size: 0.9em;
            color: #8b4513;
            line-height: 1.4;
        }
        
        .address-time {
            font-size: 0.8em;
            color: #d4779b;
            font-weight: 500;
            margin-top: 5px;
            font-style: italic;
        }
        
        .decorative-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        .flower {
            position: absolute;
            font-size: 2em;
            opacity: 0.3;
            animation: sway 4s ease-in-out infinite;
        }
        
        .flower:nth-child(1) { top: 10%; left: 5%; animation-delay: 0s; }
        .flower:nth-child(2) { top: 20%; right: 5%; animation-delay: 1s; }
        .flower:nth-child(3) { bottom: 30%; left: 10%; animation-delay: 2s; }
        .flower:nth-child(4) { bottom: 10%; right: 10%; animation-delay: 3s; }
        
        @keyframes sway {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-10px) rotate(5deg); }
        }
        
        .rsvp-section {
            background: rgba(255,255,255,0.9);
            border-radius: 15px;
            padding: 25px;
            margin: 30px 0;
            position: relative;
            z-index: 1;
            border: 2px solid #d4779b;
        }
        
        .rsvp-title {
            font-family: 'Caveat', cursive;
            font-size: 1.5em;
            color: #d4779b;
            font-weight: 600;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .rsvp-button {
            width: 100%;
            padding: 20px;
            background: linear-gradient(135deg, #d4779b 0%, #ff6b8a 100%);
            color: white;
            border: none;
            border-radius: 15px;
            font-family: 'Comfortaa', sans-serif;
            font-size: 1.2em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 6px 20px rgba(212, 119, 155, 0.3);
            text-decoration: none;
            display: block;
            text-align: center;
        }
        
        .rsvp-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(212, 119, 155, 0.4);
        }
        
        .rsvp-description {
            font-size: 0.9em;
            color: #8b4513;
            margin-bottom: 20px;
            line-height: 1.5;
        }
        
        @media (max-width: 480px) {
            .invitation {
                margin: 10px;
                padding: 20px;
            }
            
            .header {
                font-size: 2em;
            }
            
            .couple-photos {
                flex-direction: column;
                gap: 20px;
            }
            
            .photo {
                width: 140px;
                height: 180px;
            }
            
            .timeline-photos {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }
            
            .timeline-photo {
                width: 150px;
                height: 150px;
            }
            
            .address-section {
                flex-direction: column;
                gap: 15px;
            }
            
            .address-item {
                margin-bottom: 10px;
            }
            
            .rsvp-section {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="invitation">
        <div class="decorative-elements">
            <div class="flower">🌸</div>
            <div class="flower">🌺</div>
            <div class="flower">🌼</div>
            <div class="flower">🌻</div>
        </div>
        
        <div class="header">Наша свадьба</div>
        
        <div class="dear">
            Дорогой <span class="name-line">
                <span class="name-on-line">Имя гостя</span>
            </span>
        </div>
        
        <div class="invitation-text">
            Приглашаем тебя на наш праздник!
        </div>
        
        <div class="event-details">
            <div class="date-time">
                <div class="date">15.08.2025</div>
                <div class="time-venue">
                    <div class="time">17:00</div>
                    <div class="venue">Усадьба<br>"Романтика"</div>
                </div>
            </div>
            
            <div class="ceremony-label">Роспись</div>
            <div class="ceremony-time">18:00</div>
        </div>
        
        <div class="timeline">
            <div class="timeline-title">📅 Программа дня</div>
            
            <div class="timeline-item">
                <div class="timeline-event">ЗАГС</div>
                <div class="timeline-time">17:00</div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-event">Поездка</div>
                <div class="timeline-time">18:00</div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-event">Ресторан</div>
                <div class="timeline-time">19:00</div>
            </div>
            
            <div class="timeline-item">
                <div class="timeline-event">Салют</div>
                <div class="timeline-time">23:00</div>
            </div>
            
            <div class="timeline-photos">
                <div class="timeline-photo">
                    <div style="color: rgba(255,255,255,0.8);">Фото места</div>
                </div>
                <div class="timeline-photo">
                    <div style="color: rgba(255,255,255,0.8);">Фото места</div>
                </div>
            </div>
        </div>
        
        <div class="notes">
            <div class="note-item">1. Не дарите нам цветы, мы не успеем насладиться их красотой</div>
            <div class="note-item">2. Вместо букетов будем рады принять от вас в подарок любой сертификат или алкоголь</div>
        </div>
        
        <div class="couple-photos">
            <div class="photo-container">
                <div class="name-tag">ЖЕНИХ</div>
                <div class="photo">
                    <div style="color: rgba(255,255,255,0.8);">Фото жениха</div>
                </div>
            </div>
            
            <div class="photo-container">
                <div class="name-tag">НЕВЕСТА</div>
                <div class="photo">
                    <div style="color: rgba(255,255,255,0.8);">Фото невесты</div>
                </div>
            </div>
        </div>
        
        <div class="love-equation">
            Имя + Имя = <span class="heart">💕</span>
        </div>
        
        <div class="rsvp-section">
            <div class="rsvp-title">
                💌 Подтверждение присутствия
            </div>
            
            <div class="rsvp-description">
                Нажмите на кнопку ниже, чтобы подтвердить свое присутствие на нашей свадьбе. 
                Форма откроется в новом окне - это быстро и удобно!
            </div>
            
            <a href="https://forms.gle/wzuxhnMC2S4cM7wm9" 
               target="_blank" 
               class="rsvp-button">
                💕 Подтвердить присутствие
            </a>
        </div>
        
        <div class="footer-addresses">
            <div class="addresses-title">
                📍 Адреса проведения
            </div>
            
            <div class="address-section">
                <div class="address-item">
                    <div class="address-label">
                        🏛️ ЗАГС
                    </div>
                    <div class="address-text">
                        ул. Примерная, 123<br>
                        г. Город, Область
                    </div>
                    <div class="address-time">17:00</div>
                </div>
                
                <div class="address-item">
                    <div class="address-label">
                        🏰 Ресторан
                    </div>
                    <div class="address-text">
                        Усадьба "Романтика"<br>
                        ул. Красивая, 456<br>
                        г. Город, Область
                    </div>
                    <div class="address-time">19:00</div>
                </div>
            </div>
            
            <div class="address-section">
                <div class="address-item">
                    <div class="address-label">
                        📞 Контакты
                    </div>
                    <div class="address-text">
                        +7 (XXX) XXX-XX-XX<br>
                        организатор@свадьба.рф
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
