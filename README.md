# HomeWork5

#include <stdio.h>

#include <math.h>

int main() 

{
   
    double x = 0.4 * pow(10, -3);  // 0.4x10^-3
    
    double y = -0.875;
   
    double z = -0.475 * pow(10, -3);  // -0.475x10^-3
    
    printf("Исходные значения:\n");
    printf("x = %.6f\n", x);
    printf("y = %.6f\n", y);
    printf("z = %.6f\n", z);
    printf("\n");
    
    // Вычисление величины w
    double cos_x = cos(x);
    double cos_y = cos(y);
    double first_term = pow(fabs(cos_x * cos_y), 2);  // |cos(x)cos(y)|²
    
    double sum_squares = x*x + y*y + z*z;  // x² + y² + z²
    
    double second_term = sum_squares;  // (x² + y² + z²)
    
    double third_term = 2.0 / sum_squares;  // 2/(x² + y² + z²)
    
    double w = first_term + second_term + third_term;
    
    // Вывод результатов
    printf("Промежуточные вычисления:\n");
    printf("cos(x) = %.6f\n", cos_x);
    printf("cos(y) = %.6f\n", cos_y);
    printf("|cos(x)cos(y)|² = %.6f\n", first_term);
    printf("x² + y² + z² = %.6f\n", sum_squares);
    printf("2/(x² + y² + z²) = %.6f\n", third_term);
    printf("\n");
    printf("Результат:\n");
    printf("w = %.6f\n", w);
    
    return 0;
}
