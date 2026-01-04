We have the usual If-Else and Switch controls.

## Switch
```
int day = 3;
switch (day) {
	case 1: ...; break;
	case 2: ...; break;
	case 3: ...; break;
}
```

`break` required to stop further checking. Each case is like a if statement.

## goto
Another way to control the flow of programs (although not recommended) is using goto.
The program is "harder to understand and maintain" with goto statements.
```
	int x = 5;
	if (x == 5)
		goto label;
	
	std::cout << "This line is skipped" << std::endl;

label:
	std::cout << "This line is executed" << std::endl;
```