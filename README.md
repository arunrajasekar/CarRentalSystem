
class CarRentalSystem:

    def __init__(self):
        self.rates = {'Hatchback':10, 'Sedan':20, 'SUV':30}

    def displayFareList(self):
        for car in self.rates:
            print(car, self.rates[car])

    def calcRent(self):
        print("Enter the type of car and the no. of days to rent")
        cType = input()
        days = input()
        days = int(days)
        print(cType ,"- Fare for", days, "days -", self.rates[cType]*days)


crs = CarRentalSystem()

while(1):
    print("\nEnter option \n\n1. Display Cars and their rents\n2. Calculate rent for X days\n3. Exit\n")
    option = input()
    if option == '1':
        crs.displayFareList()
    if option == '2':
        crs.calcRent()
    if option == '3':
        quit()
