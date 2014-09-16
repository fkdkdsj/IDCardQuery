IDCardQuery
===========

输入身份证号码，判断18位身份证号码是否合法，并查询信息(性别，年龄，所在地)

####简介
不同版本的身份证信息查询小程序，带合法性检验

####版本
* C
* Python

####验证原理
一. 将前面的身份证号码17位数分别乘以不同的系数。从第一位到第十七位的系数分别为：<br />7 9 10 5 8 4 2 1 6 3 7 9 10 5 8 4 2<br />二. 将这17位数字和系数相乘的结果相加。<br />三. 用加出来和除以11，看余数是多少？<br />四. 余数只可能有0 1 2 3 4 5 6 7 8 9 10这11个数字。其分别对应的最后一位身份证的号<br />码为1 0 X 9 8 7 6 5 4 3 2。<br />五. 通过上面得知如果余数是2，就会在身份证的第18位数字上出现罗马数字的Ⅹ。如果余数<br />是10，身份证的最后一位号码就是2。<br />例如：某男性的身份证号码是34052419800101001X。我们要看看这个身份证是不是合法的身<br />份证。<br />首先：我们得出，前17位的乘积和是189<br />然后：用189除以11得出的结果是17 + 2/11，也就是说余数是2。<br />最后：通过对应规则就可以知道余数2对应的数字是x。所以，这是一个合格的身份证号码。<br /><br />



