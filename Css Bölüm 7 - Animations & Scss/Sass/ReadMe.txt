HTML KODLARI

<nav class="clearfix">
  <ul class="navigation">
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <div class="navigation-right">
    <a class="btn-login" href="#">Login</a>
    <a class="btn-signup" href="#">Sign Up</a>
    </div>  
    
    </nav>

------------------------------------------
------------------------------------------
------------------------------------------
------------------------------------------


CSS (SCSS) KODLARI


*{
  margin:0;
  padding:0;
}
$color-primary: #007bff;
$color-secondary: #6c757d;
$color-success: #28a745;
$color-white: #fff;
$width-button: 100px;

nav{
  margin: 50px;
  background-color: $color-success;

&::after{
  clear:both;
  content:"";
  display:block;
}

}

.navigation{
  float:left;
  list-style: none;
  li{
  display: inline-block;
  margin-left: 20px;
  
  
  &:first-child {
    margin:0;
  }
    a{
      text-decoration:none;
      text-transform: uppercase;
      color: $color-white;
      display:inline-block;
      padding:10px;
    }
  
}
}

.navigation-right{
  float:right;
}
.btn-login, .btn-signup{
  padding:10px;
  display: inline-block;
  width: $width-button;
  border-radius: 100px;
  text-decoration:none;
  text-transform:uppercase;
  color: $color-white;
  text-align:center;
}
.btn-login, .btn-signup{
  &:link{
    background-color: $color-primary;
  }
  &:hover{
    background-color: darken($color-primary,20%);
  }
}


------------------------------------------
------------------------------------------
------------------------------------------
------------------------------------------
------------------------------------------



COMPLİED CSS KODLARI

* {
  margin: 0;
  padding: 0;
}

nav {
  margin: 50px;
  background-color: #28a745;
}
nav::after {
  clear: both;
  content: "";
  display: block;
}

.navigation {
  float: left;
  list-style: none;
}
.navigation li {
  display: inline-block;
  margin-left: 20px;
}
.navigation li:first-child {
  margin: 0;
}
.navigation li a {
  text-decoration: none;
  text-transform: uppercase;
  color: #fff;
  display: inline-block;
  padding: 10px;
}

.navigation-right {
  float: right;
}

.btn-login, .btn-signup {
  padding: 10px;
  display: inline-block;
  width: 100px;
  border-radius: 100px;
  text-decoration: none;
  text-transform: uppercase;
  color: #fff;
  text-align: center;
}

.btn-login:link, .btn-signup:link {
  background-color: #007bff;
}
.btn-login:hover, .btn-signup:hover {
  background-color: #004a99;
}