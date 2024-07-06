<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>השלישי המלאכותי - מדריך למשתמש המתחיל</title>
    <style>
        /* הסגנונות נשארים זהים לגרסה הקודמת */
        body, html {
            height: 100%;
            margin: 0;
            font-family: 'Heebo', sans-serif;
            background-color: #f0f8ff;
            color: #333;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        h1 {
            color: #2c3e50;
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        h2 {
            color: #34495e;
            font-size: 1.8em;
            margin-bottom: 10px;
        }
        h3 {
            color: #2980b9;
            font-size: 1.5em;
            margin-bottom: 20px;
        }
        .button-bar {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 40px;
        }
        .button {
            padding: 15px 25px;
            font-size: 18px;
            cursor: pointer;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 50px;
            transition: all 0.3s;
            flex: 1;
            min-width: 200px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .button:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 6px 8px rgba(0,0,0,0.15);
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 30px;
            border: 1px solid #888;
            width: 90%;
            max-width: 800px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .close {
            color: #aaa;
            float: left;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover {
            color: #000;
        }
        .author {
            text-align: center;
            margin-top: 40px;
            color: #34495e;
        }
        .thanks {
            text-align: center;
            color: #7f8c8d;
            font-style: italic;
            margin-top: 10px;
        }
        .example {
            background-color: #ecf0f1;
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
        }
        .good-example {
            border-left: 5px solid #2ecc71;
        }
        .bad-example {
            border-left: 5px solid #e74c3c;
        }
        @media (max-width: 768px) {
            .button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>השלישי המלאכותי</h1>
            <h2>מדריך למשתמש המתחיל</h2>
            <h3>כיצד לדבר עם מודלי שפה גדולים?</h3>
        </div>
        
        <div class="button-bar">
            <button class="button" onclick="openModal('modal1')">כתבו הוראות ברורות</button>
            <button class="button" onclick="openModal('modal2')">בנו פרומפט מסודר</button>
            <button class="button" onclick="openModal('modal3')">נהלו שיחה</button>
            <button class="button" onclick="openModal('modal4')">צמצמו הזיות</button>
        </div>

        <div id="modal1" class="modal">
            <div class="modal-content">
                <span class="close" onclick="closeModal('modal1')">&times;</span>
                <h2>כתבו הוראות ברורות</h2>
                <p>הגדירו במדויק את הציפיות שלכם מהמודל:</p>
                <ul>
                    <li>ציינו במפורש: נושא, הקשר, פורמט, אורך וסגנון</li>
                    <li>תנו דוגמאות למענה טוב</li>
                    <li>הימנעו מתשובות כלליות</li>
                </ul>
                <div class="example bad-example">
                    <h3>דוגמה להוראה לא טובה:</h3>
                    <p>"דבר על דיכאון."</p>
                </div>
                <div class="example good-example">
                    <h3>דוגמה להוראה טובה:</h3>
                    <p>"כתוב סיכום של 200 מילים על הקשר בין דיכאון לביצועים אקדמיים בקרב סטודנטים לתואר ראשון. כלול לפחות שלוש השפעות ספציפיות ושתי אסטרטגיות התמודדות מומלצות."</p>
                </div>
            </div>
        </div>

        <div id="modal2" class="modal">
            <div class="modal-content">
                <span class="close" onclick="closeModal('modal2')">&times;</span>
                <h2>בנו פרומפט מסודר</h2>
                <p>ארגנו את הפרומפט שלכם באופן לוגי:</p>
                <ol>
                    <li>התחילו בהוראות כלליות (עובדות, נתונים ראשוניים)</li>
                    <li>עברו לפרטים ולסגנון המענה הרצוי</li>
                    <li>סיימו עם סיכום ונקודות מפתח</li>
                </ol>
                <div class="example bad-example">
                    <h3>דוגמה לפרומפט לא מסודר:</h3>
                    <p>"תן לי מידע על ADHD ואיך לטפל בו ומה ההשפעות שלו על ילדים ומבוגרים."</p>
                </div>
                <div class="example good-example">
                    <h3>דוגמה לפרומפט מסודר:</h3>
                    <p>"1. הגדר ADHD והסבר את הסימפטומים העיקריים.<br>
                    2. תאר את ההבדלים בביטוי ADHD בין ילדים למבוגרים.<br>
                    3. פרט 3 שיטות טיפול מקובלות, כולל יתרונות וחסרונות.<br>
                    4. סכם את ההשפעות העיקריות של ADHD על חיי היומיום.<br>
                    הצג את המידע בפורמט של נקודות עם כותרות משנה ברורות."</p>
                </div>
            </div>
        </div>

        <div id="modal3" class="modal">
            <div class="modal-content">
                <span class="close" onclick="closeModal('modal3')">&times;</span>
                <h2>נהלו שיחה</h2>
                <p>התייחסו לתהליך כאל דיאלוג מתמשך:</p>
                <ul>
                    <li>חזרו, שנו, ודייקו את השאלות שלכם</li>
                    <li>בקשו הבהרות ותובנות נוספות</li>
                    <li>התייחסו לתשובות קודמות</li>
                </ul>
                <div class="example bad-example">
                    <h3>דוגמה לשיחה לא טובה:</h3>
                    <p>"מה זה CBT? איך זה עובד על חרדה? תן לי טכניקות."</p>
                </div>
                <div class="example good-example">
                    <h3>דוגמה לשיחה טובה:</h3>
                    <p>"1. הסבר בקצרה מהו טיפול קוגניטיבי-התנהגותי (CBT).<br>
                    2. כיצד CBT מיושם בטיפול בהפרעות חרדה?<br>
                    3. תן דוגמה לטכניקה ספציפית ב-CBT לטיפול בחרדה חברתית.<br>
                    4. [לאחר קבלת תשובה] תודה על ההסבר. האם תוכל להרחיב על אתגרים נפוצים ביישום טכניקה זו?"</p>
                </div>
            </div>
        </div>

        <div id="modal4" class="modal">
            <div class="modal-content">
                <span class="close" onclick="closeModal('modal4')">&times;</span>
                <h2>צמצמו הזיות</h2>
                <p>הגבילו את המרחב ליצירת מידע שגוי:</p>
                <ul>
                    <li>בקשו מהמודל לציין מקורות מידע</li>
                    <li>הגבילו את התשובה לעובדות מבוססות</li>
                    <li>בקשו מהמודל לציין כאשר הוא לא בטוח במידע</li>
                </ul>
                <div class="example bad-example">
                    <h3>דוגמה להוראה שעלולה לגרום להזיות:</h3>
                    <p>"ספר לי על כל הטיפולים האפשריים לדיכאון."</p>
                </div>
                <div class="example good-example">
                    <h3>דוגמה להוראה שמצמצמת הזיות:</h3>
                    <p>"תאר את שלושת הטיפולים המבוססי-ראיות המובילים לדיכאון קליני בהתבסס על מחקרים שפורסמו ב-5 השנים האחרונות. ציין את שמות החוקרים והשנה עבור כל טיפול. אם אינך בטוח לגבי מידע מסוים, ציין זאת במפורש."</p>
                </div>
            </div>
        </div>

        <div class="author">
            <p>יובל הבר, פסיכולוג חינוכי מומחה, מייסד ומנהל השלישי המלאכותי</p>
        </div>
        <div class="thanks">
            <p>תודות לאורי פן, מנהל מוצר בתחום הבינה המלאכותית במייקרוסופט ושותף לצוות מחקר ופיתוח בשלישי המלאכותי</p>
        </div>
    </div>

    <script>
        function openModal(modalId) {
            document.getElementById(modalId).style.display = "block";
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = "none";
        }

        window.onclick = function(event) {
            if (event.target.classList.contains("modal")) {
                event.target.style.display = "none";
            }
        }
    </script>
</body>
</html>
