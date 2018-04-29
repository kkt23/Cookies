<!DOCTYPE html>
<html>
<body onload="setCookie()">

<h1>Welcome to my Home Page</h1>
<p>Please reload the page using <b>F5</b></p>

<script>
document.onkeydown = fkey;
document.onkeypress = fkey
document.onkeyup = fkey;

var wasPressed = false;

function fkey(e){
        e = e || window.event;
       if( wasPressed ) return;

        if (e.keyCode == 116) {
           var x = document.cookie;
             alert("your cookie is "+ x);
             //wasPressed = true;
        }else {
            alert("Window closed");
        }
}

function setCookie() {
     document.cookie ="name=UserOne";
}
</script>

</body>
</html>

<!-- <!DOCTYPE html>
<html>
<body onbeforeunload="return myFunction()">

<p>Close this window, press F5 or click on the link below to invoke the onbeforeunload event.</p>

<a id="myAnchor" href="https://www.w3schools.com">Click here to go to w3schools.com</a>
    
<script>
function myFunction() {
    document.getElementById("myAnchor").text = "arz";
}
</script>

</body>
</html>
