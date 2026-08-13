students = {}

while True:
    print("\n1. Add Student")
    print("2. View Students")
    print("3. Search Student")
    print("4. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        roll = input("Enter roll number: ")
        name = input("Enter student name: ")
        marks = float(input("Enter marks: "))

        students[roll] = [name, marks]
        print("Student added successfully")

    elif choice == 2:
        for roll, data in students.items():
            print("Roll:", roll, "Name:", data[0], "Marks:", data[1])

    elif choice == 3:
        roll = input("Enter roll number: ")

        if roll in students:
            print("Name:", students[roll][0])
            print("Marks:", students[roll][1])
        else:
            print("Student not found")

    elif choice == 4:
        print("Thank you!")
        break

    else:
        print("Invalid choice")
