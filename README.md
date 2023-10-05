#include<bits/stdc++.h>

using namespace std;

class CEmpleado {
public:
    string name;
    int yearOfJoining;
    double salary;
    string address;

    CEmpleado(string n, int y, double s, string a) {
        name = n;
        yearOfJoining = y;
        salary = s;
        address = a;
    }

    int getYearsOfService() {
        int currentYear = 2023; // Cambia este valor al año actual
        return currentYear - yearOfJoining;
    }

    bool livesOnWallStreet() {
        return (address.find("WallStreet") != string::npos);
    }

    void printInfo() {
        cout << name << "\t" << yearOfJoining << "\t" << address << endl;
    }
};

int main() {
    // Crear objetos CEmpleado para tres empleados
    CEmpleado empleado1("Robert", 2014, 0.0, "64C- WallStreet");
    CEmpleado empleado2("Alice", 2017, 0.0, "42D- Elm Street");
    CEmpleado empleado3("John", 2015, 0.0, "73A- WallStreet");

    // Imprimir la información de los empleados
    cout << "Name\tYear of joining\tAddress" << endl;
    empleado1.printInfo();
    empleado2.printInfo();
    empleado3.printInfo();

    // Calcular y mostrar los años de antigüedad
    cout << "Years of service:" << endl;
    cout << empleado1.name << ": " << empleado1.getYearsOfService() << " years" << endl;
    cout << empleado2.name << ": " << empleado2.getYearsOfService() << " years" << endl;
    cout << empleado3.name << ": " << empleado3.getYearsOfService() << " years" << endl;

    // Verificar si los empleados viven en la calle Wall Street
    cout << "Lives on Wall Street:" << endl;
    cout << empleado1.name << ": " << (empleado1.livesOnWallStreet() ? "Yes" : "No") << endl;
    cout << empleado2.name << ": " << (empleado2.livesOnWallStreet() ? "Yes" : "No") << endl;
    cout << empleado3.name << ": " << (empleado3.livesOnWallStreet() ? "Yes" : "No") << endl;

    return 0;
}
