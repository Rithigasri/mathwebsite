# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include Regular Expression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mathematical Calculation</title>
    <style>
        * {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
    }

    body{
        background-color:lightseagreen;
        color:black;
        
    }
    .container{
        width: 1080px;
        margin-left: auto;
        margin-right: auto;
    }
    .content{
        display:block;
        width:75%;
        margin-left: auto;
        margin-right: auto;
        background-color:lavenderblush;
        max-height: 300px;
        margin-top:50px;
    }

    h1{
        text-align: center;
        padding-top:30px;
        font-size:30px;

    }
    .formelement{
        text-align:center;
        padding-bottom:15px;
        font-size:20px;

    }
    .footer{
    display:inline-block;
    width:810px;
    height: 36px;
    background-color: lightcoral;
    color:black;
    text-align: center;
    padding-top: 8px;
    margin-left:auto;
    margin-right: auto;
    }
    </style>
</head>
<body>
    <div>
        <div class="container">
            <div class="content">
                <div class="box">
                    <h1>VOLUME OF CONE</h1>
                    <form>
                        <div class="formelement">
                            <label for="radedit">Radius:</label>
                            <input type="text" id="radedit" value="0"/>Meters
                            
                        </div>
                        <div class="formelement">
                            <label for="heiedit">Height:</label>
                            <input type="text" id="heiedit" value="0"/>Meters
                            
                            
                        </div>
                        <div class="formelement">
                            <input type="button" value="CALCULATE VOLUME" id="calculatevol"/>
                        </div>
                        <div class="formelement">
                            <label for="cedit">Volume of Cone:</label>
                            <input type="text" id="cedit" readonly value="0"/>Meter<sup>3</sup>
                            
                            
                        </div>
                    </form> 
                </div>
            <div class="footer">Developed by Rithiga Sri.B</div> 
            </div>
        </div>
    </div>
    <div>
        <div class="container">
            <div class="content">
                <div class="box">       
                    <h1>AREA OF TRIANGLE</h1>
                    <form>
                        <div class="formelement">
                            <label for="bedit">Base:</label>
                            <input type="text" id="bedit" value="0"/>Meters
                    
                            
                        </div>
                        <div class="formelement">
                            <label for="hedit">Height:</label>
                            <input type="text" id="hedit" value="0"/>Meters
                      
                        </div>
                        <div class="formelement">
                            <input type="button" value="CALCULATE AREA" id="calculatearea"/>
                        </div>
                        <div class="formelement">
                            <label for="aedit">Area of Triangle:</label>
                            <input type="text" id="aedit" readonly value="0"/>Meter<sup>2</sup>
                            
                        </div>
                    </form>
                </div>
            <div class="footer">Developed by Rithiga Sri.B</div>
            </div>
        </div>
    </div>

<script>
    var button;
    button=document.querySelector("#calculatevol");
    button.addEventListener("click",function(){
        var radtext,heitext,voltext;
        var radval,heival,volval;
        var pi;
        var num=1/3;
        var res,res1,reg;
        
        radtext=document.querySelector("#radedit");
        heitext=document.querySelector("#heiedit");
        voltext=document.querySelector("#cedit");
        pi=Math.PI;
        reg=new RegExp("^[1-9]+[0-9]*$");

        radval=radtext.value;
        res=radval.match(reg);
        heival=heitext.value;
        res1=heival.match(reg);
        
        if(res==null)
        {
            alert("Please Enter Positive Integers Only for Radius");
        }
        if(res1==null)
        {
            alert("Please Enter Positive Integers Only for Height");
        }
        volval=num*pi*radval*radval*heival;
        voltext.value=""+volval;
});
    var button;
    button=document.querySelector("#calculatearea");
    button.addEventListener("click",function(){
        var btext,htext,areatext;
        var rval,hval,areaval;
        var result,result1,rexp;

        btext=document.querySelector("#bedit");
        htext=document.querySelector("#hedit");
        areatext=document.querySelector("#aedit");

        rexp=new RegExp("^[1-9]+[0-9]*$");

        bval=btext.value;
        result=bval.match(rexp);
        hval=htext.value;
        result1=hval.match(rexp);

        if(result==null)
        {
            alert("Please Enter Positive Integers Only for Base");
        }
        if(result1==null)
        {
            alert("Please Enter Positive Integers Only for Height");
        }
        areaval=1/2*bval*hval;
        areatext.value=""+areaval;

});
    
</script>
    
</body>
</html>
```

## OUTPUT:
![OUTPUT](output.png)

## HTML VALIDATOR:
![VALIDATOR](validator.png)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
