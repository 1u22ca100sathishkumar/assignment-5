# assignment-5
1. Create a Student class and display student details using an object
    class Student {
    int rollNo;
    String name;
    int age;

    // Method to display details
    void display() {
        System.out.println("Roll No: " + rollNo);
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }

    public static void main(String[] args) {
        // Creating object
        Student s1 = new Student();

        // Assigning values
        s1.rollNo = 101;
        s1.name = "Arjun";
        s1.age = 20;

        // Displaying details
        s1.display();
    }
}
2. Create a parameterized constructor for Transport and display details
class Transport {
    String vehicleType;
    String number;
    String driverName;

    // Parameterized constructor
    Transport(String type, String num, String driver) {
        vehicleType = type;
        number = num;
        driverName = driver;
    }

    void display() {
        System.out.println("Vehicle Type: " + vehicleType);
        System.out.println("Number: " + number);
        System.out.println("Driver: " + driverName);
    }

    public static void main(String[] args) {
        // Creating object using parameterized constructor
        Transport t1 = new Transport("Bus", "TN23AB4567", "Ravi Kumar");

        t1.display();
    }
}

3. Program to simulate a Bank Account with Deposit and Withdraw methods
class BankAccount {
    String accountHolder;
    double balance;

    BankAccount(String name, double initialBalance) {
        accountHolder = name;
        balance = initialBalance;
    }

    // Deposit Method
    void deposit(double amount) {
        balance += amount;
        System.out.println("Deposited: " + amount);
        System.out.println("New Balance: " + balance);
    }

    // Withdraw Method
    void withdraw(double amount) {
        if (amount > balance) {
            System.out.println("Insufficient balance!");
        } else {
            balance -= amount;
            System.out.println("Withdrawn: " + amount);
            System.out.println("Remaining Balance: " + balance);
        }
    }

    void display() {
        System.out.println("Account Holder: " + accountHolder);
        System.out.println("Balance: " + balance);
    }

    public static void main(String[] args) {
        BankAccount acc = new BankAccount("Priya", 5000);

        acc.display();
        acc.deposit(2000);
        acc.withdraw(1500);
        acc.withdraw(7000); // will show insufficient balance
    }
}
