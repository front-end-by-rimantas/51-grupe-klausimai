# 51 grupės klausimai
## atidarius ant mazesnio ekrano nei buvo dirbta pabega viskas https://deivor24.github.io/Position/
</head>
<body class="body" style="background-color: burlywood;">
    <main class="main">
        <div class="photo">
            <h1 class="signup">Sign Up</h1>
            <p class="policy">Privacy policy & terms of service</p>
        </div>
        <div class="white">
            <div class="x">X</div>
            <div class="info">
                <p class="username">username</p>
                <input class="one" type="text">                
                <p class="email">email</p>
                <input class="two" type="text">
                <p class="password">password</p>
                <input class="three" type="text">
                <p class="repassword">repassword</p>
                <input class="four" type="text">
            </div>
            <section class="getst">
                <a href="#" class="start">Get started</a>
                <p class="or">or <span><a href="#" class="in">Sign in</a></span></p>
            </section>
        </div>

    </main>

    ----------------------
    .body{
    margin: 0;
    background-image: url(./img/Screenshot\ 2024-07-22\ 082839.png);
    background-repeat:no-repeat;
    background-size: 100%;
    
    
    
    image-resolution: 0;
}
.main{
    display: flex;
    align-items: center;
    width: 50%;
    height: 50%;
    margin-top: 13%;
    margin-left: 25%;
    position: fixed;
   
}
.x{
    float: right;
    padding: 15px;
}
.info{
    text-transform: uppercase;
    font-size: large;
    position: absolute;
    top: 8%;
    left: 48%
    
}
.getst{
    display: flex;
    align-items: center;
    gap: 40px;
    position: absolute;
    left: 48%;
    top:82%;

}
.photo{
    display: flex;
    align-items:normal;
    color: white;
    font-size: 30px;
    font-weight: lighter;
    font-family: dubai light;
    background-image: url(./img/Screenshot\ 2024-07-22\ 082839.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 40%;
    height: 500px;
    margin-left: 5%;
    
}
.white{
    background-color: white;
    width: 50%;
    height: 600px;
}
.signup{
    position: absolute;
    left: 10%;    
}

.policy{
    font-size: 16px;
    position: fixed;
    left: 30%;
    top:72%;

}

.start{
    background-color: blue;
    color: white;
    padding: 30px;
    padding-top: 5px;
    padding-bottom: 5px;
    border-radius: 15px;
}

.one,
.two,
.three,
.four{
    width: 350px;
    border: none;
    border-bottom: 2px dotted grey

}
##
