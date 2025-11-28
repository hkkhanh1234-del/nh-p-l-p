<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nhóm 4 - 12 Anh</title>

    <!-- Google font for aesthetic -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700;800&display=swap" rel="stylesheet">

    <style>
        :root {
            --primary: #f77f00;
            --primary-light: #ffb347;
            --bg: #0a1f2b;
            --card-bg: rgba(255,255,255,0.14);
            --text-dark: #ffffff;
            --text-light: rgba(255,255,255,0.85);
            --accent: #eae2b7;
            --radius: 18px;
            --shadow: 0 8px 32px rgba(0, 0, 0, 0.25);
        }

        body {
            font-family: "Poppins", "Segoe UI", sans-serif;
            margin: 0;
            background: url("beach.jpg"); /* Bạn có thể đổi thành link nếu muốn */
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            backdrop-filter: brightness(0.55) blur(2px);
            color: var(--text-dark);
        }

        /* Header */
        header {
            background: linear-gradient(180deg, rgba(0,36,50,0.8), rgba(5,90,120,0.45));
            text-align: center;
            padding: 60px 15px;
            box-shadow: var(--shadow);
            border-bottom: 3px solid rgba(247,127,0,0.5);
        }

        header h1 {
            margin: 0;
            font-size: 44px;
            font-weight: 800;
            text-shadow: 0 4px 18px rgba(0, 183, 255, 0.9), 0 0 12px rgba(255, 183, 72, 0.6);
        }
        header p {
            margin-top: 10px;
            font-size: 18px;
            color: var(--accent);
            font-weight: 500;
        }

        /* Navbar */
        .navbar {
            display: flex;
            justify-content: center;
            gap: 35px;
            font-size: 19px;
            margin-bottom: 20px;
        }
        .navbar a {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            position: relative;
        }
        .navbar a::after {
            content: "";
            position: absolute;
            width: 0%;
            height: 2px;
            background: var(--primary);
            left: 0;
            bottom: -5px;
            transition: 0.4s;
        }
        .navbar a:hover::after {
            width: 100%;
        }

        /* Container */
        .container {
            width: 85%;
            max-width: 1200px;
            margin: auto;
            padding: 40px 0;
        }

        /* Section title */
        .section-title {
            font-size: 32px;
            font-weight: 800;
            margin: 30px 0 18px 6px;
            color: var(--accent);
            text-shadow: 0 0 8px rgba(255, 180, 100, 0.7);
            border-left: 5px solid var(--primary);
            padding-left: 14px;
        }

        /* Box & Card */
        .box, .card {
            background: var(--card-bg);
            padding: 26px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            border: 1px solid rgba(255,255,255,0.25);
            margin-bottom: 28px;
            transition: 0.3s;
            backdrop-filter: blur(6px);
        }
        .box:hover, .card:hover {
            transform: translateY(-6px);
            box-shadow: 0 10px 40px rgba(255, 180, 80, 0.3);
        }

        /* Member list */
        .member {
            font-size: 20px;
            font-weight: 600;
            padding: 14px 0;
            border-bottom: 1px dashed rgba(255,255,255,0.25);
            color: var(--accent);
            text-shadow: 0 0 6px rgba(0,183,255,0.5);
        }
        .member:last-child { border-bottom: none; }

        /* Links in card */
        .card a {
            display: inline-block;
            margin-top: 14px;
            padding: 12px 20px;
            background: var(--primary);
            color: #0a1f2b;
            text-decoration: none;
            border-radius: 10px;
            font-weight: 700;
            box-shadow: 0 4px 14px rgba(247,127,0,0.6);
        }
        .card a:hover {
            background: var(--primary-light);
            box-shadow: 0 4px 20px rgba(255,180,80,0.9);
        }

        /* Balloon animation */
        @keyframes floatBalloon {
            0% {transform: translateY(15px); opacity: 0;}
            30% {opacity: 1;}
            100% {transform: translateY(-120px); opacity: 0;}
        }
        .balloon {
            position: fixed;
            bottom: -30px;
            width: 22px;
            height: 28px;
            background: var(--primary-light);
            border-radius: 50%;
            box-shadow: 0 2px 10px rgba(255,150,100,0.7);
            animation: floatBalloon 5s infinite ease-in;
            z-index: 999;
        }
        .balloon:nth-child(1){left:10%;animation-delay:0.6s;}
        .balloon:nth-child(2){left:25%;animation-delay:1.3s;}
        .balloon:nth-child(3){left:40%;animation-delay:0.3s;}
        .balloon:nth-child(4){left:55%;animation-delay:1.8s;}
        .balloon:nth-child(5){left:70%;animation-delay:0.9s;}
        .balloon:nth-child(6){left:85%;animation-delay:1.5s;}

        /* Footer */
        footer {
            background: rgba(0,20,30,0.35);
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            font-size: 14px;
            color: var(--accent);
            backdrop-filter: blur(8px);
        }

        /* Back button */
        #back-btn {
            display: block;
            width: max-content;
            margin: 45px auto 10px;
            padding: 14px 26px;
            background: var(--accent);
            color: var(--bg);
            border-radius: 12px;
            font-weight: 800;
            text-decoration: none;
            box-shadow: 0 4px 18px rgba(255,180,80,0.6);
            transition: 0.3s;
        }
        #back-btn:hover {
            transform: scale(1.08);
            background: #fff;
            box-shadow: 0 6px 24px rgba(255,220,150,0.8);
        }

    </style>
