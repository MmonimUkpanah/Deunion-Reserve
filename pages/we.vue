<template>
    <div>
        <div class="nav1">
            <ul class="nav nav-tabs">
                <li class="nav-item">
                    <a class="nav-link "  href="/">Deunion Reserve</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link "  href="/do">What we do</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/we">Who we Are</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link"  href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="con3">
            <h1>Management Board</h1>
            <p>The Management Board is responsible for managing the company. Its members are jointly accountable for the management of the company. The Management Board has, as its prime responsibility, the group's strategic management, resource allocation, financial accounting and reporting, risk management, and corporate control.</p>
        </div>
        <div class="con4">
            <div class="con5">
                <img src="/img/new/sew.jpg" alt="">
                <div class="con6">
                    <h4>Christian Sewing</h4>
                    <p>Chief Executive Officer</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/von.jpg" alt="">
                <div class="con6">
                    <h4>Karl von Rohn</h4>
                    <p>President</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/cam.jpg" alt="">
                <div class="con6">
                    <h4>Fabrizio Campelli</h4>
                    <p>Corporate Bank and Investment Bank</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/ben.jpg" alt="">
                <div class="con6">
                    <h4>Bernd Leukert</h4>
                    <p>Chief Technology, Data and Innovation Officer</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/lew.jpg" alt="">
                <div class="con6">
                    <h4>Stuart Lewis </h4>
                    <p>Chief Risk Officer</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/vt.jpg" alt="">
                <div class="con6">
                    <h4>James von Moltke</h4>
                    <p>Chief Financial Officer</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/alex.jpg" alt="">
                <div class="con6">
                    <h4>Alexander von zur Muhlen</h4>
                    <p>Chief Executive Officer Asia Pacific</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/ri.jpg" alt="">
                <div class="con6">
                    <h4>Christiana Riley</h4>
                    <p>Chief Executive Officer Americas</p>
                </div>
            </div>
            <div class="con5">
                <img src="/img/new/ca.jpg" alt="">
                <div class="con6">
                    <h4>Rebecca Short</h4>
                    <p>Chief Transformation Officer</p>
                </div>
            </div>

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
    .con2{
        background: url("/img/new/page.jpg") center center/cover;
        height: 100vh;
        margin-bottom: 1rem;
    }
    .con3{
        margin-left: 5%;
        margin-right: 5%;
        margin-top: 2rem;
    }
    .con3 h1{
        color: blue;
    }
    .con3 p{
        font-size: 20px;
    }
    .con4{
        margin-left: 5%;
        margin-right: 5%;
        display: grid;
        grid-gap: 2rem;
        margin-top: 2rem;
        grid-template-columns: 1fr 1fr 1fr;
    }
    .con5{
        text-align: center;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
    .con5 img{
        width: 100%;
    }
    .con6 h4{
        margin-top: 0.5rem;
        margin-bottom: 0.5rem;
    }
    @media(max-width:567px){
        .con{
        margin-left: 10px;
        margin-right: 10px;
    }
        .con3{
        margin-left: 10px;
        margin-right: 10px;
        margin-top: 2rem;
    }
        .con4{
        margin-left: 10px;
        margin-right: 10px;
        display: grid;
        grid-gap: 2rem;
        margin-top: 2rem;
        grid-template-columns: 1fr;
    }
    }
</style>