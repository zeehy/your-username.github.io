# zeehy78.github.io
<!DOCTYPE html>
<html>
<head>
    <title>예약 페이지</title>
    <style>
        body {
            font-family: '맑은 고딕', Arial, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(to bottom, #FFF9E0 0%, #FFEE58 100%);
        }
        h1 {
            text-align: center;
            padding: 20px 0;
            color: #575757;
        }
        form {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        label {
            font-weight: bold;
            color: #575757;
        }
        input[type="text"],
        input[type="date"],
        input[type="number"],
        select {
            width: 100%;
            padding: 6px;
            margin: 6px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        input[type="submit"] {
            width: 100%;
            background-color: #FFD700;
            color: #575757;
            padding: 14px 20px;
            margin: 8px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            cursor: pointer;
            font-weight: bold;
        }
        input[type="submit"]:hover {
            background-color: #FFC72C;
        }
        .phone-section {
            display: flex;
            justify-content: space-between;
        }
        .phone-section input[type="text"] {
            width: calc((100% - 6% * 2) / 3);
        }
        p {
            color: #575757;
        }
    </style>

<script>
    function showMessage() {
        alert("예약이 완료되었습니다!\n추가적인 내용은 문자로 발송드리겠습니다.");
    }
</script>

</head>
<body>
    <h1>⚾️ 예약 페이지 ⚾️</h1>
    <form onsubmit="event.preventDefault(); showMessage();">
        <!-- 야구장 선택 -->
        <label for="stadium-select">야구장 선택:</label>
        <select id="stadium-select" name="stadium">
            <option value="stadium1">삼락생태공원 - 야구장(유소년)(하절기)</option>
            <option value="stadium2">삼락생태공원 - 야구장(유소년)(동절기)</option>
            <option value="stadium3">화명생태공원 - 야구장(유소년)(하절기)</option>
            <option value="stadium4">낙동강관리본부 야구장(평일)(하절기)</option>
            <option value="stadium5">낙동강관리본부 야구장(평일)(동절기)</option>


            <!-- (추가적인 야구장 옵션들) -->
        </select>
        <br><br>

        <!-- 예약자 이름 -->
        <label             for="reservation-name">예약자 이름*</label>
        <input type="text" id="reservation-name" name="reservation-name" placeholder="예약자 이름 입력" required>
        <br><br>

        <!-- 날짜 선택 -->
        <label for="reservation-date">예약 날짜*</label>
        <input type="date" id="reservation-date" name="reservation-date" required>
        <br><br>

        <!-- 시간 선택 -->
        <label for="reservation-time">예약 시간*</label>
        <input type="text" id="reservation-time" name="reservation-time" placeholder="예: 13:00-15:00" required>
        <br><br>

        <!-- 전화번호 입력 -->
        <label for="phone-number">전화번호*</label>
        <div class="phone-section">
            <input type="text" id="phone-number1" name="phone-number1" placeholder="예: 010" required>
            <input type="text" id="phone-number2" name="phone-number2" placeholder="예: 1234" required>
            <input type="text" id="phone-number3" name="phone-number3" placeholder="예: 5678" required>
        </div>
        <br><br>

        <!-- 비고 -->
        <label for="remarks">비고</label>
        <input type="text" id="remarks" name="remarks" placeholder="예: 볼이나 배트가 필요합니다.">
        <br><br>

        <!-- 예약 완료 버튼 -->
        <input type="submit" value="예약 완료">
        <br><br>
    </form>
</body>
</html>
