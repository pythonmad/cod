def NumberOfCity():


    user_input = input("Enter Your number : " )


    if len(user_input) > 11:
        print("Invalid input , please Try again")
        
    else:
        if user_input[:4] == "0919":
            print('Qom')
            
        elif user_input[:4] == '0936':
            print('Tehran')
        
        elif user_input[:4] == '0912':
            print('kashan')
        elif user_input == '0910':
            print('esfahan')
        else:
            print('another city')


NumberOfCity()
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
import math

class Cylinder:
    def __init__(self, radius, height):
        self.radius = radius
        self.height = height

    def surface_area(self):
        base_area = math.pi * self.radius ** 2
        side_area = 2 * math.pi * self.radius * self.height
        return 2 * base_area + side_area

# استفاده از کلاس Cylinder برای محاسبه مساحت استوانه
radius = float(input("شعاع دایره را وارد کنید: "))
height = float(input("ارتفاع استوانه را وارد کنید: "))
cylinder = Cylinder(radius, height)
print(f"مساحت استوانه برابر است با: {cylinder.surface_area()}")

,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,
def validate_national_id(national_id):

    if len(national_id) != 10 or not national_id.isdigit():
        return False

    check_digit = int(national_id[-1])
    weights = range(10, 1, -1)
    sum_digits = sum(int(national_id[i]) * weights[i] for i in range(9))
    remainder = sum_digits % 11

    if (remainder < 2 and check_digit == remainder) or (remainder >= 2 and check_digit == 11 - remainder):
        return True
    else:
        return False


national_id = input("lotfan code meli ra vared konid")

if validate_national_id(national_id):
    print("code motabar ast")
else:
    print("code motabar nist")












