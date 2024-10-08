شركة I.M.A للبرمجيات
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>شركة I.M.A - المستقبل في برمجة الذكاء الصناعي</title>
    <style>
        body {
            font-family: 'Cairo', sans-serif;
            direction: rtl;
            text-align: right;
            margin: 0;
            padding: 0;
            background: linear-gradient(120deg, #4f4cfc, #00a2ff);
            color: #ffffff;
            overflow-x: hidden;
        }
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');
        .container {
            width: 90%;
            margin: 20px auto;
            background-color: rgba(255, 255, 255, 0.1);
            box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.3);
            padding: 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            animation: fadeIn 1.5s ease-in-out;
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        .header {
            text-align: center;
            margin-bottom: 20px;
            position: relative;
        }
        .header img {
            max-width: 60%;
            height: auto;
            border-radius: 20px;
            box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.5s;
        }
        .header img:hover {
            transform: rotateY(360deg);
        }
        h1 {
            color: #f4f4f4;
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.4);
        }
        ul {
            list-style: none;
            padding: 0;
            font-size: 1.2em;
        }
        ul li {
            padding: 15px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            animation: fadeUp 2s ease-in-out;
        }
        ul li::before {
            content: '•';
            color: #ff9800;
            font-size: 1.5em;
            position: absolute;
            left: -25px;
            top: 10px;
            animation: bounceIn 2s infinite;
        }
        .contact {
            margin-top: 20px;
            background-color: rgba(0, 0, 0, 0.2);
            padding: 20px;
            border-radius: 10px;
            backdrop-filter: blur(5px);
            animation: slideIn 2s ease-in-out;
        }
        .contact a {
            color: #ffc107;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }
        .contact a:hover {
            color: #ff5722;
            text-decoration: underline;
        }
        @keyframes fadeUp {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        @keyframes bounceIn {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-15px);
            }
            60% {
                transform: translateY(-7px);
            }
        }
        @keyframes slideIn {
            from {
                transform: translateX(-100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }
        canvas {
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;
        }
    </style>
</head>
<body>
    <canvas id="bg"></canvas>
    <div class="container">
        <div class="header">
            <img src="https://i.postimg.cc/zy5L5z8J/IMA-Service-Image.jpg" alt="I.M.A Services">
            <h1>شركة I.M.A - المستقبل في برمجة الذكاء الصناعي</h1>
        </div>
        <ul>
            <li>خبرة واسعة في صناعة تطبيقات Google المتميزة وتصميم صفحات ويب مبتكرة، بالإضافة إلى البرمجة باستخدام Unity لإنشاء ألعاب وتطبيقات تفاعلية.</li>
            <li>نقدم لك خدمة كتابة الأكواد البرمجية بجودة عالية واحترافية في مختلف لغات البرمجة لتلبية احتياجاتك البرمجية بشكل كامل، سواء كنت تبحث عن تطوير تطبيقات، مواقع ويب، أو حلول برمجية متقدمة.
                <br>لغات البرمجة الأمامية: HTML, CSS, JavaScript
                <br>لغات البرمجة الخلفية: PHP, Python, Ruby, Java, C#
                <br>تطوير تطبيقات الجوال: Swift (iOS), Kotlin (Android), Flutter, React Native
                <br>برمجة الألعاب: C++, C#, Unity
            </li>
            <li>إنشاء رسائل ماجستير ودكتوراه. دعم أكاديمي كامل من إعداد الرسائل البحثية حتى تقديمها بالشكل المثالي، مع الالتزام بأعلى معايير الجودة والدقة العلمية.</li>
            <li>إنشاء أبحاث جامعية. مساعدة شاملة في إعداد الأبحاث الجامعية، من جمع المعلومات إلى التحليل وكتابة البحث بأسلوب أكاديمي مميز.</li>
            <li>تصميم فيديوهات احترافية. تحويل أفكارك إلى فيديوهات مبدعة ومؤثرة باستخدام أحدث تقنيات التصميم والمونتاج.</li>
        </ul>
        <div class="contact">
            <p>خدمة مباشرة على مدار الساعة 24 ساعه أونلاين.<br>
            للتواصل: واتساب أو اتصال مباشر: <a href="tel:+962797988270">+962797988270</a></p>
        </div>
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // Background 3D animation
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({canvas: document.getElementById('bg'), alpha: true});
        renderer.setSize(window.innerWidth, window.innerHeight);
        document.body.appendChild(renderer.domElement);

        // Create a Torus geometry
        const geometry = new THREE.TorusGeometry(10, 3, 16, 100);
        const material = new THREE.MeshBasicMaterial({color: 0x00ff00, wireframe: true});
        const torus = new THREE.Mesh(geometry, material);
        scene.add(torus);

        camera.position.z = 50;

        function animate() {
            requestAnimationFrame(animate);

            torus.rotation.x += 0.01;
            torus.rotation.y += 0.01;

            renderer.render(scene, camera);
        }

        animate();

        window.addEventListener('resize', () => {
            renderer.setSize(window.innerWidth, window.innerHeight);
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
        });
    </script>
</body>
</html>
