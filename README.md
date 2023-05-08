# MSQ
Multiple Server Single Queue implementation using python
import numpy as np: This imports the NumPy library, which is a powerful library for numerical computations in Python.

np.random.seed(10): This sets the random seed for NumPy to ensure reproducibility of the simulation results.

class FastFoodRestaurant:: This defines a class called FastFoodRestaurant that represents a fast food restaurant simulation.

def init(self, num_servers):: This is the constructor of the FastFoodRestaurant class, which is called when an instance of the class is created. It takes the number of servers as an argument and initializes various attributes, such as num_servers, interarrivals, service_times, clocks, next_arrivals, next_departures, num_in_queue, times_of_arrival_in_queue, service_times_in_queue, total_delays, num_of_delays, customers_served, and server_statuses, with appropriate initial values.

def start(self):: This method simulates the events in the fast food restaurant until 50 customers are served. It repeatedly calls the simulate_next_event() method to simulate the next event.

def simulate_next_event(self):: This method simulates the next event in the fast food restaurant. It determines the next event (either an arrival or a departure) based on the minimum of the next arrival times and next departure times, and updates the simulation clock accordingly. It then calls the appropriate methods arrival() or departure() based on the event type, and updates the simulation state and attributes accordingly. Finally, it prints the current status of the simulation, such as server statuses, number of customers in the queue, total delay, next arrival time, and next departure times.

def arrival(self):: This method simulates an arrival event in the fast food restaurant. It updates the next arrival time, and if there is an available server, it updates the next departure time for that server. Otherwise, it adds the customer to the queue and records their arrival time and service time in the queue.

def departure(self, server_idx):: This method simulates a departure event from a specific server in the fast food restaurant. It updates the customer served count, releases the server by updating its status, and if there are customers in the queue, it dequeues the next customer and updates the next departure time for the server based on the service time of the dequeued customer. Otherwise, it sets the next departure time for the server to infinity.

The code at the end creates an instance of the FastFoodRestaurant class with a specific number of servers, and calls the start() method to begin the simulation.
