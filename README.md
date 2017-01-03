# psmodnasyncjs
##3. Building a Promise Framework
###3 Solution - Split Success and Error Callbacks
```
function fetCurrentCity(onSuccess,onError){
  getCurrentCity(function(error,result){
    if(error){
      onError(error);
      return;
    }
    onSuccess(result);
  }
}
```
test
```
test('desc',function(){
  function onSuccess(result){console.log(result);}
  function onError(result){console.log(error);}
  fetchCurrentCity(onSuccess,onError);
})
```
