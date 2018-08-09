# Number-Pyramid
Using recursion to build a number pyramid from an array of numbers

function pyramidrecur(arr){
  if(!arr[0][0]){
arr = [arr];}
  else if(arr[0].length == 1){
  return [arr[0]];}
 var newLayer = []
  for( var i = 0; i < arr[0].length - 1; i++){
    newLayer.push(arr[0][i] + arr[0][i+1]);}
  return pyramidrecur([newLayer]).concat(arr);
}
console.log(pyramidrecur([1,2,3,4]));
