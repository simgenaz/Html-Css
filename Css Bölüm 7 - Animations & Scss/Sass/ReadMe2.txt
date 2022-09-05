MİXİNS HTML KODLARI


  <div id="first"></div>
  <div id="second"></div>
  <div id="third"></div>
    
----------------------------------
----------------------------------
----------------------------------
----------------------------------

MİXİNS CSS(SCSS) KODLARI

div{
  float:left;
}

@mixin box($color, $width){
  width:$width;
  height:100px;
  background-color:$color;
  margin:15px;
}

#first {
 @include box(red , 200px);
}
#second {
 @include box(green, 100px);

}
#third {
 @include box(blue, 300px);
  
}

----------------------------------
----------------------------------
----------------------------------
----------------------------------
----------------------------------


MİXİNS COMPLİED CSS KODLARI

div {
  float: left;
}

#first {
  width: 200px;
  height: 100px;
  background-color: red;
  margin: 15px;
}

#second {
  width: 100px;
  height: 100px;
  background-color: green;
  margin: 15px;
}

#third {
  width: 300px;
  height: 100px;
  background-color: blue;
  margin: 15px;
}

----------------------------------
----------------------------------
----------------------------------
----------------------------------
----------------------------------


EXTEND CSS(SCSS) KODLARI

div{
  float:left;
}
%box{
  width:100px;
  height:100px;
  margin:15px;
}

#first {
  @extend %box;
  background-color:red;
}
#second {
 @extend %box;
  background-color:green;
}
#third {
   @extend %box;
  background-color:blue;
  
}

----------------------------------
----------------------------------
----------------------------------
----------------------------------
----------------------------------



EXTENDS COMPLİED CSS KODLARI

div {
  float: left;
}

#third, #second, #first {
  width: 100px;
  height: 100px;
  margin: 15px;
}

#first {
  background-color: red;
}

#second {
  background-color: green;
}

#third {
  background-color: blue;
}


MİXİNS VE EXTENDS KULLANIMLI SCSS KODLARI

*{
  margin:0;
  padding:0;
}
$color-primary: #007bff;
$color-secondary: #6c757d;
$color-success: #28a745;
$color-white: #fff;
$color-black: #000;
$width-button: 100px;

@mixin clearfix{
  &::after{
  clear:both;
  content:"";
  display:block;
}
}

@mixin link-color($color){
    text-decoration:none;
  text-transform:uppercase;
  color: $color-white;
}

nav{
  margin: 50px;
  background-color: $color-success;
  @include clearfix;
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
      display:inline-block;
      padding:10px;
      @include link-color($color-white);
    }
  }
}

.navigation-right{
  float:right;
}
%btn-placeholder{
  padding:10px;
  display: inline-block;
  width: $width-button;
  border-radius: 100px;
  text-align:center;
  @include link-color($color-black);
}

.btn-login{
  &:link{
    @extend %btn-placeholder;
    background-color: $color-primary;
  }
  &:hover{
    background-color: darken($color-primary,20%);
  }
}
.btn-signup{
  &:link{
    @extend %btn-placeholder;
    background-color: $color-secondary;
  }
  &:hover{
    background-color: lighten($color-secondary,20%);
  }
}


