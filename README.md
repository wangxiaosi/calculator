# calculator
本程序的核心思想就是显示还有运算进行分离，先进行显示比如输入3+3*3

操作顺序为 按钮3 按钮+ 按钮3 按钮* 按钮3 按钮=


前边五个按钮的工作就是正确显示式子，然后都赋值给textBox1.Text也就是屏幕显示的text文本

然后在 = 按钮中进行了大量工作，


第一步将获取的textBox1.Text的值然后分开为数字集合还有运算符号集合

第二步根据数字集合中数字的数量来判定是两个数字的计算，还是三个数字的计算

第三步根据数字数组内容还有符号数组内容进行列举式计算
第四步清空俩个数组，然后输出结果


注意点：

1.在程序中创建了两个数组，用来存放数字还有符号

double[] number_double = new double[10];//数字集合

string[] operator_string = new string[10];//运算符集合

int numberxiabiao_int = 0;//数字集合下标

int operatorxiabiao_int = 0;//运算符下标

  当清空数组的时候是将下标变为0
  
2.在进行开根号还有求倒数的计算就是对式子最后一个数字或者只有一个数字的情况进行结果输出例如

1+4*9的情况 进行 开根号操作 就变成 1+4*3

9 变成 3

开根号或者求倒数部分就是如果不止一个数字就将最后一个数字截取出来，然后开根号或者求倒数再放回去

3.小数按钮只是显示。在分开为数字集合还有符号集合的时候，已经通过遇到运算符才终止本数字的读取的方法来识别了。

4.关于程序健壮性

（1）不能连续输入两个运算符，或者小数点。实现部分位置，在运算符还有小数点输入按钮中，通过读取上一个符号是不是运算符或者小于号来实现。

（2）除法除数不能为0。实现部位位置，数字输入函数public void numclik(int num)


