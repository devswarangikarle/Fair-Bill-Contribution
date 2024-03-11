# Fair-Bill-Contribution
Seven colleagues eagerly gathered for a memorable team dinner at a luxurious restaurant. Laughter filled the air, and the excitement grew with each passing moment. As the dishes arrived, they indulged in a feast, savoring every bite. However, when the moment of truth arrived, they were taken aback. 


#include <iostream>
#include <iomanip>
#include <vector>
#include <cmath>

using namespace std;

double fair_distribution(int n, const vector<int>& prices) {
    double total_cost = 0;
    for (int price : prices) {
        total_cost += price;
    }

  
    double contribution_per_person = total_cost / 7;

    return round(contribution_per_person * 100) / 100; 
}

int main() {
   
    int n;
    cin >> n;

    vector<int> prices(n);
    for (int i = 0; i < n; ++i) {
        cin >> prices[i];
    }

    
    double result = fair_distribution(n, prices);
    cout << fixed << setprecision(2) << result << endl;

    return 0;
}
