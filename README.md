
#include <cstdlib>
#include <iostream>

using namespace std;
void leerA();
void imprimirA();
void burbuja();

int A[5], i;

int main() {
	leerA();
	imprimirA();
	burbuja();
	cout << endl << "Datos Ordenado: ";
	imprimirA();

	return 0;

}

void leerA() {
	for (i = 0; i < 5; i++) {
		cout << "Inserta un dato: ";
		cin >> A[i];
	}
}

void imprimirA() {
	for (i = 0; i < 5; i++) {
		cout<<A[i] << " ";
	}
}

void burbuja() {
	int j, aux;
	for (i = 0; i < 4; i++) {
		for (j = i + 1; j < 5; j++) {
			if (A[j] < A[i]) {
				aux = A[i];
				A[i] = A[j];
				A[j] = aux;

			}

		}
	}
}


