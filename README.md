# Command_Dialog
弹窗输入口令

// 直接调用 CommandDialog((value, callback) => {}, options) 函数显示弹窗  
// 该方法传入一个函数和一个配置对象，函数接收一个回调函数，配置信息： title: '主标题', subTitle: '副标题'  
// 传入的函数是点击确定按钮的事件  
// 回调函数必须执行，且只执行一次  
// 回调函数接收一个参数，传入false或者不传  
// 传入false的时候，提示：口令输入错误！  
// 不传或者传入true的时候则关闭弹窗  
// 示例如下：  
```
CommandDialog((value, callback) => {
   // value：输入框的值， callback：用来关闭弹窗的函数，必须执行
   setTimeout(() => {
      // 模拟ajax请求xxxxxx

      // 第一个参数：是否关闭弹窗，非必填
      // 第二个参数：输入完成关闭弹窗之后的回调函数，非必填
      callback(true, () => {
         console.log('callback')
      })
   }, 1000)
}, {
   title: '主要的标题',
   subTitle: '副标题',
   // 口令语句设置待定
})
```