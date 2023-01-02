//verification-of-sinx-and-cox

function factorial(a){
  if(a==0 || a==1){
    return 1;
  }
  else{
    return a*factorial(a-1);
  }
}
let n=prompt("Enter the value of range: ")
n=Number.parseInt(n)
let x=prompt("Enter the value of angle: ")
x=Number.parseInt(x)
let s=prompt("Enter S for sin and C for cos: ")

let b= x*(3.14/180);
let sinx=0;
let cosx=0;
if(s=="s"|| s=="S"){
  for(let i=0;i<n;i++){
    sinx=sinx + Math.pow(-1,i)*(Math.pow(b,2*i +1))/(factorial(2*i + 1));
  }
  console.log("Value of sin "+ x +" is "+ sinx);
  console.log("Value of sin "+ x +"library is "+ Math.sin(b));
}
if(s=="c" || s=="C"){
  for(let i=0;i<n;i++){
    cosx=cosx + Math.pow(-1,i)*(Math.pow(b,2*i))/(factorial(2*i));
  }
  console.log("Value of cos "+ x +" is "+ cosx);
  console.log("Value of cos "+ x +"by library is "+ Math.cos(b));
}


