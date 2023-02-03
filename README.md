
#include <iostream>

int main() {
  double capital = 1000.0;
  double interestRate = 0.05;
  double paymentPercentage = 0.1;
  int paymentNumber = 1;
  
  while (capital > 0) {
    double interest = capital * interestRate;
    double paymentAmount = capital * paymentPercentage;
    capital = capital + interest - paymentAmount;
    
    std::cout << "Payment #" << paymentNumber << ": ";
    std::cout << "Interest = " << interest << ", ";
    std::cout << "Payment Amount = " << paymentAmount << ", ";
    std::cout << "Remaining Capital = " << capital << std::endl;
    
    interestRate = interestRate * 1.05;
    paymentNumber++;
  }
  
  std::cout << "Total number of payments: " << paymentNumber - 1 << std::endl;
  
  return 0;
}
