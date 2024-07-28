# data-structures
#assignmnet
#excercise 1
numbers = [5, 2, 9, 1, 7, 3]
numbers.sort()
print(numbers)

#output
#[1, 2, 3, 5, 7, 9]


#excercise 2
my_list = [5, 2, 9, 1, 7, 3]

my_list.reverse()

print("Reversed list using reverse():", my_list)

reversed_list = my_list[::-1]

print("Reversed list using slicing:", reversed_list)

#output
Reversed list using reverse(): [3, 7, 1, 9, 2, 5]
Reversed list using slicing: [5, 2, 9, 1, 7, 3]


#excercise 3
class PhoneBook:
    def __init__(self):
        self.contacts = {}

    def add_contact(self, name, phone_number):
        self.contacts[name] = phone_number
        print(f"Added contact: {name} with phone number: {phone_number}")

    def remove_contact(self, name):
        if name in self.contacts:
            del self.contacts[name]
            print(f"Removed contact: {name}")
        else:
            print(f"Contact {name} not found in the phone book.")

    def lookup_contact(self, name):
        if name in self.contacts:
            print(f"{name}'s phone number is {self.contacts[name]}")
        else:
            print(f"Contact {name} not found in the phone book.")

    def display_all_contacts(self):
        if self.contacts:
            print("Phone Book Contacts:")
            for name, phone_number in self.contacts.items():
                print(f"Name: {name}, Phone Number: {phone_number}")
        else:
            print("The phone book is empty.")
phone_book = PhoneBook()
phone_book.add_contact("ukrish", "773-456-7890")
phone_book.add_contact("flynn", "730-765-4321")
phone_book.lookup_contact("ukrish")
phone_book.display_all_contacts()
phone_book.remove_contact("flynn")
phone_book.display_all_contacts()


#excercise 4
#game1 = {'ukrish', 'abi', 'hari', 'kailas'}
#game2 = {'Otis', 'ukrish', 'Ruby'}
#game3 = {'walter', 'hank', 'ukrish'}

#common_players = game1.intersection(game2).intersection(game3)


#print("Common players who can participate in all the games:", common_players)

#output
#Common players who can participate in all the games: {'ukrish'}


#Excercise 5
def is_palindrome(s):
    s = s.lower()
    s = ''.join(filter(str.isalnum, s))
    return s == s[::-1]

input_string = input("Enter a string to check if it is a palindrome: ")

if is_palindrome(input_string):
    print(f'"{input_string}" is a palindrome.')
else:
    print(f'"{input_string}" is not a palindrome.')

   # output
    # Enter a string to check if it is a palindrome: LEVEL
# "LEVEL" is a palindrome.

