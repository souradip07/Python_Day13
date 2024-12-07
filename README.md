# Python_Day13
#Here's an example that combines classes, objects, methods, and attributes to create a simple class representing an electrical circuit:
class ElectricalCircuit:
    def __init__(self, resistors=None, capacitors=None, inductors=None):
        self.resistors = resistors if resistors else []
        self.capacitors = capacitors if capacitors else []
        self.inductors = inductors if inductors else []
    
    def add_resistor(self, value):
        self.resistors.append(value)
    
    def add_capacitor(self, value):
        self.capacitors.append(value)
    
    def add_inductor(self, value):
        self.inductors.append(value)
    
    def total_resistance(self):
        return sum(self.resistors)
    
    def total_capacitance(self):
        # Assuming capacitors in parallel for simplicity
        return sum(self.capacitors)
    
    def total_inductance(self):
        # Assuming inductors in series for simplicity
        return sum(self.inductors)

# Example usage:
circuit = ElectricalCircuit()
circuit.add_resistor(10)
circuit.add_resistor(5)
circuit.add_capacitor(0.001)
circuit.add_inductor(0.01)
circuit.add_inductor(0.02)
print(f"Total Resistance: {circuit.total_resistance()} ohms")
print(f"Total Capacitance: {circuit.total_capacitance()} farads")
print(f"Total Inductance: {circuit.total_inductance()} henries")

#Activities: Create a Class to Represent an Electrical Circuit
class ElectricalCircuit:
    def __init__(self, resistors=None, capacitors=None, inductors=None):
        self.resistors = resistors if resistors else []
        self.capacitors = capacitors if capacitors else []
        self.inductors = inductors if inductors else []
    
    def total_resistance(self):
        return sum(self.resistors)
    
    def total_capacitance(self):
        # For simplicity, assuming capacitors in parallel
        return sum(self.capacitors)
    
    def total_inductance(self):
        # For simplicity, assuming inductors in series
        return sum(self.inductors)
    
    def add_resistor(self, value):
        self.resistors.append(value)
    
    def add_capacitor(self, value):
        self.capacitors.append(value)
    
    def add_inductor(self, value):
        self.inductors.append(value)

# Example usage:
circuit = ElectricalCircuit()
circuit.add_resistor(10)
circuit.add_capacitor(0.001)
circuit.add_inductor(0.01)
print(f"Total Resistance: {circuit.total_resistance()} ohms")
print(f"Total Capacitance: {circuit.total_capacitance()} farads")
print(f"Total Inductance: {circuit.total_inductance()} henries")

#Project: Build an Object-Oriented System for Circuit Simulation
class Resistor:
    def __init__(self, resistance):
        self.resistance = resistance

class Capacitor:
    def __init__(self, capacitance):
        self.capacitance = capacitance

class Inductor:
    def __init__(self, inductance):
        self.inductance = inductance

class Circuit:
    def __init__(self):
        self.components = []
    
    def add_component(self, component):
        self.components.append(component)
    
    def total_resistance(self):
        return sum(c.resistance for c in self.components if isinstance(c, Resistor))
    
    def total_capacitance(self):
        return sum(c.capacitance for c in self.components if isinstance(c, Capacitor))
    
    def total_inductance(self):
        return sum(c.inductance for c in self.components if isinstance(c, Inductor))

# Example usage:
circuit = Circuit()
circuit.add_component(Resistor(10))
circuit.add_component(Capacitor(0.001))
circuit.add_component(Inductor(0.01))
print(f"Total Resistance: {circuit.total_resistance()} ohms")
print(f"Total Capacitance: {circuit.total_capacitance()} farads")
print(f"Total Inductance: {circuit.total_inductance()} henries")
