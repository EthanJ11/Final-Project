# Code
Some of my previous code for an assignment.

    import math
    do_estimate = True
    while (do_estimate):
    
    	while (True): 
    		try:
    			square_feet = int(input("Square feet of wall space to be painted?: "))		
    			if (square_feet < 1):
    				print("Enter a number greater than 0.")
    				continue
    		except ValueError:
    			print("The value you entered is invalid. Only numerical values are valid.")
    		else:
    			break
    
    	while (True): 
    		try:
    			gallon_cost = float(input("How much per gallon does the paint cost?: "))
    			if (gallon_cost < 0.01):
    				print("Enter a number greater than 0.")
    				continue
    		except ValueError:
    			print("The value you entered is invalid. Only numerical values are valid.")
    		else:
    			break
    
    	required_gallons = math.ceil(square_feet / 350)
    	print('We will need to purchase', required_gallons, 'gallons of paint.')
    	
    	total_paint_cost = round(gallon_cost * required_gallons,2)
    	print('The total cost of paint will be: $'+str(total_paint_cost))
    	
    	painting_hours = round((square_feet / 350) * 6,1)
    	print('It will take', painting_hours, 'hours to paint.')
    	
    	labor_cost = round(painting_hours * 62.25,2)
    	print('The cost of labor will be: $'+str(labor_cost))
    	
    	overall_cost = total_paint_cost + labor_cost
    	print('The total cost of the paint job will be: $'+str(overall_cost))
    
    	another_calculation = input("Would you like another estimate? (y/n): ")
    	if (another_calculation != "y"):
    		do_estimate = False

---
[Back to home.](https://github.com/EthanJ11/Final-Project)
