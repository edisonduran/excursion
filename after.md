---
Title: '.after'
Description: 'Compare wheter the current instance of Calendar occurs after the time represented by the specified Object.'
Subjects:
  - 'Computer Science'
Tags:
  - 'Classes'
  - 'Date'
  - 'Methods'
CatalogContent:
  - 'learn-java'
  - 'paths/computer-science'
---

The **`.afeter`** [class](https://www.codecademy.com/resources/docs/java/classes) is an abstract class that represents dates and time. The class has methods for converting between a given moment in time and a number of calendar attributes such as `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR`, and so on.

## Syntax

```pseudo
public boolean after(Object time);
```

> **Note:** The `.getInstance()` function creates an object that represents the current date and time.

## Example

In the example below, a `Calendar` object is created using the `getInstance()` method. Then the `set()` method is used to set the year, month, date, hour, minute, and second. Finally, the `getTime()` method is used to get the date. Note that the month is zero-based, so January is 0, February is 1, and so on. Also, the `set()` overload could have been used that takes all the parameters at once.

```java
import java.util.Calendar;

public class CalendarExample {
    public static void main(String[] args) {
        // Create two instances of Calendar
        Calendar calendar1 = Calendar.getInstance();
        Calendar calendar2 = Calendar.getInstance();

        // Set different dates for each instance
        calendar1.set(2023, Calendar.AUGUST, 1); // August 1, 2023
        calendar2.set(2023, Calendar.SEPTEMBER, 1); // September 1, 2023

        // Check if calendar1 is after calendar2
        boolean isAfter = calendar1.after(calendar2);

        if (isAfter) {
            System.out.println("calendar1 is after calendar2");
        } else {
            System.out.println("calendar1 is not after calendar2");
        }
    }
}

```

The above code will output:

```shell
Sun Jan 08 00:00:00 GMT 2023
```

## Fields

There are many fields in the `Calendar` class. Here are some of the most important ones:

- `YEAR`: The field indicating the year.
- `MONTH`: The field indicating the month.
- `DAY_OF_MONTH`: The field indicating the day of the month.
- `DATE`: Synonym for `DAY_OF_MONTH`.
- `HOUR`: The field indicating the hour of the day.
- `MINUTE`: The field indicating the minute within the hour.
- `SECOND`: The field indicating the second within the minute.
- `MILLISECOND`: The field indicating the millisecond within the second.

## Methods

Methods of the `Calendar` class include:
