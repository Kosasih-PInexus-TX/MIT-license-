Copyright (c) 2025 KOSASIH
PI NOT DOUL COIN
def toman_to_pi_converter_manual():
    """
    This program calculates the PI equivalent of a Toman amount based on the dollar rate entered by the user and
    a fixed PI to USD rate (1 PI = $314159).
    """
    print("OMID.7 Toman to PI Converter (Manual Rate Entry)")

    PI_IN_DOLLARS = 314159  # Constant: 1 PI = $314159

    try:
        # Get input from the user
        while True:  # Loop for valid dollar rate input
            try:
                dollar_rate = float(input("Please enter the current dollar rate (Toman): "))
                if dollar_rate > 0:
                    break  # Exit loop if valid input
                else:
                    print("Dollar rate must be a positive value.")
            except ValueError:
                print("Invalid input. Please enter a numeric value for the dollar rate.")

        while True:  # Loop for valid toman amount input
            try:
                toman_amount = float(input("Enter the amount in Toman: "))
                if toman_amount > 0:
                    break  # Exit loop if valid input
                else:
                    print("Toman amount must be a positive value.")
            except ValueError:
                print("Invalid input. Please enter a numeric value for the Toman amount.")



        # Perform calculations
        dollar_amount = toman_amount / dollar_rate  # Convert Toman to dollars
        pi_amount = dollar_amount / PI_IN_DOLLARS  # Convert dollars to PI (using fixed rate)

        # Display the result
        print(f"The PI equivalent (based on the entered rate) is: {pi_amount:.5f} PI")

    except Exception as e:  # Catch any unexpected errors
        print(f"An unexpected error occurred: {e}")


if name == "main":
    toman_to_pi_converter_manual()