</head>

<body>

    <!-- Bóng bay -->
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>

    <header>
        <img src="logo.png" alt="Logo" style="width:90px;margin-bottom:10px;filter:drop-shadow(0 3px 4px rgba(0,0,0,0.2));">
        <nav class="navbar">
            <a href="#baitap">Bài tập</a>
            <a href="#thuyettrinh">Thuyết trình</a>
        </nav>
        <h1>Nhóm 4 – Lớp 12 Anh</h1>
        <p>Góc sáng tạo của học sinh yêu nghệ thuật & biển 🌅</p>
    </header>

    <div class="container">

        <div class="box">
            <h2 class="section-title">👋 Xin chào!</h2>
            <p>
                Mình là <strong>học sinh cấp 3 bình thường</strong>, thích <strong>khám phá những điều sáng tạo</strong>,
                <strong>học từ trải nghiệm</strong>, và đặc biệt <strong>yêu hoàng hôn trên biển</strong> —
                nơi truyền cảm hứng bất tận cho mình. Trang web này là nơi nhóm mình lưu lại bài tập &
                sản phẩm học tập theo cách <strong>nghệ thuật nhất có thể</strong> 🎨
            </p>
        </div>

        <h2 id="baitap" class="section-title">📚 Danh sách bài tập</h2>

        <div class="card">
            <h3><strong>Bài tập 1</strong></h3>
            <p>Mô tả: Tác phẩm học tập đầu tiên của nhóm 🌊</p>
            <a href="#" target="_blank">Xem bài làm</a>
        </div>

        <div class="card">
            <h3><strong>Bài tập 2</strong></h3>
            <p>Mô tả: Sản phẩm tiếp theo với tinh thần sáng tạo 🌅</p>
            <a href="#" target="_blank">Xem bài làm</a>
        </div>

        <h2 id="thuyettrinh" class="section-title">🎤 Bài thuyết trình</h2>

        <div class="card">
            <h3><strong>Chủ đề thuyết trình</strong>: Biển & cảm hứng sáng tạo</h3>
            <p>Mô tả: Bài trình bày được thiết kế theo phong cách nghệ thuật biển 🌴</p>
            <a href="#" target="_blank">Xem slide</a>
        </div>

    </div>

    <footer>
        © 2025 - Nhóm 4 | Lớp 12 Anh
        <a id="back-btn" href="../">← Quay lại trang chính</a>
    </footer>

</body>
</html>
