import java.util.HashMap;
import java.util.Scanner;

class BankAccount {
    private String name;
    private String accountNo;
    private double balance;

    BankAccount(String name, String accountNo) {
        this.name = name;
        this.accountNo = accountNo;
        this.balance = 0;
    }

    void deposit(double amount) {
        balance += amount;
        System.out.println("₹" + amount + " Successfully Deposited!");
    }

    void withdraw(double amount) {
        if (amount > balance) {
            System.out.println("Insufficient Balance!");
        } else {
            balance -= amount;
            System.out.println("₹" + amount + " Successfully Withdrawn!");
        }
    }

    void showDetails() {
        System.out.println("\n---- Account Details ----");
        System.out.println("Name: " + name);
        System.out.println("Account Number: " + accountNo);
        System.out.println("Balance: ₹" + balance);
        System.out.println("-------------------------");
    }
}

public class BankApp {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        HashMap<String, BankAccount> accounts = new HashMap<>();

        while (true) {
            System.out.println("\n===== BANK MENU =====");
            System.out.println("1. Create Account");
            System.out.println("2. Deposit");
            System.out.println("3. Withdraw");
            System.out.println("4. Account Details");
            System.out.println("5. Exit");
            System.out.print("Enter choice: ");
            int choice = sc.nextInt();
            sc.nextLine();

            switch (choice) {
                case 1:
                    System.out.print("Enter Name: ");
                    String name = sc.nextLine();
                    System.out.print("Enter Account No: ");
                    String accNo = sc.nextLine();
                    accounts.put(accNo, new BankAccount(name, accNo));
                    System.out.println("Account Created Successfully!");
                    break;

                case 2:
                    System.out.print("Enter Account No: ");
                    accNo = sc.nextLine();
                    System.out.print("Enter amount: ");
                    double depositAmount = sc.nextDouble();
                    accounts.get(accNo).deposit(depositAmount);
                    break;

                case 3:
                    System.out.print("Enter Account No: ");
                    accNo = sc.nextLine();
                    System.out.print("Enter amount: ");
                    double withdrawAmount = sc.nextDouble();
                    accounts.get(accNo).withdraw(withdrawAmount);
                    break;

                case 4:
                    System.out.print("Enter Account No: ");
                    accNo = sc.nextLine();
                    accounts.get(accNo).showDetails();
                    break;

                case 5:
                    System.out.println("Thank you for using the banking system!");
                    sc.close();
                    return;

                default:
                    System.out.println("Invalid Input! Try Again!");
            }
        }
    }
}
