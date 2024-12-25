# Start-up-python
Class 01
import time

# Mock functions to simulate switching
def switch_to_k_electric():
    print("Switched to K-Electric service.")

def switch_to_ups():
    print("Switched to UPS system.")

def toggle_power_source(current_source):
    if current_source == "K-Electric":
        print("Switching to UPS...")
        switch_to_ups()
        return "UPS"
    elif current_source == "UPS":
        print("Switching to K-Electric...")
        switch_to_k_electric()
        return "K-Electric"
    else:
        print("Invalid power source.")
        return current_source

# Main logic
if __name__ == "__main__":
    current_source = "K-Electric"  # Initial power source
    print(f"Current power source: {current_source}")
    
    while True:
        user_input = input("Enter 'toggle' to switch power source, or 'exit' to quit: ").strip().lower()
        if user_input == "toggle":
            current_source = toggle_power_source(current_source)
            print(f"Power source is now: {current_source}")
        elif user_input == "exit":
            print("Exiting the system. Goodbye!")
            break
        else:
            print("Invalid input. Please type 'toggle' or 'exit'.")
        time.sleep(1)  # To simulate a delay in operation



Functions:
switch_to_k_electric: Simulates switching to K-Electric power.
switch_to_ups: Simulates switching to UPS power.
toggle_power_source: Handles the logic for toggling between power sources.
Interactive Input: Allows the user to toggle power sources or exit the program.
