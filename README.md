# 查找正整数中最小数字（无函数，直接执行）
try:  # 新增try，与except配对，捕获非数字输入异常
    n = input("请输入整数：")
    num = int(n)  # 把字符串输入转为整数，用于判断是否为正整数
    if num <= 0:  # 用转换后的整数num判断，而非字符串n
        print("输入错误，请输入正整数！")
    else:
        min_digit = 9
        for i in range(len(n)):
            current_digit = int(n[i])
            if current_digit < min_digit:
                min_digit = current_digit
        print(f"{num}中最小的数字为：{min_digit}")  # 统一用num，与前面变量名匹配
except ValueError:
    print("输入错误，请输入数字！")
