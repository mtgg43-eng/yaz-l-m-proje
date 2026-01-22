# yaz-l-m-proje
c++ proje






#include <iostream>

using namespace std;

bool asalTespit(int sayi) {
    if (sayi < 2) return false;
    for (int i = 2; i * i <= sayi; i++) {
        if (sayi % i == 0) return false;
    }
    return true;
}

int main() {
    int limit = 10000000;
    int sayac = 0;
    int n;

    for (int n = 2; n <= limit - 4; n++) {
        if (asalTespit(n) && asalTespit(n + 4)) {
            sayac++;
        }
    }

    cout << "10 milyona kadar toplam kuzen asal sayisi: " << sayac << endl;

    return 0;
}
