<html>
<head>
<title>lift Services</title>
</head>
<body>
<h1 align="center">WELCOME to tallex</h1>
<h1 >Lift Services</h1>
<script>


function mockup()
{
  gpos=prompt("Enter your floor", 0);
  var i;
  for(i=1; i<=4; i++)
  {
    a[i]=posl(i)
    b[i]=lift(gpos, i);
  }

  var h=b[1];

  for(i=1; i<=4; i++)
  { 
    if(h<b[i])
    {
      h=b[i];
      d=i;
    }
  }
  
  s=posl(i);
  
  document.write("closest lift to you is"+s)<br/>;
  document.write("current position of the lift "+d+" is "+s)<br/>;


}  


function posl(i)
{
  var x;
  if(i==1)
  {
    x=73;
  }
  else if(i==2)
  {
    x=94;
  }
  else if(i==3)
  {
    x=3;
  }
  else if(i==4)
  {
    x=20;
  }
  
  return x;
}


function lift(gpos, i)
{
  var t=0;
  var x = posl(i);
  if(gpos<x)
  {
    for(k=x; k>=gpos; k--)
    {
      t=t+5;
      if(k%i==0)
      {
        t=t+2;
      }
    }
  }
  else if(gpos>x)
  {
    for(k=x; k<=gpos; k++)
    {
      t=t+7;
      if(k%i==0)
      {
        t=t+2;
      }
    }
  }
  return t;
  document.write(t)
}


</script>
<button onclick="mockup()">Current position of the Lift</button>
</body>
</html>
