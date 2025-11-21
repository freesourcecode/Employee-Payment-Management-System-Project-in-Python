# Employee Payment Management System Project in Python

The **Employee Payment Management System Project in Python** is essentially desktop software developed using Pycharm and Tkinter platforms.

To create an **Employee Payment Management System Project in Python**. Make sure you have PyCharm IDE installed on your computer.

By the way, if you are new to Python programming and don’t know what Python IDE to use, I have here a list of the Best Python IDE for Windows, Linux, and Mac OS that will suit you.

## How to create an Employee Payment Management System Project in Python.

1. **Create a Project Name**

First step open the PyCharm IDE and click “File” and select “New Project” and then create a project name after that click the “create” button.

2. **Create a Python File**

In the second step after creating a project name, “right” click the project name and then click “New.” After that choose “Python File”.

<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/43c3a4bc-b988-4ea3-a645-ae95437ad044" />

3. **Name the Python File**

The third step after choosing Python File name the file “Employee-Payment-System” and then click “Enter”.

<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/9bcaac5a-8d7e-4d14-a85e-113d17ac8eee" />

4. **Creating a File name in the Employee Payment Management System**

Now you can start coding, you are free to copy the code that being provided below.

### Example Codes of Employee Payment Management System

*  **Whole Frame Window**

```
root = Tk()
root.title("Employee Payment System")
root.geometry('1370x720+0+0')
root.maxsize(width=1370, height=720)
root.minsize(width=1370, height=720)
root.configure(background="dark gray")

Tops = Frame(root, width=1350, height=50, bd=8, bg="dark blue")
Tops.pack(side=TOP)

f1 = Frame(root, width=600, height=600, bd=8, bg="dark gray")
f1.pack(side=LEFT)
f2 = Frame(root, width=300, height=700, bd=8, bg="dark blue")
f2.pack(side=RIGHT)

fla = Frame(f1, width=600, height=200, bd=8, bg="dark blue")
fla.pack(side=TOP)
flb = Frame(f1, width=300, height=600, bd=8, bg="dark blue")
flb.pack(side=TOP)

lbl_information = Label(Tops, font=('arial', 45, 'bold'), text="Employee Payment Management System ", relief=GROOVE, bd=10, bg="Dark Gray", fg="Black")
lbl_information.grid(row=0, column=0)
```

* **Exit Function**

```
def Exit():
wayOut = tkinter.messagebox.askyesno("Employee Payment System", "Do you want to exit the system")
if wayOut > 0:
root.destroy()
return
```
### Reset Function 

```
def Reset():
FullName.set("")
Address.set("")
Wrk_Hrs.set("")
Hrs_Wage.set("")
Payable.set("")
Taxable.set("")
NetPayable.set("")
GrossPayable.set("")
OverTimeBonus.set("")
CompanyAgency.set("")
PhoneNumber.set("")
txtPaymentSlip.delete("1.0", END)
```

* **View Payslips**

```
def InformationEntry():
txtPaymentSlip.delete("1.0", END)
txtPaymentSlip.insert(END, "\t\tPay Slip\n\n")
txtPaymentSlip.insert(END, "Full Name :\t\t" + FullName.get() + "\n\n")
txtPaymentSlip.insert(END, "Home Address :\t\t" + Address.get() + "\n\n")
txtPaymentSlip.insert(END, "Company/Agency :\t\t" + CompanyAgency.get() + "\n\n")
txtPaymentSlip.insert(END, "Phone Number :\t\t" + PhoneNumber.get() + "\n\n")
txtPaymentSlip.insert(END, "Hours Worked :\t\t" + Wrk_Hrs.get() + "\n\n")
txtPaymentSlip.insert(END, "Net Payable :\t\t" + NetPayable.get() + "\n\n")
txtPaymentSlip.insert(END, "Wages per hour :\t\t" + Hrs_Wage.get() + "\n\n")
txtPaymentSlip.insert(END, "Tax Paid :\t\t" + Taxable.get() + "\n\n")
txtPaymentSlip.insert(END, "Payable :\t\t" + Payable.get() + "\n\n")
```

* **Calculation of Payments of weekly wages**

```
def WagesForWeekly():
txtPaymentSlip.delete("1.0", END)
hrs_wrk_per_wek = float(Wrk_Hrs.get())
hrs_per_wgs = float(Hrs_Wage.get())

DuePayment = hrs_per_wgs * hrs_wrk_per_wek
PaymentDue = "P" + str('%.2f' % DuePayment)
Payable.set(PaymentDue)

tax = DuePayment * 0.12
taxable = "P" + str('%.2f' % tax)
Taxable.set(taxable)

PaymentNet = DuePayment - tax
NetPayments = "P" + str('%.2f' % PaymentNet)
NetPayable.set(NetPayments)

if hrs_wrk_per_wek > 40:
HoursTimeOver = (hrs_wrk_per_wek - 40) + hrs_per_wgs * 1.5
OverTime = "P" + str('%.2f' % HoursTimeOver)
OverTimeBonus.set(OverTime)
elif hrs_wrk_per_wek <= 40:
PaymentOverTime = (hrs_wrk_per_wek - 40) + hrs_per_wgs * 1.5
HoursOverTime = "P" + str('%.2f' % PaymentOverTime)
OverTimeBonus.set(HoursOverTime)
return
```

* **Declaring Variables Function**

```
FullName = StringVar()
Address = StringVar()
Hrs_Wage = StringVar()
Wrk_Hrs = StringVar()
Payable = StringVar()
Taxable = StringVar()
NetPayable = StringVar()
GrossPayable = StringVar()
OverTimeBonus = StringVar()
CompanyAgency = StringVar()
PhoneNumber = StringVar()
TimeOfOrder = StringVar()
DateOfOrder = StringVar()
DateOfOrder.set(time.strftime("%d/%m/%Y"))
```

### Output:

<img width="1024" height="543" alt="image" src="https://github.com/user-attachments/assets/83d37283-18e0-4273-9824-bb321f46f330" />

### 📌 Here's the full documentation for the [Employee Payment Management System Project in Python](https://itsourcecode.com/free-projects/python-projects/employee-payment-management-system-project-in-python/)


