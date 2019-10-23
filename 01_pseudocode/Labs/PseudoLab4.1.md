CHOOSE THREE PROMPTS (Plus mandatory ones if assigned)

============================================================
============================================================

Kilometer Converter
Design a modular program that asks the user to enter a distance in kilometers, and then converts that distance to miles. The conversion formula is as follows: Miles = Kilometers * 0.6214

MILESTOKM = .6214

Main()
    double dblMiles = RequestMiles()
    double dblKilometers = ConvertMilesToKilometers(dblMiles)
    Display "{0} miles is equal to {1} kilometers", dblMiles, dblKilometers
    
RequestMiles()
    Display "Enter the number of miles to convert to kilometers."
    return input
    
ConvertMilesToKilometers(double dblMiles = 0)
    return dblMiles * MILESTOKM

============================================================
============================================================

Sales Tax Program Refactoring (Mandatory)
See program below, the Sales Tax program. This program calculates and displays the county and state sales tax on a purchase. Refactor it so the subtasks are in modules.
// Variable declarations
Declare Real purchase, stateTax, countyTax, totalTax, totalSale

// Constants for the state and county tax rates
Constant Real STATE_TAX_RATE = 0.04
Constant Real COUNTY_TAX_RATE = 0.02

Main()
    GetPurchaseAmount()
    CalculateTaxAmounts()
    CalculateTotalSale()
    DisplaySaleData()
    
GetPurchaseAmount()
    Display "Enter the amount of the purchase."
    purchase = input

CalculateTaxAmounts()
    Set stateTax = purchase * STATE_TAX_RATE
    Set countyTax = purchase * COUNTY_TAX_RATE
    Set totalTax = stateTax + countyTax

CalculateTotalSale()
    // Calculate the total of the sale.
    Set totalSale = purchase + totalTax

DisplaySaleData()
    // Display information about the sale.
    Display "Purchase Amount: $", purchase
    Display "State Tax: ", stateTax
    Display "County Tax: ", countyTax
    Display "Total Tax: ", totalTax
    Display "Sale total: ", totalSale

============================================================
============================================================

Automobile Costs
Design a modular program that asks the user to enter the monthly costs for the following expenses incurred from operating his or her automobile: loan payment, insurance, gas, oil, tires, and maintenance. The program should then display the total monthly cost of these expenses, and the total annual cost of these expenses.

decimal decMonthlyCost, decAnnualCost, decMonthlyLoanPayment, decMonthlyInsuranceCost, 
    decMonthlyGasCost, decMonthlyOilCost, decMonthlyTiresCost, decMonthlyMaintenanceCost

Main()
    ObtainCosts()
    CalculateMonthlyCost()
    CalculateAnnualCost()
    DisplayData()
    
ObtainCosts()
    Display "Please enter your monthly loan payment cost."
    decMonthlyLoanPayment = input
    Display "Please enter your monthly insurance cost."
    decMonthlyInsuranceCost = input
    Display "Please enter your monthly gas cost."
    decMonthlyGasCost = input
    Display "Please enter your monthly oil cost."
    decMonthlyOilCost = input
    Display "Please enter your monthly tires cost."
    decMonthlyTiresCost = input
    Display "Please enter your monthly maintenance cost."
    decMonthlyMaintenanceCost = input

CalculateMonthlyCost()
    decMonthlyCost = decMonthlyLoanPayment + decMonthlyInsuranceCost + decMonthlyGasCost + 
        decMonthlyOilCost + decMonthlyTiresCost + decMonthlyMaintenanceCost

CalculateAnnualCost()
    const integer MONTHS_IN_YEAR = 12
    decAnnualCost = decMonthlyCost * MONTHS_IN_YEAR

DisplayData()
    Display "Your total monthly cost is {0}", decMonthlyCost
    Display "Your total annual cost is {0}", decAnnualCost

============================================================
============================================================

Hot Dog Cookout Calculator
Assume that hot dogs come in packages of 10, and hot dog buns come in packages of 8. Design a modular program that calculates the number of packages of hot dogs and the number of packages of hot dog buns needed for a cookout, with the minimum amount of leftovers. The program should ask the user for the number of people attending the cookout, and the number of hot dogs each person will be given. The program should display the following:
    The minimum number of packages of hot dogs required
    The minimum number of packages of buns required
    The number of hot dogs that will be left over
    The number of buns that will be left over

Const integer HOTDOGPACKAGE = 10
Const integer BUNPACKAGE = 8
integer intNumOfPeople
integer intHotDogCount
integer intHotDogCountReq
integer intHotDogPackageReq
integer intBunPackageReq

Main()
    CalcHotDogPackageCount()
    CalcBunPackageCount()
    DisplayData()
    
CalcHotDogPackageCount()
    intHotDogCountReq = intNumOfPeople * intHotDogCount
    intHotDogPackageReq = Roundup(intHotDogCountReq / HOTDOGPACKAGE)

CalcBunPackageCount()
    intBunPackageReq = Roundup(intHotDogCountReq / BUNPACKAGE)

DisplayData()
    Display "The minimum number of packages of hot dogs required is {0}", intHotDogPackageReq
    Display "The minimum number of packages of buns required {0}", intBunPackageReq
    Display "The number of hot dogs that will be left over {0}", Mod(intHotDogCountReq / HOTDOGPACKAGE)
    Display "The number of buns that will be left over {0}", Mod(intHotDogCountReq / BUNPACKAGE)

