<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>1 BAC CRONO</title>
    <style>
        body {
            background-color: #f1f1f1;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .countdown {
            text-align: center;
        }

        .countdown-label {
            font-size: 24px;
            color: #333;
            margin-bottom: 10px;
        }

        .countdown-timer {
            font-size: 36px;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .countdown-timer span {
            width: 50px;
            height: 50px;
            background-color: #fff;
            border-radius: 5px;
            border: 2px solid #ccc;
            margin: 0 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
        }
        #footer {
                margin-top: 800px;
                margin-left: -300px ;
                color: #1e1e1e;
        }
    </style>
</head>
<body>
    <div class="countdown">
        <div class="countdown-label">1 BAC CRONO :</div>
        <div class="countdown-timer">
            <span class="days">00</span> :
            <span class="hours">00</span> :
            <span class="minutes">00</span> :
            <span class="seconds">00</span>
        </div>
    </div>
    <script>
        // The date  of Jihawi hh :):
        var endDate = new Date("June 6, 2024 00:00:00").getTime();

        var x = setInterval(function() {
            var now = new Date().getTime();
            var distance = endDate - now;

            var days = Math.floor(distance / (1000 * 60 * 60 * 24));
            var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.querySelector(".days").innerHTML = formatTime(days);
            document.querySelector(".hours").innerHTML = formatTime(hours);
            document.querySelector(".minutes").innerHTML = formatTime(minutes);
            document.querySelector(".seconds").innerHTML = formatTime(seconds);

            if (distance < 0) {
                clearInterval(x);
                document.querySelector(".countdown-timer").innerHTML = "<h1>3la slamtk</h1>";
            }
        }, 1000);

        function formatTime(time) {
            return time < 10 ? "0" + time : time;
        }
    </script>
  
</body>


<footer>
    <h3  id="footer" style="text-align:center; font-family:Arial, sans-serif;">Powered by Zakaria Erradi</h3>
</footer>
</html>
