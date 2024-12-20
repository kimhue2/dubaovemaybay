﻿# dubaovemaybay
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dự báo giá vé máy bay</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Quicksand:wght@300;500&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f8fa;
        }

        header {
            background-color: #4e73df;
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom: 5px solid #2e59d9;
        }

        header h1 {
            margin: 0;
            font-size: 26px;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #3b4c78;
            padding: 12px 20px;
        }

        .menu a {
            color: white;
            text-decoration: none;
            margin-right: 20px;
            font-size: 16px;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .menu a:hover {
            color: #f39c12;
        }

        .search input {
            padding: 8px;
            font-size: 16px;
            border: 1px solid #bdc3c7;
            border-radius: 4px;
            margin-right: 10px;
        }

        .search button {
            background-color: #f39c12;
            color: white;
            padding: 8px 14px;
            font-size: 16px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .search button:hover {
            background-color: #e67e22;
        }

        .container {
            max-width: 850px;
            margin: 30px auto;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
            padding: 30px;
        }

        .input-section, .output-section {
            margin-bottom: 25px;
        }

        .input-section h2, .output-section h2 {
            font-size: 22px;
            color: #333;
            margin-bottom: 20px;
            font-weight: 600;
        }

        label {
            display: block;
            margin-bottom: 6px;
            font-weight: 500;
        }

        input, select, button {
            width: 100%;
            padding: 12px;
            margin-bottom: 18px;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 16px;
        }

        .radio-group {
            display: flex;
            gap: 15px;
            margin-bottom: 18px;
        }

        .radio-group label {
            font-weight: 500;
        }

        .highlight {
            font-size: 24px;
            font-weight: 700;
            color: #4e73df;
        }

        .output-section {
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 25px;
        }

        button {
            background-color: #4e73df;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
        }

        button:hover {
            background-color: #2e59d9;
        }

        footer {
            background-color: #2e59d9;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .social-icons i {
            margin: 0 10px;
            font-size: 24px;
            cursor: pointer;
            color: white;
            transition: color 0.3s ease;
        }

        .social-icons i:hover {
            color: #f39c12;
        }

    </style>
</head>
<body>
    <header>
        <h1>Dự báo giá vé máy bay</h1>
    </header>
    <nav>
        <div class="menu">
            <a href="#">Trang chủ</a>
            <a href="#">Nhập dữ liệu</a>
            <a href="#">Kết quả dự báo</a>
            <a href="#">Trợ giúp</a>
        </div>
        <div class="search">
            <input type="text" placeholder="Tìm kiếm...">
            <button>Tìm</button>
        </div>
    </nav>

    <div class="container">
        <div class="input-section">
            <h2>Nhập thông tin chuyến bay của bạn</h2>

            <label for="destination">Điểm đến:</label>
            <select id="destination">
                <option value="Bangalore">Bangalore</option>
                <option value="Cochin">Cochin</option>
                <option value="Delhi">Delhi</option>
                <option value="Hyderabad">Hyderabad</option>
                <option value="Kolkata">Kolkata</option>
                <option value="New Delhi">New Delhi</option>
            </select>

            <label for="date">Ngày xuất phát:</label>
            <input type="date" id="date">

            <label for="return-date">Ngày trở về:</label>
            <input type="date" id="return-date">

            <label for="time">Thời gian bay:</label>
            <select id="time">
                <option value="morning">Sáng</option>
                <option value="afternoon">Chiều</option>
                <option value="evening">Tối</option>
                <option value="night">Đêm</option>
            </select>

            <label>Khoảng cách:</label>
            <div class="radio-group">
                <label><input type="radio" name="distance" value="800" checked> 800</label>
                <label><input type="radio" name="distance" value="1000"> 1000</label>
                <label><input type="radio" name="distance" value="1500"> 1500</label>
                <label><input type="radio" name="distance" value="1800"> 1800</label>
                <label><input type="radio" name="distance" value="2150"> 2150</label>
                <label><input type="radio" name="distance" value="2500"> 2500</label>
                <label><input type="radio" name="distance" value="2850"> 2850</label>
                <label><input type="radio" name="distance" value="3200"> 3200</label>
                <label><input type="radio" name="distance" value="3550"> 3550</label>
            </div>

            <label for="airline">Hãng hàng không:</label>
            <select id="airline">
                <option value="AirAsia">Air Asia</option>
                <option value="AirIndia">Air India</option>
                <option value="GoAir">GoAir</option>
                <option value="IndiGo">IndiGo</option>
                <option value="JetAirways">Jet Airways</option>
                <option value="JetAirwaysBusiness">Jet Airways Business</option>
                <option value="SpiceJet">SpiceJet</option>
                <option value="Trujet">Trujet</option>
                <option value="Vistara">Vistara</option>
                <option value="VistaraPremium">Vistara Premium Economy</option>
            </select>

            <label for="passengers">Số lượng hành khách:</label>
            <input type="number" id="passengers" min="1" value="1">

            <button onclick="predictPrice()">Dự báo giá vé</button>
        </div>

        <!-- Output Section -->
        <div class="output-section">
            <h2>Kết quả dự báo</h2>
            <p>Giá vé dự báo: <span class="highlight" id="predicted-price">--</span></p>
            <p>Giá cao nhất có thể: <span id="max-price">--</span></p>
            <p>Giá thấp nhất có thể: <span id="min-price">--</span></p>
        </div>
        <script>
            function predictPrice() {
                // Dummy data for testing
                const predictedPrice = 2500000;
                const maxPrice = 5000000;
                const minPrice = 1800000;
    
                document.getElementById('predicted-price').innerText = `${predictedPrice.toLocaleString()} VNĐ`;
                document.getElementById('max-price').innerText = `${maxPrice.toLocaleString()} VNĐ`;
                document.getElementById('min-price').innerText = `${minPrice.toLocaleString()} VNĐ`;
            }
        </script>
    </div>
    <footer>
        <p>&copy; 2024 Dự báo giá vé máy bay. Tất cả các quyền được bảo lưu.</p>
        <footer class="bg-main">
            <div class="social-icons">
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-facebook-official"></i></a>
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-instagram"></i></a>
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-snapchat"></i></a>
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-pinterest"></i></a>
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-twitter"></i></a>
                <a href="#" class="social-icon" target="_blank"><i class="fa fa-linkedin"></i></a>
            </div>
        </footer>
        
        <style>
            /* Tổng thể footer */
            .bg-main {
                color: white;
                padding: 20px;
                text-align: center;
                position: relative;
            }
        
            /* Chỉnh sửa các biểu tượng mạng xã hội */
            .social-icons {
                margin-top: 10px;
                display: flex;
                justify-content: center;
                gap: 15px; /* Khoảng cách giữa các icon */
            }
        
            .social-icon {
                color: white;
                font-size: 24px;
                text-decoration: none;
                transition: color 0.3s ease;
            }
        
            .social-icon:hover {
                color: #3498db; /* Màu khi di chuột vào */
            }
        </style>
        
        <!-- Thêm liên kết Font Awesome nếu chưa có -->
        <head>
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
        </head>
        
    </footer>
    </body>
    </html>
