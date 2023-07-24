# Python-To-Do-List
# lets import the tkinter module
import tkinter as tk

# create the empty gui
root = tk.Tk()

#lets define function
def add():
    print('Adding task in the list')
    # lets get the text written inside the text
    data = entry.get()
    if data:
       #  task_list.insert(0, data)
         task_list.insert(tk.END, data)
       # lets clean the entry widget
         entry.delete(0, tk.END)

def delete():
    print('Deleting the task')
#lets delete the taskfrom list
    task_list.delete(tk.ACTIVE)
#lets define the size
root.geometry('400x400')

# lets stop the resizing
root.resizable(width=False, height=False)

#lets change the title
root.title('To Do List')

#lets add entry widget
entry = tk.Entry(root)
entry.pack(padx=30, pady=12, fill='x')

#lets add a button
add_button = tk.Button(root, text='Add Task',width=20, bg='yellow', fg='green', command=add)
add_button.pack()
# lets add the task list
task_list = tk.Listbox(root)
task_list.pack(fill='x', padx=20,pady=20)

#lets add delete button
delete_button = tk.Button(root, text='Delete',width=20, bg='yellow', fg='green', command=delete)
delete_button.pack()
root.mainloop()
