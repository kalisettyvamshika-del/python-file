print("===== CAMPUS EVENT FINANCIAL PLANNING =====")

# Get event expenses
venue = float(input("Enter venue cost: "))
equipment = float(input("Enter equipment cost: "))
catering = float(input("Enter catering cost: "))
transport = float(input("Enter transport cost: "))
certificate = float(input("Enter certificate cost: "))

# Calculate total expenses
total = venue + equipment + catering + transport + certificate

print("\nTotal Event Expense:", total)

# Get sponsorship amount
sponsorship = float(input("Enter sponsorship amount: "))

# Calculate sponsorship shortfall
if sponsorship >= total:
    shortfall = 0
else:
    shortfall = total - sponsorship

print("Sponsorship Shortfall:", shortfall)

# Get participant details
participants = int(input("Enter expected participants: "))

if participants > 0:

    # Calculate contribution per participant
    contribution = shortfall / participants

    print("Contribution per Participant:", contribution)

    # Calculate minimum registrations
    if shortfall == 0:
        minimum = 0
    else:
        minimum = participants

    print("Minimum Registrations Required:", minimum)

else:
    print("Invalid participant count")

# Display final report
print("\n===== EVENT FINANCIAL REPORT =====")
print("Total Expense:", total)
print("Sponsorship:", sponsorship)
print("Sponsorship Shortfall:", shortfall)

print("Thank You!")
