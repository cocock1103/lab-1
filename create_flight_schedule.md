

```python
import csv
```


```python
#file name
file_name = 'flight_schedule'
# csv first line
csv_header = [['tail_number', 'origin', 'destination', 'departure_time', 'arrival_time']]
# create file
fout = open(file_name, 'wt', newline='')
# create csv format writter as csvout
csvout = csv.writer(fout)
# write csv_header to file
csvout.writerows(csv_header)
```


```python
# tail number
tail_number = ['T1', 'T2', 'T3', 'T4', 'T5', 'T6']
```


```python
airplanes = [T1, T2, T3, T4, T5]
```


```python
#flight times
filght_times = {'time_AUS_DAL': 50, 'time_AUS_HOU': 45, 'time_DAL_HOU': 65}
```


```python
#ground times
ground_times = {'AUS_ground': 25, 'DAL_ground': 30, 'HOU_ground': 35}
```


```python
airport = {'HOU', 'DAL', 'AUS'}
```


```python
gate1 = Gate(AUS, 360) 
gate2 = Gate(DAL, 360)
gate3 = Gate(DAL, 360)
gate4 = Gate(HOU, 360)
gate5 = Gate(HOU, 360)
gate6 = Gate(HOU, 360)
```


```python
def military_time(minutestotal)
    hours = [minutestotal // 60]
    minutes = [minutestotal % 60]
    if len(hours) < 2:
    hours = '0'+ hours
    if len(minutes) < 2:
    minutes = minutes + '0'
return (hours + minutes)  
```


```python
def available_gate(arrival_time, airport)
    if (gate.airport = airport and gate.gatetime <= arrival_time)
    return gate
return none
```


```python
def available_gatetime(airport)
    available_time = 1500
    if ((gate.airport is airport and gate.gatetime <= available_time))
    return available_time
```


```python
def gate_airport(airport)
    if airport = AUS:
        return AUS_ground
    if airport = DAL：
        return = DAL_ground
    if airport = HOU:
        return = HOU_ground
```


```python
class Gate:
    def __init__(self,airport, available_time):
        self.airport = airport
        self.available_time = available_time
```


```python
class Airplane:
    def __init__(self,tail_number,origin,departure_time):
        self.tail_number = tail_number
        self.origin = origin
        self.departure_time = departure_time
```


```python
While True
if origin = DAL:
    aus_arrival = departure time + time_AUS_DAL
    hou_arrival = departure time + time_DAL_HOU
```


```python
finalgate = available_gate(AUS, aus_arrival_time)
```


```python
  if finalgate = None:
        finalgate = available_gate(HOU, hou_arrival_time)
```


```python
       if finalgate = None:
        gate_time = available_gatetime(HOU, AUS)
        departure_time_new = available_gatetime - time_AUS_HOU
        departure_time = departure_time_new
        airplaneorder()
        continue
```


```python
elif origin = AUS:
    dal_arrival = departure time + time_AUS_DAL
    hou_arrival = departure time + time_AUS_HOU
```


```python
finalgate = available_gate(DAL, dal_arrival_time)
```


```python
  if finalgate = None:
        finalgate = available_gate(HOU, hou_arrival_time)
```


```python
     if finalgate = None:
        gate_time = available_gatetime(DAL, HOU)
        departure_time_new = available_gatetime - time_DAL_HOU
        departure_time = departure_time_new
        airplaneorder()
        continue
```


```python
elif origin = HOU:
    dal_arrival = departure time + time_DAL_HOU
    aus_arrival = departure time + time_AUS_DAL
```


```python
finalgate = available_gate(AUS, aus_arrival_time)
```


```python
  if finalgate = None:
        finalgate = available_gate(DAL, dal_arrival_time)
```


```python
     if finalgate = None:
        gate_time = available_gatetime(AUS, HOU)
        departure_time_new = available_gatetime - time_AUS_HOU
        departure_time = departure_time_new
        airplaneorder()
        continue
```


```python
if arrival_time >= 1320
break
```


```python
#create list
create_flight =[Airplanes.tail_number,origin, finalgate.airport, military_time(departure_time), military_time(arrival_time)]
```


```python
#sort
flight_schedule.sort = (key = lambda x: x[0],x[3])
```


```python
print(flight_schedule)
```


```python
csvout.writerows(flight_schedule)
fout.close()
```
