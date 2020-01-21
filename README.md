# sandipavere


<html>
    <head>
      
         <script>
            function my(){
             var a=document.getElementById("passwords").value;
             var b=document.getElementById("confirm pass").value;
            
             
             if(a==""){
                document.getElementById("messages").innerHTML="*** please fill password";
                return false;
             }  
             if(a.length < 5){
                 document.getElementById("messages").innerHTML="** password length must be greater than 5 character";
                 return false; 
                }  
                else if(a.search(/[0-9]/)== -1){
                 document.getElementById("messages").innerHTML="atleast 1 numeric value";
                 
                return false;
             }
             else if(a.search(/[A-Z]/)== -1){
                 document.getElementById("messages").innerHTML="atleast 1 upper case letter";
                 return false;
             } 
             else if(a.search(/[a-z]/)== -1){
                 document.getElementById("messages").innerHTML="atleast 1 lower case letter";
                 return false;
             } 
              else if(a.search(/[!\@\#\$\^\&\*\%]/)== -1){
                 document.getElementById("messages").innerHTML="atleast 1 special character";
                 return false;
             }
             if(a.length > 10){
                 document.getElementById("messages").innerHTML="** password length must be smaller than 10 character";
                 return false;
             }
             if(a!=b){
               document.getElementById("messages").innerHTML="** password not match";
               return false;
             }      
             
             
         }
        </script>
    </head>
    <body>
       
        <form onsubmit="return my()">
        password:<input type="password" id="passwords" value="">
        <span id="messages" style="color: red"></span><br/>
        confirm password:<input type="password" id="confirm pass" value="">
        <span id="messages"></span><br/> 
        <input type="submit" value="Submit">
        </form>
    </body>
</html
