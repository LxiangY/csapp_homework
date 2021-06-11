# csapp_homework
## first
## second
2.32:
the buggy code
```c
int tsub_ok(int x, int y){
  return tadd_ok(x, -y);
}
```
because tmin + tmin = 0
so if y = tmin, -y = tmin too
when y = tmin, we hope when x > 0 it return true
but it is when x < 0, it will return true
the corrected code
```c
int tsub_ok(int x, int y){
	if(y == pow(2,w)){
		return x<=0;
	}
	else{
		return tadd_ok(x,-y);
	}
}
```

