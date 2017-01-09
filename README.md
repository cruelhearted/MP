---
title: js-冒泡排序
date: 2017-01-09 11:02:40
tags:
---
 
![](http://p1.bpimg.com/567571/475307cad577afe4.png)

***
 javascript 冒泡排序 简而言之 就是把一串 无序的 数字 通过js语法 变为有序的数字  或从大到小  或从小到大

 - 在这里 我写了一段关于从小到大排序的 冒泡排序。

 ~~~JS
    <!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>冒泡排序</title>
</head>

<body>
    <script>
    var arr = [99, 52, 36, 49, 23, 24, 5, 9]
    var count = 0;
    // 外循环  控制比较的轮数
    for (var i = 0; i < arr.length - 1; i++) {
        // 在每一轮开始比较前，假设这一轮是比较完毕的
        var isSorted = true;
        // 记录比较的轮数
        count++;
        // 内循环 控制每一轮比较的次数
        for (var j = 0; j < arr.length - 1 - i; j++) {
            // 如果当前项大于当前项的后一项，那么--交换位置
            if (arr[j] > arr[j + 1]) {
                // 交换变量的值
                // 先设置一个新的变量
                var temp = 0;
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                isSorted = false;
            }
        }
        // 确认每一轮比较完毕后，结束循环。
        if (isSorted) {
            break;
        }
    }
    console.log(arr);
    console.log(count);
    </script>
</body>

</html>

 ~~~
