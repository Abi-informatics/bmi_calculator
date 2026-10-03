# bmi_calculator
A python BMI calculator that finds out your BMI and weight adjustment. 
def bmi_calculator(h,w):
    BMI=w/(h)**2
    print("Your BMI is:",BMI)
    if BMI<18.5:
        print("You are underweight.")
        gw=(18.5*h**2)-w
        print("Gain atleast",round(gw),"kilograms to attain healthy weight")
        return "Underweight" 
    elif BMI<25.0:
        print("You are in a healthy weight")
        return "Healthy weight"
    elif BMI<30.0:
        return "Overweight"
    elif BMI<35.0:
        return "Obesity class1"
    elif BMI<40.0:
         return "Obesity class2"
    else:
         return "Severe Obesity"
Choice =True
while Choice==True:
    print (" Check your BMI and category")
    He=float(input("Enter your height in meters:"))
    We=float(input("Enter your weight in kg :"))
    category=bmi_calculator(He,We)
    if category in ("Overweight","Obesity class1","Obesity class2","Severe Obesity"):
        print(category)
        lw=We-(24.9*He**2)
        print("Loss atleast",round(lw),"kgs to attain healthy weight")
    Choice=input("do you wish to continue(Y/N):")
    if Choice.lower()=="n":
        Choice =False
        print("Thank you")
    else:
        Choice=True
