+++
title = "Ada_Case"
slug = "../ada"
weight = 13
+++

_Ada case_ is the capital pattern with underscore delimiter.

## History

This php case conversion library calls this case "Ada". [^1]

[^1]: [github:jawira/case-converter](https://github.com/jawira/case-converter)

Ada's style guide acturally describes this case as follows: [^2]

> Use mixed case for all other identifiers, a capital letter beginning every word separated by underscores.

[^2]: [Ada Style Guide 3.1 Spelling: Capitalization](https://ada-lang.io/docs/style-guide/s3/01#capitalization)

## Example

Ada uses this case for most variables. 

```ada
type Second_Of_Day      is range 0 .. 86_400;
type Noon_Relative_Time is (Before_Noon, After_Noon, High_Noon);

subtype Morning   is Second_Of_Day range 0 .. 86_400 / 2 - 1;
subtype Afternoon is Second_Of_Day range Morning'Last + 2 .. 86_400;

Current_Time := Second_Of_Day(Calendar.Seconds(Calendar.Clock));
if Current_Time in Morning then
   Time_Of_Day := Before_Noon;
elsif Current_Time in Afternoon then
   Time_Of_Day := After_Noon;
else
   Time_Of_Day := High_Noon;
end if;
```
[^2]
