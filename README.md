# Python-current-time-window


Here is a simple Python program that displays the current time in a window using the Tkinter library:
```
import tkinter as tk
import time

# Create a new Tkinter window
window = tk.Tk()

# Function to update the time display every second
def update_time():
  # Get the current time
  current_time = time.strftime("%I:%M:%S %p")

  # Update the time display label
  time_label.configure(text=current_time)

  # Call this function again in 1 second
  window.after(1000, update_time)

# Create a time display label
time_label = tk.Label(window, font=("Helvetica", 32))
time_label.pack()

# Start the time update loop
update_time()

# Start the Tkinter event loop
window.mainloop()
```
This code creates a new Tkinter window, adds a label to display the time, and then uses a function to update the time display every second. The time is formatted using the strftime function from the time module, and the Tkinter after method is used to call the update function every 1 second. You can customize this code to change the font, layout, or other aspects of the time display.
