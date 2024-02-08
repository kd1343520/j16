<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        button {
            padding: 10px;
            font-size: 16px;
            margin: 5px;
            background-color: transparent; /* 透明にする */
            border: none; /* ボーダーをなくす */
        }
        img {
            display: none;
        }
    </style>
    <script>
        let currentImageIndex = 0;

        function showImage() {
            const images = document.querySelectorAll('img');
            if (currentImageIndex < images.length) {
                images[currentImageIndex].style.display = 'block';
                currentImageIndex++;
            } else {
                alert('すべての画像を表示しました。');
            }
        }

        function clearImages() {
            const images = document.querySelectorAll('img');
            images.forEach(image => {
                image.style.display = 'none';
            });
            currentImageIndex = 0;
            alert('クリア！');
        }
    </script>
</head>
<body>
    <button onclick="showImage()">次の画像</button>
    <button onclick="clearImages()">クリア</button>

    <img src="j16/..images/image1.j16" alt="Image1">
    <img src="j16/..images/image2.j16" alt="Image2">
    <img src="j16/..images/image3.j16" alt="Image3">
