# Cpp-practice-exercises
//*Programación orientada a objetos cpp segundo semestre, profesor Daniel Capera
*//

//mediana en un arreglo
#include <iostream>
#include <algorithm>
using namespace std;

int main() {
    int arr[] = {5, 2, 9, 1, 7};
    int n = sizeof(arr)/sizeof(arr[0]);
    sort(arr, arr + n);
    float mediana = (n % 2 == 0) ? (arr[n/2 - 1] + arr[n/2]) / 2.0 : arr[n/2];
    cout << "Mediana: " << mediana << endl;
}

//2. transpuesta de matriz 

#include <iostream>
using namespace std;

int main() {
    int mat[2][3] = {{1,2,3},{4,5,6}};
    for (int j = 0; j < 3; j++) {
        for (int i = 0; i < 2; i++)
            cout << mat[i][j] << " ";
        cout << endl;
    }
}

//3. Inventario simple 

#include <iostream>
using namespace std;

int main() {
    string productos[] = {"Pan", "Leche", "Huevos"};
    int stock[] = {10, 5, 12};
    for (int i = 0; i < 3; i++)
        cout << productos[i] << ": " << stock[i] << endl;
}

//4. Ordenado por selección 

#include <iostream>
using namespace std;

int main() {
    int arr[] = {64, 25, 12, 22, 11}, n = 5;
    for (int i = 0; i < n-1; i++) {
        int min = i;
        for (int j = i+1; j < n; j++)
            if (arr[j] < arr[min]) min = j;
        swap(arr[i], arr[min]);
    }
    for (int i = 0; i < n; i++) cout << arr[i] << " ";
}

//5. elementos duplicados 

#include <iostream>
using namespace std;

int main() {
    int arr[] = {1, 2, 3, 2, 4, 1}, n = 6;
    for (int i = 0; i < n; i++)
        for (int j = i+1; j < n; j++)
            if (arr[i] == arr[j]) cout << "Duplicado: " << arr[i] << endl;
}
