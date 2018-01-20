# js-Math
js-Math对象的基础使用

max()  获取最大值   min() 获取最小值


          var max=Math.max(1,2,5,4,0,6,8,9);
           console.log(max)   //9

           var min=Math.min(1,3,0);
           console.log(min)   // 0
           
           
           还可以使用apply() 方法
           这个技巧的关键把Math对象作为apply() 的第一个参数，从而正确的设置了this值，
           然后，可以将任何数组作为第二个参数
           
           
           	var val=[1,2,4,3,6,9,0];
            var min=Math.min.apply(Math,val);

            console.log(min)   // 0
            
            
   舍入方法
     
               Math.ceil()  向上舍入，总是将数值向上舍入到最接近的整数
               Math.floor() 向下舍入，总是将数值向下舍入到最接近的整数
               Math.round() 标准舍入，总是将数值四舍五入到最接近的整数

                   Math.round() 标准舍入
                    console.log(Math.round(26.5))  //27
                    console.log(Math.round(26.4)) //26 

                  Math.floor() 向下舍入     
                    console.log( Math.floor(25.8))  //25
                    console.log( Math.floor(25.4))  //25  

                 Math.ceil()  向上舍入
                     console.log(  Math.ceil(25.8))  //26
                     console.log(  Math.ceil(25.1))  //26  
            
random() 获取随机数

           公式：-》  值=Math.floor(Math.random() * 可能值的总数 + 第一个可能的值);

            例子 ： 比如得到一个20之间的随机数
                    var num=Math.floor(Math.random()*20+1);
               
               
                    比如得到一个10与2之间的随机数   就得这样写
                    var num=Math.floor(Math.random() * 9+2 );
                   
              再看下面这个  取随机 字母 例子：
                   
                  function setText(max_s,min_s){
                    var sun=max_s-min_s+1;
                    return Math.floor(Math.random()*sun+min_s)
                    }	
		var arr=["a","b","c","d","e","f"];
		var text=arr[setText(0,arr.length-1)];
                    
                    这样可以随机取出  a-f 之间的随机数
		console.log(text)
                    
