#leetcode上各题型的解法总结

##数组：

1. [二分法](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0704.%E4%BA%8C%E5%88%86%E6%9F%A5%E6%89%BE.md)
	
	- 左闭右闭	[left,right]

	- 左闭右开	[left,right)

	两种不同的解法对于循环判断条件及right的取值有所不同

2. [双指针法](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0027.%E7%A7%BB%E9%99%A4%E5%85%83%E7%B4%A0.md)

	- 快慢指针
	
		逻辑上为建立一个新数组，物理上该新数组的元素直接覆盖在原数组上

	- 左右指针

		从中间向左右或从左右至中间

3. [滑动窗口法](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0209.%E9%95%BF%E5%BA%A6%E6%9C%80%E5%B0%8F%E7%9A%84%E5%AD%90%E6%95%B0%E7%BB%84.md)

	重点为滑动窗口起始位置的变化，且起始位置和终止位置变化的频率可能不同

##链表：

1. [虚拟头结点](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0203.%E7%A7%BB%E9%99%A4%E9%93%BE%E8%A1%A8%E5%85%83%E7%B4%A0.md)

	可以统一链表头结点与其它结点的循环操作

2. 双指针（多指针）

	- [反转链表](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0206.%E7%BF%BB%E8%BD%AC%E9%93%BE%E8%A1%A8.md)
	
		两个相差一个元素的指针fast和slow，循环一遍可将所有链表元素反转
	
	- [两两交换链表元素](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0024.%E4%B8%A4%E4%B8%A4%E4%BA%A4%E6%8D%A2%E9%93%BE%E8%A1%A8%E4%B8%AD%E7%9A%84%E8%8A%82%E7%82%B9.md)

		三个指针prev、cur和next，循环一遍可将所有链表元素两两交换

	- [删除倒数第N个结点](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0019.%E5%88%A0%E9%99%A4%E9%93%BE%E8%A1%A8%E7%9A%84%E5%80%92%E6%95%B0%E7%AC%ACN%E4%B8%AA%E8%8A%82%E7%82%B9.md)

		两个相差N个元素的指针fast和slow，当fast移动至链尾时slow将同步移动至目标结点

3. 链表长度的作用
	
	- [链表相交](https://github.com/Ssatomi/leetcode-master/blob/master/problems/%E9%9D%A2%E8%AF%95%E9%A2%9802.07.%E9%93%BE%E8%A1%A8%E7%9B%B8%E4%BA%A4.md)

		单链表相交最后必对齐，可根据两个链表的长度差对齐查找

4. 环形链表

	- [找环的入口](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0142.%E7%8E%AF%E5%BD%A2%E9%93%BE%E8%A1%A8II.md)

		两个指针fast和slow，fast每移动两步则slow移动一步，最后两个指针会在环内相遇，此时相遇点设为index1，头结点设为index2，两个结点同步移动，最终会在环的入口结点相遇

##哈希表：

1. [数组](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0242.%E6%9C%89%E6%95%88%E7%9A%84%E5%AD%97%E6%AF%8D%E5%BC%82%E4%BD%8D%E8%AF%8D.md)

	数组可以当哈希表，存取速度均为O(1)，当哈希值不能太少太分散

2. [set](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0349.%E4%B8%A4%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86.md)

	当数组不合适，且所求目标仅为一个值，无需记录其它关联信息时，可使用set

3. [map](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0454.%E5%9B%9B%E6%95%B0%E7%9B%B8%E5%8A%A0II.md)

	当所求目标为值的关联信息时，可使用map，利用key-value的关联特性得到

##字符串：

1. 库函数

	sort(begin(),end()), substr(index,length), find("s",index), replace(index,length,"s"), insert(index,"s"), push_back("s"), append("s"), erase(index,length), s.swap(t), size(), length(), empty(), at()

2. [双指针法](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0344.%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2.md)

	反转(左移右移)字符串：反转局部->反转整体；反转整体->反转局部

3. [扩展字符串后倒序填充](https://github.com/Ssatomi/leetcode-master/blob/master/problems/%E5%89%91%E6%8C%87Offer05.%E6%9B%BF%E6%8D%A2%E7%A9%BA%E6%A0%BC.md)

4. [KMP算法](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0028.%E5%AE%9E%E7%8E%B0strStr.md)

	求next数组，根据next数组匹配子串

##双指针法：

1. [数组](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0027.%E7%A7%BB%E9%99%A4%E5%85%83%E7%B4%A0.md)

2. [字符串](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0151.%E7%BF%BB%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2%E9%87%8C%E7%9A%84%E5%8D%95%E8%AF%8D.md)

3. [链表](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0142.%E7%8E%AF%E5%BD%A2%E9%93%BE%E8%A1%A8II.md)

##栈与队列

1. [栈实现队列](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0232.%E7%94%A8%E6%A0%88%E5%AE%9E%E7%8E%B0%E9%98%9F%E5%88%97.md)

2. [队列实现栈](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0225.%E7%94%A8%E9%98%9F%E5%88%97%E5%AE%9E%E7%8E%B0%E6%A0%88.md)

3. [栈的应用](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0020.%E6%9C%89%E6%95%88%E7%9A%84%E6%8B%AC%E5%8F%B7.md)

4. [单调队列](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0239.%E6%BB%91%E5%8A%A8%E7%AA%97%E5%8F%A3%E6%9C%80%E5%A4%A7%E5%80%BC.md)

5. [优先级队列](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0347.%E5%89%8DK%E4%B8%AA%E9%AB%98%E9%A2%91%E5%85%83%E7%B4%A0.md)

6. [单调栈](https://github.com/Ssatomi/leetcode-master/blob/master/problems/0042.%E6%8E%A5%E9%9B%A8%E6%B0%B4.md)