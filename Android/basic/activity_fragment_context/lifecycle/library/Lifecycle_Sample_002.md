###### 打开与关闭一个新的Activity

基于Android Api 26 版本的 源码

> 打开 新页面

[ (MainActivity.kt:16) #onCreate] 执行了  
[ (MainActivity.kt:28) #onStart] 执行了  
[ (MainActivity.kt:33) #onResume] 执行了  
[ (MainActivity.kt:43) #onPause] 执行了  
[ (AIndexActivity.kt:17) #onCreate] 执行了  
[ (AIndexActivity.kt:29) #onStart] 执行了  
[ (AIndexActivity.kt:34) #onResume] 执行了  
[ (MainActivity.kt:58) #onSaveInstanceState] 执行了  
[ (MainActivity.kt:48) #onStop] 执行了  

> A页面按下Home

[ (AIndexActivity.kt:44) #onPause] 执行了  
[ (AIndexActivity.kt:59) #onSaveInstanceState] 执行了  
[ (AIndexActivity.kt:49) #onStop] 执行了  

> 再次进入A页面

[ (AIndexActivity.kt:39) #onRestart] 执行了  
[ (AIndexActivity.kt:29) #onStart] 执行了  
[ (AIndexActivity.kt:34) #onResume] 执行了  

> A页面返回Main

[ (AIndexActivity.kt:44) #onPause] 执行了  
[ (MainActivity.kt:38) #onRestart] 执行了  
[ (MainActivity.kt:28) #onStart] 执行了   
[ (MainActivity.kt:33) #onResume] 执行了  
[ (AIndexActivity.kt:49) #onStop] 执行了  
[ (AIndexActivity.kt:54) #onDestroy] 执行了    
[ (MainActivity.kt:43) #onPause] 执行了  
[ (MainActivity.kt:48) #onStop] 执行了  
[ (MainActivity.kt:53) #onDestroy] 执行了  
