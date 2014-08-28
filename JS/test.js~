
checkbox=[];

for(i=0;i<$(":input").length;i++)
{
if($(":input")[i].type=="checkbox")
  checkbox.push($(":input")[i]);
}

$(":input").blur(function(){
if(this.type=="text")
textFieldValid(this);
else if(this.type=="password")
passwordValid(this);
else if(this.type=="email")
emailValid(this);
else if(this.type=="checkbox")
checkboxValid();
else if(this.type=="radio")
radioValid(this);
else if(this.type=="file")
fileUploadValid(this);
  });

$("select").blur(function(){
selectValid(this);
});
/*TextFeild validation start*/


function textFieldValid(obj)
{
$(obj).next("p").remove();
var reg = /^((?:[A-z]+)[a-zA-Z0-9]{5,8})$/;


if($(obj).val()==""||$(obj).val().length<5||$(obj).val().length>8)
{
$(obj).after("<p>This field should not be empty & length of {5-8}</p>");
$(obj).focus();
$(obj).select();
return false;
}
else if(reg.test($(obj).val()) == false)
   {	
$(obj).after("<p>Accepts alphanumeric characters & length of {5-8}</p>");
$(obj).focus();
$(obj).select();
        
   return false;

    }

else

return true;
}


/*TextFeild validation end*/


/* Password Field validation start*/

function passwordValid(obj)
{
$(obj).next("p").remove();
var reg = /^[a-zA-Z0-9]{6}$/;
if($(obj).val()=="")
{
$(obj).after("<p>This field should not be empty</p>");

$(obj).focus();
$(obj).select();
return false;
}
else if(reg.test($(obj).val()) == false)
   {	
$(obj).after("<p>This field contains maximum of 6 characters</p>");

$(obj).focus();
$(obj).select();
   return false;

    }
else
return true;
}

/* Password Field validation end*/



/* file upload validation start*/

function fileUploadValid(obj)
{
$(obj).next("span").remove();
var pic1=/.gif/;
    var pic2=/.jpg/;
    var pic3=/.jpeg/;
    var pic4=/.png/;


    if($(obj).val() == null || $(obj).val() == "")
   {
       $(obj).after("<span>Select image</span>");
      $(obj).focus();
      return false;
   } 

   else if($(obj).val().match(pic1) || $(obj).val().match(pic2) || $(obj).val().match(pic3)|| $(obj).val().match(pic4))
   {
        return true;
   }
   else
   {
  $(obj).after("<span>Select image of format{jpg,gif,png,jpeg}</span>");
     $(obj).focus();
    return false;
   }


}

/* file upload validation end*/


/* Radiobutttons validation start*/
function radioValid(obj)
{
$(obj).next("span").remove();
count1=0;
if($(obj).is(":checked"))
count1++;
if(count1==0)
{
$(obj).after("<span>Select radio button</span>");
$(obj).focus();
return false;
}
else 
return true;
}


/* Radiobutttons validation end*/



/*select box validation start*/

function selectValid(obj)
{
$(obj).next("span").remove();
if ($(obj).val()=="" ||  $(obj).val()==null)
{
$(obj).after("<span>Select this field</span>");
$(obj).focus();
return false;
}
else 
return true;
}


/*select box validation end*/



/*checkbox validation start*/

function checkboxValid()
 {
$("input:checkbox").next("span").remove();
 count=0;
 for(t=0;t<checkbox.length;t++)
  {
   if($(checkbox[t]).is(":checked"))
 count++;
   }
   if(count==0)
   {
    $("input:checkbox").last().after("<span>Select atleast one checkbox</span>");
    return false;

   }
   else 
    return true;
   }

/*checkbox validation end*/

/* Email feild validation start*/
function emailValid(obj)
{
$(obj).next("p").remove();
var reg= /^[a-zA-Z0-9]+[\@][a-zA-Z0-9]+[\.][a-zA-Z]{2,4}$/;


if($(obj).val()=="")			//||$(obj).val().length<10||$(obj).value.length>25
{
$(obj).after("<p>This field should not be empty</p>");
$(obj).focus();
$(obj).select();
return false;
}
else if(reg.test($(obj).val()) == false)
   {	
$(obj).after("<p>This field should be in format[Ex:abc@gmail.com]</p>");
$(obj).focus();
$(obj).select();    
   return false;
    }

else
return true;
}

/* Email feild validation end*/




function genjqvalid()
{

 
for(i=0;i<$(":input").length;i++)
{   
if($(":input")[i].type=="text")
 {

var TextField=textFieldValid($(":input")[i]);
if(!TextField)
return false;
}  

else if($(":input")[i].type=="password")
{

 
var PasswordField=passwordValid($(":input")[i]);
if(!PasswordField)
return false;

}




else if($(":input")[i].type=="file")
{

var Browse=fileUploadValid($(":input")[i]);
if(!Browse)
return false;

}



else if($(":input")[i].type=="email")
{

 
var EmailField=emailValid($(":input")[i]);
if(!EmailField)
return false;

}

else if($(":input")[i].type=="select-multiple")
{

var SelectField1 = selectValid($(":input")[i]);
if(!SelectField1)
return false;

}
else if($(":input")[i].type=="select-one")
{

 
var SelectField2 = selectValid($(":input")[i]);
if(!SelectField2)
return false;

}

else if($(":input")[i].type=="checkbox")
{

var Checkboxes=checkboxValid($("input[type=checkbox]")[0]);
if(!Checkboxes)
return false;

}
else if($(":input")[i].type=="radio")
{

var Radiobuttons=radioValid($("input[type=radio]")[0]);
if(!Radiobuttons)
return false;

}




}
alert("submit success");
return true;



}


