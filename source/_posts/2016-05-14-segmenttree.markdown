---
layout: post
title: "segmentTree"
date: 2016-05-14 23:10:30 +0800
comments: true
categories: [Data Structure , Algorithm]
---
# 你好 Octopress
## 这里介绍Segmentree算法

**这段文字被加粗了**

`标亮`

- Android
- PHP
- HTML
	- CSS3
	- HTML5
> 引用

[百度一下](http://www.baidu.com)

![image](http://www.nxist.com/Economic/images/banner1.jpg)

{% video http://static-jkxy.qiniudn.com/event/jkxy_profile20150318.mp4 http://assets.jikexueyuan.com/practice/list_android.jpg 640 320 %}

```
public class SegmentTree{
	public static void main(String args[]){
		System.out.println("Hello Octopress!");
	}
}
```
{% codeblock  快速排序Java版 %}
void sort(int []a, int left, int right){
        if(left >= right)/*如果左边索引大于或者等于右边的索引就代表已经整理完成一个组了*/
        {
            return ;
        }
        int i = left;
        int j = right;
        int key = a[left];

        while(i < j)                               /*控制在当组内寻找一遍*/
        {
            while(i < j && key <= a[j])
            {
                j--;/*向前寻找*/
            }
            a[i] = a[j];
            while(i < j && key >= a[i])
            {
                i++;
            }
            a[j] = a[i];
        }

        a[i] = key;/*当在当组内找完一遍以后就把中间数key回归*/
        sort(a, left, i - 1);/*最后用同样的方式对分出来的左边的小组进行同上的做法*/
        sort(a, i + 1, right);/*用同样的方式对分出来的右边的小组进行同上的做法*/
    }
{% endcodeblock %}