#include <iostream>
#include <string>
using namespace std;

class Carro {
    private:
        string marca;
        string modelo;
        int ano;
        float velocidadeInstantanea;  // Atributo privado
        
    public:
        // Construtor para inicializar o carro
        Carro(string m, string mod, int a) {
            marca = m;
            modelo = mod;
            ano = a;
            velocidadeInstantanea = 0.0;  // Inicia com velocidade zero
        }
        
        // Método público para acelerar
        void acelerar(float incremento) {
            velocidadeInstantanea += incremento;
            cout << "Acelerando... Velocidade atual: " << velocidadeInstantanea << " km/h" << endl;
        }
        
        // Método para exibir informações do carro
        void exibirInfo() {
            cout << "\n--- Informações do Carro ---" << endl;
            cout << "Marca: " << marca << endl;
            cout << "Modelo: " << modelo << endl;
            cout << "Ano: " << ano << endl;
            cout << "Velocidade final: " << velocidadeInstantanea << " km/h" << endl;
        }
};

int main() {
    // Criando um objeto Carro
    Carro meuCarro("Toyota", "Corolla", 2022);
    
    // Exibindo informações iniciais
    meuCarro.exibirInfo();
    
    cout << "\n--- Teste de Aceleração ---" << endl;
    
    // Acelerando o carro com diferentes taxas
    meuCarro.acelerar(20.5);   // Acelera 20.5 km/h
    meuCarro.acelerar(15.0);   // Acelera mais 15 km/h
    meuCarro.acelerar(30.0);   // Acelera mais 30 km/h
    
    // Exibindo informações finais com a velocidade acumulada
    meuCarro.exibirInfo();
    
    return 0;
}

