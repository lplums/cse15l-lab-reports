# Lab Report 2
## Part 1:

## Part 2:
Before 
```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
  ```
  
After:
`static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    int index = 0;
    for(int i = 0; i < arr.length; i++) {
      if(arr[i] < lowest) { lowest = arr[i]; index = i;}
    }
    double sum = 0;
    for(int i = 0; i < arr.length; i++) {
      if(i != index) { sum += arr[i]; }
    }
    return sum / (arr.length - 1);
  }`
  
  ## Part 3:
  
