## Hi there 👋

<!--
**tridentglobalservices/TridentGlobalServices** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Compress your images online with our fully responsive image compression tool. Optimize images for web use with adjustable compression levels.">
    <meta name="keywords" content="image compression, optimize images, image optimizer, online image compressor">
    <meta name="author" content="Your Name">
    <title>Online Image Compression Tool</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }

        main {
            padding: 20px;
        }

        #compression-tool {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        #image-container {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
        }

        #image-container img {
            max-width: 45%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
    <!-- Google AdSense -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_AD_SENSE_ID" crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>Online Image Compression Tool</h1>
    </header>
    <main>
        <section id="ad-top">
            <!-- AdSense Ad Unit -->
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_AD_SENSE_ID"
                 data-ad-slot="1234567890"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </section>
        <section id="compression-tool">
            <input type="file" id="image-input" accept="image/*">
            <label for="compression-level">Compression Level:</label>
            <input type="range" id="compression-level" min="0" max="1" step="0.1" value="0.5">
            <span id="compression-value">0.5</span>
            <button id="compress-btn">Compress Image</button>
            <div id="image-container">
                <img id="original-image" src="#" alt="Original Image">
                <img id="compressed-image" src="#" alt="Compressed Image">
            </div>
        </section>
        <section id="ad-bottom">
            <!-- AdSense Ad Unit -->
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_AD_SENSE_ID"
                 data-ad-slot="0987654321"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Online Image Compression Tool. All rights reserved.</p>
    </footer>
    <script>
        document.getElementById('compression-level').addEventListener('input', function() {
            document.getElementById('compression-value').textContent = this.value;
        });

        document.getElementById('compress-btn').addEventListener('click', function() {
            const fileInput = document.getElementById('image-input');
            const compressionLevel = parseFloat(document.getElementById('compression-level').value);

            if (fileInput.files && fileInput.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = new Image();
                    img.src = e.target.result;

                    img.onload = function() {
                        const canvas = document.createElement('canvas');
                        const ctx = canvas.getContext('2d');
                        canvas.width = img.width;
                        canvas.height = img.height;
                        ctx.drawImage(img, 0, 0);

                        const compressedImage = canvas.toDataURL('image/jpeg', compressionLevel);
                        document.getElementById('compressed-image').src = compressedImage;
                    };
                };
                reader.readAsDataURL(fileInput.files[0]);
            }
        });
    </script>
</body>
</html>
