<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="cache-control" content="no-cache">
    <meta http-equiv="expires" content="0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@900&family=Russo+One&display=swap" rel="stylesheet">

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-0evHe/X+R7YkIZDRvuzKMRqM+OrBnVFBL6DOitfPri4tjfHxaWutUpFmBp4vmVor" crossorigin="anonymous">

    <link rel="stylesheet" href="css/style.css">
    <title>Wildberries всё для старта!</title>
    <link rel="icon" href="img/favicon.ico" type="image/vnd.microsoft.icon">
</head>

<body>
    <header class="header">
        <div class="container">
            <div class="row">
                <div class="col-12 justify-content-center">
                    <h1 class="jid-toptitle text-center text-white text-uppercase mt-5 mb-5">Wildberries - всё для
                        старта!</h1>
                </div>
                <div class="col-lg-2 col-md-0"></div>
                <div class="col-lg-8 col-md-12 mt-5">
                    <div class="embed-container">
                        <iframe src='https://www.youtube.com/embed//9iABZQgWj1k' frameborder='0'
                            allowfullscreen></iframe>
                    </div>
                </div>
                <div class="col-lg-2 col-md-0"></div>
            </div>
            <div class="row">
                <div class="col-12 d-flex justify-content-center mt-5">
                    <a class="jid-btn btn btn-lg btn-dark mt-5" href="#why" role="button">Записаться</a>
                </div>
            </div>
        </div>
    </header>
    <section class="run-text mb-5">
        <div class="container">
            <div class="row">
                <div class="col-12 overflow-hidden">
                    <div class="text-window">БЕЗ ВОДЫ | ПРОСТЫМИ СЛОВАМИ | АКТУАЛЬНАЯ ИНФОРМАЦИЯ | СТРИМЫ</div>
                </div>
            </div>
        </div>
    </section>
    <section class="ladder">
        <div class="container">
            <div class="row justify-content-center">
                <div class="ladder-item text-center fs-2 fading">Аналитика и поиск товара</div>
            </div>
            <div class="row justify-content-center">
                <div class="ladder-item text-center fs-2 fading">Подводные камни WB</div>
            </div>
            <div class="row justify-content-center">
                <div class="ladder-item text-center fs-2 fading">Оформление карточки товара</div>
            </div>
            <div class="row justify-content-center">
                <div class="ladder-item text-center fs-2 fading">Работа с региона</div>
            </div>
            <div class="row justify-content-center">
                <div class="ladder-item text-center fs-2 fading">Продвижение</div>
            </div>
        </div>
    </section>
    <section class="footer mb-5">
        <div class="container">
            <div class="row">
                <div class="d-flex justify-content-center col-12">
                    <div class="buy-form">
                        <a name="why"></a>
                        <form method="POST" action="https://yoomoney.ru/quickpay/confirm.xml"> 
                            <input type="hidden" name="receiver" value="410011106317851"> 
                            <input type="hidden" name="formcomment" value="Курс Wildberries"> 
                            <input type="hidden" name="short-dest" value="Курс Wildberries">
                            <input type="hidden" name="label" value="$order_id">
                            <input type="hidden" name="quickpay-form" value="donate">
                            <input type="hidden" name="targets" value="транзакция {order_id}">
                            <input type="hidden" name="sum" value="800" data-type="number">
                            <div class="form-floating mb-3">
                                <input name="need-fio" type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                                <label for="floatingInput">Имя</label>
                            </div> 

                            <div class="form-floating mb-3">
                                <input name="need-email" type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                                <label for="floatingInput" class="form-label mb-2">Адрес электронной почты</label>
                                <div id="emailHelp" class="form-text mb-3 text-black">На почту придет ссылка для вступления закрытый телеграм канал.</div>
                            </div>
                            <input type="hidden" name="need-phone" value="false">
                            <input type="hidden" name="need-address" value="false"> 
                            <input type="hidden" name="paymentType" value="AC">
                            <div class="d-flex justify-content-center">
                                <input type="submit" value="Записаться" class="buy-btn jid-btn btn btn-primary">
                            </div>
                        </form>

                    </div>
                </div>
            </div>
            <div class="row mt-5">
                <div class="d-flex justify-content-center col-12">
                    <h3 class="buy-form__timer text-white"></h3>
                </div>
            </div>
        </div>
    </section>
    <script>
        function getNoun(number, one, two, five) {
            let n = Math.abs(number);
            n %= 100;
            if (n >= 5 && n <= 20) {
                return five;
            }
            n %= 10;
            if (n === 1) {
                return one;
            }
            if (n >= 2 && n <= 4) {
                return two;
            }
            return five;
        }
        function timer() {
            let doc = document.querySelector('.buy-form__timer');
            let timeNow = new Date();
            let timeEnd = new Date(2022, 6, 26);
            let result = timeEnd - timeNow;
            if (result <= 0) {
                doc.innerHTML = 'КУРС УЖЕ ИДЁТ!';
            } else {
                let dateTo = Math.trunc(result / 1000 / 60 / 60 / 24);
                doc.innerHTML = `ДО НАЧАЛА: ${dateTo} ${getNoun(dateTo, 'ДЕНЬ', 'ДНЯ', 'ДНЕЙ')}`;
            }
        }
        timer();
    </script>
    <!-- Fading -->
    <script>
        let fadingHeading = document.querySelectorAll('.fading');
        for (let a = 0; a < fadingHeading.length; a++){
            let letters = fadingHeading[a].textContent.split('');
            let content = letters.map((val, i) => {
                let delay = Math.floor((Math.random() * 1000) + 1);
                return ('<span style="animation-delay: '+ delay + 'ms">'+ val +'</span>');
            });
            fadingHeading[a].innerHTML = "";
            for (let i = 0; i < content.length; i++) {
                fadingHeading[a].innerHTML += content[i];
            }
        }
    </script>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM"
        crossorigin="anonymous"></script>
</body>

</html>
