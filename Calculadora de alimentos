#include <iostream>
#include <cmath>
#include <conio.h>

using namespace std;

float calcularCalorias(float peso, float altura, int edad, char genero, float factorActividad) 
{
    float resultado;

    if (genero == 'M' || genero == 'm') 
    {
        resultado = 66.0f + (13.7f * peso) + (5.0f * altura) - (6.8f * edad);
    } 
    else if (genero == 'F' || genero == 'f') 
    {
        resultado = 655.0f + (9.6f * peso) + (1.8f * altura) - (4.330f * edad);
    } 
    else 
    {
        cout << "Genero no valido. Por favor, ingrese 'M' o 'F'." << endl;
        return 0.0f;
    }

    return resultado * factorActividad;
}

float obtenerFactorActividad() 
{
    cout << "Seleccione el factor de actividad que realiza a la semana: " << endl;
    cout << "1.- Sedentario (poco o ningún ejercicio) -> 1.2" << endl;
    cout << "2.- Ligera actividad (ejercicio ligero o deportes 1-3 días a la semana) -> 1.37" << endl;
    cout << "3.- Moderada actividad (ejercicio moderado o deportes 3-5 días a la semana) -> 1.55" << endl;
    cout << "4.- Alta actividad (ejercicio intenso o deportes 6-7 días a la semana) -> 1.72" << endl;
    cout << "5.- Muy alta actividad (actividad física extenuante y trabajo físico diario o entrenamiento dos veces al día) -> 1.9" << endl;

    int eleccion;
    cout << "Ingrese el numero correspondiente a su eleccion: " << endl;
    cin >> eleccion;

    switch (eleccion) 
    {
        case 1:
            return 1.2f;
        case 2:
            return 1.37f;
        case 3:
            return 1.55f;
        case 4:
            return 1.72f;
        case 5:
            return 1.9f;
        default:
            cout << "Opcion no válida. Se utilizara el factor de actividad predeterminado (1.55)." << endl;
            return 1.55f;
    }
}

void recomendarComidas(float caloriasDiarias) 
{
    cout << "\nRecomendaciones de comidas:" << endl;

    if (caloriasDiarias < 1500) 
    {
        cout << "Desayuno: Yogur con frutas y granola" << endl;
        cout << "Almuerzo: Ensalada de atún" << endl;
        cout << "Comida: Ensalada de pollo a la parrilla" << endl;
        cout << "Cena: Salmon al horno con verduras asadas" << endl;
    } 
    else if (caloriasDiarias < 2000) 
    {
        cout << "Desayuno: Tostadas de pan integral con aguacate y huevo" << endl;
        cout << "Almuerzo: Ensalada de atún" << endl;
        cout << "Comida: Sándwich de pavo y queso con ensalada" << endl;
        cout << "Cena: Pasta integral con salsa de tomate y verduras" << endl;
    } 
    else 
    {
        cout << "Desayuno: Batido de proteínas con frutas y avena" << endl;
        cout << "Almuerzo: Ensalada de atún" << endl;
        cout << "Comida: Filete a la parrilla con papas asadas" << endl;
        cout << "Cena: Salmón al horno con brócoli al vapor" << endl;
    }
}

int main() 
{
    float peso, altura, factorActividad;
    int edad;
    char genero;

    cout << "Bienvenido a la calculadora de calorias diarias" << endl;

    cout << "Ingrese el peso en kg: ";
    cin >> peso;

    cout << "Ingrese la altura en cm: ";
    cin >> altura;

    cout << "Ingrese la edad en años: ";
    cin >> edad;

    cout << "Ingrese el genero (M/F): ";
    cin >> genero;

    factorActividad = obtenerFactorActividad();

    float caloriasDiarias = calcularCalorias(peso, altura, edad, genero, factorActividad);

    if (caloriasDiarias > 0.0f) 
    {
        cout << "Las calorias diarias estimadas son: " << caloriasDiarias << " kcal" << endl;
        recomendarComidas(caloriasDiarias);
        getch();
        system("pause");
    }

    return 0;
    getch();
    system("pause");
}
