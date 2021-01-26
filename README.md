# ATM-Project
# Mock ATM system to practice applying Python code

while True:
    balance = 1000
    print ("   ATM   ")
    print ("""
    1)  Current Balance
    2)  Withdrawal
    3)  Deposit
    4)  Quit
    """)
    try:
        Option = int(input("Enter Option: "))
    except Exception as e:
        print("Error", e)
        print("Enter 1,2,3,or 4 only")
        continue
    if Option == 1:
        print("Current Balance $ ", balance)
    if Option == 2:
        print("Current Balance $ ", balance)
        Withdrawal = float(input("Enter withdrawal amount $ "))
        if Withdrawal > 0:
            forwardbalance = (balance - withdrawal)
            print("New Balance $ ", forwardbalance)
        elif Withdrawal > balance:
            print("Insufficient Funds")
        else:
            print("No Withdrawal Made")
    if Option == 3:
        print("Current Balance $ ", balance)
        deposit = float(input("Enter Deposit Amount $ "))
        if deposit > 0:
            forwardbalance = (balance + deposit)
            print("New Balance $ ", forwardbalance)
        else:
            print("No Deposit Made")
        if Option == 4:
            exit()
