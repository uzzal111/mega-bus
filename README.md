# mega-bus
#live link:
https://uzzal111.github.io/mega-bus/index.html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bus Ticket</title>
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Roboto:wght@400;500;700&display=swap"
        rel="stylesheet">
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous">
    <!-- Stylesheet -->
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <!--Header and Menu Section-->
    <header class="container">
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About Us</a></li>
                <li><a href="#">Contact</a></li>
                <li><a class="active" href="#">Sign Up</a></li>
            </ul>
        </nav>
    </header>

    <!--Booking Section-->
    <main id="cart-view" class="main-content container">

        <div class="booking-content">
            <h1>Mega City Bus</h1>
            <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
        </div>


        <div class="booking-form">
            <h3>Explore By Bus</h3>

            <div class="inputs">
                <div class="input-group">
                    <label" for="">From</label>
                    <input class="inp-style" type="text" name="" placeholder="Dhaka">
                </div>
                <div class="input-group">
                    <label" for="">To</label>
                    <input class="inp-style" type="text" name="" placeholder="Chittagone">
                </div>
            </div>

            <div class="inputs">
                <div class="input-group">
                    <label" for="">Departure</label>
                    <input class="inp-style" type="date" name="">
                </div>
                <div class="input-group">
                    <label for="">Return</label>
                    <input class="inp-style" type="date" name="">
                </div>
            </div>
            <div class="inputs">
                <div class="input-group f-class">
                <div>
                    <label for="">First Class ($150) <h5 id="phone-total">$150</h5></label>
                    <input id="phone-count" class="inp-style inp-width"type="text" class="form-control text-center" value="1">
                </div>
                <div class="plus-minus-btn">
                    <p> <button id="phone-increse" class="btn btn-success"> +</button>
                        <button id="phone-decrse" class="btn btn-danger">- </button> </p>
                </div>
            </div>
                <div class="input-group f-class">
                    <div>
                        <label for="">Economy ($100)<h5 id="case-total">$100</h5></label>
                        <input id="case-count" class="inp-style inp-width" type="text" class="form-control text-center" value="1">
                    </div>
                    <div class="plus-minus-btn">
                        <p> <button> <span id="case-increse" class="btn btn-success">+</span></button>
                            <button><span id="case-decrse" class="btn btn-danger">-</span> </button> </p>
                    </div>
                </div>

            </div>
            <div class="calculations">
                <div class="amount">
                    <div class="left">
                        <p>Subtotal</p>
                    </div>
                    <div class="right">
                        <h5 id="total-price">$250</h5>
                    </div>
                </div>

                <div class="amount">
                    <div class="left">
                        <p>Charge 10% VAT</p>
                    </div>
                    <div class="right">
                        <h5 id="tax-total">$0</h5>
                    </div>
                </div>
                
                <hr>
                <div class="amount">
                    <div class="left">
                        <h4>Total</h4>
                    </div>
                    <div class="right">
                        <h5 id="sub-total">$300</h5>
                    </div>
                </div>
            </div>
            <button id="booknow" class="btn-style">Book Now</button>
        </div>
    </main>

    <section id="user-detail">
        <div class="container">
           <div class="row">
              <div class="col-md-12 my-5 form">
                 <input type="text" name="" id="" class="form-control my-3" placeholder="First Name"><br>
                 <input type="text" name="" id="" class="form-control mb-3" placeholder="Last Name"> <br>
                 <input type="email" name="" id="" class="form-control mb-3" placeholder="Email"><br>
                 <input type="text" name="" id="" class="form-control mb-3" placeholder="Phone No"><br>
                 <input type="text" name="" id="" class="form-control mb-3" placeholder="Address"><br>
                 <button class="btn btn-success mb-3">Submit</button>
              </div>
           </div>
        </div>
     </section>
    <script>
        
        document.getElementById('phone-increse').addEventListener('click',function(){
            handlephoneProduct(true);
           
         });
         document.getElementById('phone-decrse').addEventListener('click',function(){
            handlephoneProduct(false);
         });
         function handlephoneProduct(Isincrse){
            const phoneInput = document.getElementById('phone-count');
            const phoneCount = parseInt(phoneInput.value);
            //const caseNewCount = caseCount +1;
            let phoneNewCount = phoneCount;
            if(Isincrse == true){
               phoneNewCount = phoneCount +1;
            }
            if(Isincrse == false && phoneCount >0){
               phoneNewCount = phoneCount -1;
            }
            phoneInput.value = phoneNewCount;
            const phoneTotal = phoneNewCount * 150;
            document.getElementById('phone-total').innerText = '$'+ phoneTotal;
            calculate();
         }
         document.getElementById('case-increse').addEventListener('click',function(){
            handleChangeProduct(true);
           
         });
         document.getElementById('case-decrse').addEventListener('click',function(){
            handleChangeProduct(false);
         });
         function handleChangeProduct(Isincrse){
            const caseInput = document.getElementById('case-count');
            const caseCount = parseInt(caseInput.value);
            //const caseNewCount = caseCount +1;
            let caseNewCount = caseCount;
            if(Isincrse == true){
               caseNewCount = caseCount +1;
            }
            if(Isincrse == false && caseCount >0){
               caseNewCount = caseCount -1;
            }
            caseInput.value = caseNewCount;
            const caseTotal = caseNewCount * 100;
            document.getElementById('case-total').innerText = '$'+ caseTotal;
            calculate();
         }
         function calculate(){
            const phoneInput = document.getElementById('phone-count');
            const phoneCount = parseInt(phoneInput.value);
            const caseInput = document.getElementById('case-count');
            const caseCount = parseInt(caseInput.value);
            const totalPrice = phoneCount*150 + caseCount*100;
            document.getElementById('total-price').innerText = '$'+ totalPrice;
            const tax = Math.round(totalPrice * 0.1);
            document.getElementById('tax-total').innerText = '$'+tax;
            const subTotal = totalPrice + tax;
            document.getElementById('sub-total').innerText = '$'+subTotal;
         }   
         document.getElementById('booknow').addEventListener('click', function (){
      
      document.getElementById('cart-view').style.display = 'none';
   document.getElementById('user-detail').style.display = 'block';
});
    </script>

    <!--Thank You-->
</body>

</html>