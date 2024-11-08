
class ATM:
    def __init__(self):
        self.balance = 0.0

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"${amount:.2f} deposited successfully.")
        else:
            print("Invalid amount. Please enter a positive number.")

    def check_balance(self):
        print(f"Your current balance is: ${self.balance:.2f}")

    def run(self):
        while True:
            print("\nWelcome to First Bank!")
            print("1. Deposit Money")
            print("2. Check Balance")
            print("3. Exit")

            option = input("Please choose an option (1-3): ")

            if option == '1':
                try:
                    amount = float(input("Enter the amount to deposit: "))
                    self.deposit(amount)
                except ValueError:
                    print("Invalid input. Please enter a numeric value.")
            elif choice == '2':
                self.check_balance()
            elif choice == '3':
                print("Thank you for using the ATM. Goodbye!")
                break
            else:
                print("Invalid choice. Please select a valid option.")

if __name__ == "__main__":
    atm = ATM()
    atm.run()
