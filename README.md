# asked for the scores then divides to 3 to get the average
def studentAverage(first, second, third):
    average = (first + second + third) / 3
    return average
# asked for the average grade then decides using if else
# whether the grade has passed or failed
def gradeStatus(average):
    if average>=90:
        status="Excellent!"
    elif average>=80:
        status="Good job."
    elif average>=75:
        status = "Good."
    else:
        status = "Failed."
    return status

studentNumber = int(input("Students to be processed: "))

while studentNumber<3:
    print("Required student should be at least 3.")
    studentNumber = int(input("Students to be processed: "))

studentCount = 1

# using while loop and the condition
# where student number asked by the user
# and the student count that iterates
# everytime the condition in while sends true
while studentCount<=studentNumber:
    print("\nStudent", studentCount)
    studentName = input("Student Name: ")
    first = float(input("First Activity Score: "))
    second = float(input("Second Activity Score: "))
    third = float(input("Third Activity Score: "))
    
  # this computes the average of the score
    average = studentAverage(first, second, third)
  # this decides the status base on the average grade
    status = gradeStatus(average)
    
    print("\nAverage: ", round(average, 2))
    print("Status: ", status)
  # increments the student count so it won’t do unli loop
    studentCount = studentCount + 1

print("\nAll students have been processed.")
