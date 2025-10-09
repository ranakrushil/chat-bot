order = [] 

print("FoodBot: Welcome to FoodBot! What would you like to order? (pizza/burger/drink)") print("Type 'summary' to see your order or 'quit' to exit.\n") 

while True: 
user_input = input("You: ").lower().strip() 

if user_input == "quit": 
        print("FoodBot: Here's your final order:")         for item in order: 
            print(f"- {item}")         print("FoodBot: Thanks for ordering! Have a tasty day!")         break 

elifuser_input == "summary":         if order: 
            print("FoodBot: Your current order:")             for item in order: 
                print(f"- {item}")         else: 
            print("FoodBot: Your order is empty.") 

elif "pizza" in user_input: 
        print("FoodBot: We have Margherita, Pepperoni, and Veggie pizzas.")         pizza_type = input("Which pizza would you like? ").lower().strip() 
print("FoodBot: Available toppings: extra cheese, olives, mushrooms.")         toppings = input("Choose your toppings (comma-separated): ").lower().strip()         order.append(f"{pizza_type.title()} Pizza with {toppings}")         print(f"FoodBot: {pizza_type.title()} pizza with {toppings} added to your order.") 

elif "burger" in user_input: 
        print("FoodBot: We offer Beef, Chicken, and Veggie burgers.")         burger_type = input("Which burger would you like? ").lower().strip()         print("FoodBot: Add-ons available: cheese, bacon, lettuce, tomato.")         addons = input("Choose your add-ons (comma-separated): ").lower().strip()         order.append(f"{burger_type.title()} Burger with {addons}")         print(f"FoodBot: {burger_type.title()} burger with {addons} added to your order.") 

elif "drink" in user_input or "drinks" in user_input: 
        print("FoodBot: Our drinks include Soda, Water, and Juice.")         drink = input("Which drink would you like? ").lower().strip()         size = input("Choose a size (small/medium/large): ").lower().strip()         order.append(f"{size.title()} {drink.title()}")         print(f"FoodBot: {size.title()} {drink.title()} added to your order.") 
     else:         print("FoodBot: Sorry, I didn’t understand. Please choose: pizza/burger/drink or type 'summary' or 'quit'.") 
