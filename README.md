# Funciones
Codigo 1 de Funciones en C

#include<stdio.h>
float calcBmi(float h, float w);
float calcWi(float i, float h);

int main(){

    float height;
    float weight;
    float bmi;
    float wi;


    printf("Enter your height in m: ");
    scanf("%f",&height);


    printf("Enter your weight in kgs: ");
    scanf("%f",&weight);


    bmi=calcBmi(height,weight);


    printf("Your body mass index is %.2f kg/m^2 \n",bmi);

    if (bmi < 18.5){
        printf("You're thin \n");
        wi = calcWi(18.5, height);
        printf("your ideal weight is: %.2f", wi);
    }
    else if (bmi >= 18.5 && bmi <= 24.9){
        printf("You're in a normal weigth");
    }
    else if (bmi >= 25.0 && bmi <= 29.9){
        printf("you're overweight \n");
        wi = calcWi(24.9, height);
        printf("your ideal weight is: %.2f", wi);
    }
    else {
        printf("you're obese \n");
        wi = calcWi(24.9, height);
        printf("your ideal weight is: %.2f", wi);
    }
}


float calcBmi(float h,float w){
    float bmi;
    bmi=w/(h*h);
    return bmi;
}
float calcWi(float i, float h){
    float wi;
    wi = i * (h*h);
    return wi;
}
