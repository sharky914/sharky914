<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>링크 선택기</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h1 {
            color: #333;
        }
        select, button {
            padding: 10px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <h1>링크 선택기</h1>
    <select id="linkSelect">
        <option value="">링크를 선택하세요</option>
        <option value="https://example1.com">예제 링크 1</option>
        <option value="https://example2.com">예제 링크 2</option>
        <option value="https://example3.com">예제 링크 3</option>
    </select>
    <button id="goButton">이동</button>

    <script>
        document.getElementById('goButton').addEventListener('click', function() {
            const select = document.getElementById('linkSelect');
            const url = select.value;

            if (url) {
                window.location.href = url; // 선택한 링크로 이동
            } else {
                alert('링크를 선택하세요!');
            }
        });
    </script>
</body>
</html>
