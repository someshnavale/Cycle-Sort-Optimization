# Cycle-Sort-Optimization

(input)
output = 0
for cycleStart from 0 to length(array) - 2
 item = array[cycleStart]
 pos = cycleStart
 for i from cycleStart + 1 to length(array) - 1
 if array[i] < item:
 pos += 1
 if pos == cycleStart:
 continue
 while item == array[pos]:
 pos += 1
 array[pos], item = item, array[pos]
 writes += 1
 while pos != cycleStart:
 pos = cycleStart
 for i from cycleStart + 1 to length(array) - 1
 if array[i] < item:
 pos += 1
 while item == array[pos]:
 pos += 1
 array[pos], item = item, array[pos]
 writes += 1
return outout
