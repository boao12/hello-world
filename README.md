# hello-world
def calculate_bmi():
    height = float(input("请输入您的身高（米）："))
    weight = float(input("请输入您的体重（公斤）："))
    bmi = weight / (height ** 2)
    return bmi

def bmi_category(bmi):
    if bmi < 18.5:
        return "偏瘦"
    elif 18.5 <= bmi < 24.9:
        return "正常"
    elif 24.9 <= bmi < 29.9:
        return "超重"
    else:
        return "肥胖"

bmi = calculate_bmi()
category = bmi_category(bmi)

print("您的BMI指数为：{:.2f}".format(bmi))
print("您的健康状态为：{}".format(category))

if category == "偏瘦":
    print("建议您增加营养摄入，适当进行锻炼。")
elif category == "正常":
    print("恭喜您，您的体重在正常范围内，请继续保持。")
elif category == "超重" or category == "肥胖":
    print("您的体重超出了正常范围，建议您控制饮食，增加运动量，以达到健康的体重。")
