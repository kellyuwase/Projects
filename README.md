# Projects
'''
CS 5001
Spring 2022-Online
Homework 3
ATM
Kelly Uwase Rubangura
'''

'''
atm() function takes an amount as parameter and output
the amount of bills or coins
needed to dispense that amount.

Divident: used to determine how many of
each bill or coins should
be dispensed using //. The value is updated
as we go through each denomination.

Amount: Amount is updated as we go through
each denomination.

If loop: check if the divident is bigger than one
to determine if it is printing
multiple of that denomination.

elif: check if divident is equal to one to
determine if it is printing
just a single of that denomination.


'''


def atm(amount):

    fifty_dollars = 50

    twenty_dollars = 20

    ten_dollars = 10

    five_dollars = 5

    two_dollars = 2

    one_dollar = 1

    quarter = 0.25

    ten_cents = 0.10

    five_cents = 0.05

    divident = amount // fifty_dollars

    amount = amount % fifty_dollars

    if divident > 1:

        print(int(divident), "fifties")

    elif divident == 1:

        print(int(divident), "fifty")

    divident = amount // twenty_dollars

    amount = amount % twenty_dollars

    if divident > 1:

        print(int(divident), "twenties")

    elif divident == 1:

        print(int(divident), "twenty")

    divident = amount // ten_dollars

    amount = amount % ten_dollars

    if divident > 1:

        print(int(divident), "tens")

    elif divident == 1:

        print(int(divident), "ten")

    divident = amount // five_dollars

    amount = amount % five_dollars

    if divident > 1:

        print(int(divident), "fives")

    elif divident == 1:

        print(int(divident), "five")

    divident = amount // two_dollars

    amount = amount % two_dollars

    if divident > 1:

        print(int(divident), "toonies")

    elif divident == 1:

        print(int(divident), "toony")

    divident = amount // one_dollar

    amount = round(amount % one_dollar, 2)

    if divident > 1:

        print(int(divident), "loonies")

    elif divident == 1:

        print(int(divident), "loony")

    divident = amount // quarter

    amount = round(amount % quarter, 2)

    if divident > 1:

        print(int(divident), "quarters")

    elif divident == 1:

        print(int(divident), "quarter")

    divident = amount // ten_cents

    amount = round(amount % ten_cents, 2)

    if divident > 1:

        print(int(divident), "dimes")

    elif divident == 1:

        print(int(divident), "dime")

    divident = amount // five_cents

    amount = amount % five_cents

    if divident > 1:

        print(int(divident), "nickels")

    elif divident == 1:

        print(int(divident), "nickel")


def main():

    '''
    input_request: float

    round_to_nickel: Have to round the amount to the
    nearest nickel for better precesion

    Convert the amount from float to int

    call on atm() funnction with the amount as parameter

    '''

    input_request = float(input("Input request: "))

    round_to_nickel = round(input_request * 2, 1) / 2

    amount_int = round(round_to_nickel * 100)

    amount = int(amount_int) / 100

    atm(amount)


if __name__ == "__main__":
    main()
