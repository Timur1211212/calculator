# Калькулятор
#include <iostream>
using namespace std;

class Calculator
{
private:
    double num1;
    double num2;
public:
        bool set_num1(double num1)
        {if (num1 == 0){return false;}            
            this->num1 = num1;
            return true;}

        bool set_num2(double num2)
        {if (num2 == 0) {return false;}
                this->num2 = num2;
                return true;}

            double add() { cout << "num1 + num2 = " << num1 + num2 << endl; return num1 + num2; }
            double multiply() { cout << "num1 * num2 = " << num1 * num2 << endl; return num1 * num2; }
            double subtract_1_2() { cout << "num1 - num2 = " << num2 - num1 << endl; return num2 - num1; }
            double subtract_2_1() { cout << "num2 - num1 = " << num1 - num2 << endl; return num1 - num2; }
            double divide_1_2() { cout << "num1 / num2 = " << num1 / num2 << endl; return num1 / num2; }
            double divide_2_1() { cout << "num2 / num1 = " << num2 / num1 << endl; return num2 / num1; }
    };

int main(){
    setlocale(LC_ALL, "rus");
    Calculator calculator;
    double num1 = 0;
    double num2 = 0;
        do {
            cout << "Введите num1 : ";
            cin >> num1;
            cout << "Введите num2 : ";
            cin >> num2;
            if (num1 == 0) { cout << "Неверный ввод!\n"; cout << "Введите num1: "; cin >> num1; }
            else if (num2 == 0) { cout << "Неверный ввод!\n"; cout << "Введите num2: "; cin >> num2; }
        } while (calculator.set_num1(num1),
            calculator.set_num2(num2),
            calculator.add(),
            calculator.multiply(),
            calculator.subtract_1_2(),
            calculator.subtract_2_1(),
            calculator.divide_1_2(),
            calculator.divide_2_1());
}