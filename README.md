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
