<template>
    <div>
        <div class="nav1">
            <ul class="nav nav-tabs">
                <li class="nav-item">
                    <a class="nav-link "  href="/">Deunion Reserve</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/do">What we do</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/we">Who we Are</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link active" aria-current="page" href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="con">
            <h1>Contact</h1>
            <p>Your questions or comments are very important to us. For enquiries regarding online banking – including security topics, phishing, PIN/TAN numbers, banking terminals, lost or stolen credit cards, loans, savings etc. – please visit the relevant section of your local Private Bank website. You can send us an email for other topics.</p>
            <p>IMPORTANT NOTE: In order to maintain discretion, please do not email any confidential information such as account numbers. For your own security, since it is not possible to identify an email sender, Deutsche Bank cannot accept via email any orders for business transactions such as the opening of accounts, payment orders, trading orders, changes of address or the like. For such transactions, please contact the appropriate office. You can also find the address of all our locations worldwide at db.com/addresses. Send an email to deutsche.bank@db.com for other enquiries.</p>
        </div>
        <footer-sections/>
    </div>
</template>
<style scoped>
@font-face {
    font-family: DMSans;
    src: url("/font/DMSans-Regular.ttf");
    }
    
    .con{
        margin-left: 5%;
        margin-right: 5%;
    }
    .con h1{
        color: blue;
        margin-bottom: 2rem;
    }
    .con p{
        margin-bottom: 2rem;
    }
    .nav1{
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    .nav1{
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    .nav-item{
        margin-left: 3rem;
    }
    .active{
        border-bottom: 1px solid #dee2e6  !important ;
    }
    a{
        color: black;
    }

    @media(max-width:567px){
        .con{
        margin-left: 10px;
        margin-right: 10px;
    }
    }
</style>