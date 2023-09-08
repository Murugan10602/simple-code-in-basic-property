# simple-code-in-basic-property
# Sample code for a basic to-do list app
tasks = []

while True:
    print("Options:")
    print("1. Add task")
    print("2. List tasks")
    print("3. Remove task")
    print("4. Exit")
    
    choice = input("Enter your choice: ")

    if choice == "1":
        task = input("Enter a task: ")
        tasks.append(task)
    elif choice == "2":
        for i, task in enumerate(tasks, 1):
            print(f"{i}. {task}")
    elif choice == "3":
        index = int(input("Enter the task number to remove: ")) - 1
        if 0 <= index < len(tasks):
            removed_task = tasks.pop(index)
            print(f"Removed task: {removed_task}")
        else:
            print("Invalid task number.")
    elif choice == "4":
        break
    else:
        print("Invalid choice. Please try again.")
