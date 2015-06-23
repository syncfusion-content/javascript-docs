---
layout: post
title: Remove-and-Replace-Function
description: remove and replace function
platform: js
control: Calculate
documentation: ug
---

# Remove and Replace Function

This section discusses the **Remove and Replace** function available for the **CalcEngine**.

## Remove Function

**Remove function** removes unused functions from the Function Library, reduces the memory usage, and speeds up parsing as well. When you use only a few Library functions, you may want to remove the unused ones. This is achieved by using the following method.

* To remove all functions, you can clear the hash table that holds them by using the **engine.getLibraryFunctions().clear** method.

* After clearing all functions, you can add few functions that are used often. To know how to add functions, refer to the **Add function** section.

* To remove a single function from the Function Library, use the **calcObj.removeFunction** method, passing a **function name** as the string that references this function from a formula.



{% highlight js %}

 // Remove formula name ADD from the Library.
 calcObj.removeFunction("ADD", "customAdd")


{% endhighlight %}

## Replace Function

To replace a function with another implementation, remove the original name and add the same name again with a different method name.

## Supported Formulas

**Ej.calculate.js** supports more than 200 formulas in many sections.

### Text formulas

#### Char

The **Char** function returns the character whose number code is defined in the parameter.

**Syntax:**

_Char(number)_

Where**,**

* number is the numeric value to retrieve the character.

#### Code

The **code** function converts the first character of a supplied text string into a numeric character set code.

**Syntax:**

_Code(name)_ 

Where,

* name is the text for which you want the code of the first character. 

#### Clean

The **Clean** function is used to remove the non-printable characters from the given text, represented by numbers 0 to 31 of the 7-bit ASCII code.

**Syntax:**

Where,

_=Clean(Text)_

* Text: Required. String or text from which to remove non-printable characters.

#### UNICHAR

The **Unichar** function retrieves the Unicode character for a given numeric value.

**Syntax:**

_Unichar(num)_ 

Where,

* num is the Unicode number that represents the character.

**Remarks:**

'#N/A'-occurs when data types are not valid.

'#VALUE!'-occurs when num falls outside the allowable range, when number is zero.

#### UNICODE

The **UNICODE** function calculates the number corresponding to the first character of the text.

**Syntax:**

_UNICODE(text)_ 

Where,

* text is the character for which you want the Unicode value.

**Remarks:**

'#VALUE!'-occurs when data type is not valid.

#### Upper

The **Upper** function converts all characters in a text string to uppercase.

**Syntax:**

_Upper(text )_

Where,

* text is the string you want to convert to uppercase.

#### Lower

The **Lower** function converts all characters in the specified text string to lowercase. Characters in the string that are not letters are not changed.

**Syntax:**

_Lower(text)_

Where,

* text is the string you want to convert to lowercase.

#### Left

The **Left** function returns the first character or characters in a text string, based on the number of bytes you specify.

**Syntax:**

_Left(text, bytes)_ 

Where,

* text is a string that contains the characters that you want to return.

* bytes specify the number of characters

#### Len

The **Len** function returns the number

**Syntax:**

_Len(name)_ 

Where,

* name is the text whose length you want to find. 

#### Mid

The **Mid** function returns a specific number of characters from a text string, starting at the position you specify.

**Syntax:**

_Mid(text, startNum, numBytes)_ 

Where,

* text is a string that contains the characters that you want to return.

* startNum is the position of the first character that you want to extract in text.

* numBytes specifies the number of characters you want in bytes.



#### Rept

The **Rept** function returns a supplied text string, repeated a specified number of times.

**Syntax:**

_Rept(string, number)_ 

Where,

* string is the text that you want to repeat.

* num is the number of times to repeat the text.



**Remarks:**

Blank text-occurs when number is zero.

#### Right

The **Right** function returns the last character or characters in a string, based on the number.

**Syntax:**

_Right(string, num)_ 

Where,

* string contains the characters you want to return. 

* num specifies the number of characters.



#### REPLACE

The **Replace** function replaces a certain part of text with a different part of text based on the number of characters given.

**Syntax:**

_Replace(oldText, startNum, numChars, newText)_ 

Where,

* oldText is the text that needs to be replaced.

* startNum is the position of the character in oldText.

* numChars is the number of characters needs to be replaced.

* newText is the text that replaces the character in old text.



#### Exact

The **Exact** function compares two values ignoring the styles and returns the Boolean value as **true** or **false**.

**Syntax:**

_Exact(value1, value2)_

Where,

* value1 is the first value you want to compare.

* value2 is the second value you want to compare.



#### Find

The **Find** function finds one text string (text1) within another text string (text2) and returns the number of the starting position of text1, based on the number of bytes each character uses, from the first character of text2. 

**Syntax:**

_Find(text1,text2, num)_ 

Where,

* text1 is the text that is to be found.

* text2 is the text that contains the found text.

* num specifies the character where to start the search.



**Remarks:**

'#VALUE!'-occurs when text1 does not appear in text2 and when num is not greater than zero.

#### T

The **T** function tests whether the given value is a text or not. When the given value is a text, then it returns the given text. Otherwise, the function returns as an empty text string.

**Syntax:**

=T( value )

Where,

* value is a required value to be checked. 

When the value is not a number or logical value, then the function returns as an empty string.

#### Trim

The **Trim** function returns a text value with the leading and trailing spaces removed. 

**Syntax:**

_Trim( text )_

Where,

* text is the text value for which you want to remove the leading and the trailing spaces.

#### Search

The **Search** function finds one text string (find_text) within another text string (within_text), and returns the number of the starting position of find_text.

**Syntax:**

_Search(findText,withinText, startNum )_ 

where,

* findText is the text that you want to find.

* withinText is the text in which you want to search findText.

* startNum is the character number in withinText, where you want to start the search.



**Remark:**

'#VALUE!'-occurs when find Text is not found.

#### Substitute

It **substitutes** new_text for old_text in a text string. Use **Substitute** when you want to replace specific text in a text string; use **Replace** when you want to replace any text that occurs in a specific location in a text string.

**Syntax:**

_Substitute(text, old_text, new_text, instance_num)_

 Where,	

* Text is the text or the reference to a cell containing text in which you want to substitute characters.

* Old_text is the text you want to replace.

* New_text is the text you want to replace old_text with.

* Instance_num specifies the occurrence of old_text you want to replace with the new_text. When you specify instance_num, only that instance of old_text is replaced. Otherwise, every occurrence of old_text in text is changed to new_text.



#### Value

The **Value** function computes the date or a string that contains the number, and converts it into number format.

**Syntax:**

_Value(range)_

Where,

* range is the string that contains the date or a number.

#### Concatenate

**Concatenate** joins several text strings into one text string.

**Syntax:**

_Concatenate (text1, text2,...)_

Where,

* text1, text2 ... are text items to be joined into a single text item. The text items can be text strings, numbers, or single-cell references.

#### NumberValue

The **NumberValue** function converts text to a number in a locale-independent way.

**Syntax:**

_NumberValue(text)_ 

Where,

* text is the text to be converted into a number.

**Remarks:**

'#VALUE!'-occurs when any of the argument is not valid.

#### Dollar

The **Dollar** function converts a number to text by using the currency format. The format used is $#,##0.00_);($#,##0.00).

**Syntax:**

_Dollar(number, decimal_places)_

Where,

* number is the number you want to convert to text.

* decimal_places is the number of digits in decimal places you want to display. The value is rounded accordingly.



#### Fixed

The **Fixed** function rounds off to a specified number of decimal places and returns the value in text format.

**Syntax:**

_Fixed(number, decimal_places, no_commas)_

Where,

* number is the number you want to round.

* decimal_places is the number of decimal places you want to display in the result.

* no_commas is a logical value. This displays commas when it is set to **false** and does not display commas when it is set to **true**.



### Engineering formulas

#### BIN2OCT

The **BIN2OCT** function converts a binary number into an octal number.

**Syntax:**

_BIN2OCT(num, places)_ 

where,

* num is the decimal integer you want to convert. 

* places is the number of characters to use.



#### BIN2HEX

The **BIN2HEX** function converts a binary number into a hexadecimal.

**Syntax:**

_BIN2HEX(num places)_ 

where,

* num is the decimal integer you want to convert. 

* places is the number of characters to use.



**Remarks:**

'#NUM!'-occurs when number is not a valid binary number, when places is negative.

'#VALUE!'-occurs when places is non-numeric.

#### BIN2DEC

The **BIN2DEC** function converts a binary number into a decimal number.

**Syntax:**

_BIN2DEC(num)_ 

Where,

* num is the binary number that you want to convert.

**Remark:**

'#NUM!'-occurs when number is not a valid binary number or when number contains more than 10 characters.

#### DEC2BIN

The **DEC2BIN** function converts a decimal number into a binary number.

**Syntax:**

_DEC2BIN(num,places)_ 

Where,

* num is the decimal integer you want to convert. 

* places is the number of characters to use.



**Remarks:**

'#NUM!'-occurs when number &lt; -512 or if number &gt; 511 and when places is zero or negative.

'#VALUE!'-occurs when number  or places is non-numeric and when DEC2BIN requires more than the number of characters specified in places.

#### DEC2OCT

The **DEC2OCT** function converts a decimal number into an octal number.

**Syntax:**

_DEC2OCT(num, places)_ 

where,

* num is the decimal integer you want to convert. 

* places is the number of characters to use.



**Remarks:**

'#NUM!'-occurs when number &lt; -512 or if number &gt; 511 and when places is zero or negative.

'#VALUE!'-occurs when the number or places is non-numeric and when DEC2OCT requires more than the number of characters specified in places.

#### HEX2BIN

The **HEX2BIN** function converts a hexadecimal number into a binary number. 

**Syntax:**

_HEX2BIN(num, places)_ 

where,

* num is the decimal integer you want to convert. 

* places is the number of characters to use.



**Remarks:**

'#NUM!'-occurs when number is not a valid binary number and when places is negative.

'#VALUE!'-occurs when places is non-numeric.

#### HEX2OCT

The **HEX2OCT** function converts a hexadecimal number into an octal number. 

**Syntax:**

_HEX2OCT(num, places)_

where:

* num is the hexadecimal integer you want to convert. 

* places is the number of characters to use.



**Remarks:**

'#NUM!'-occurs when number is not a valid hexadecimal number and when places is negative.

'#VALUE!'-occurs when places is non-numeric.

### Date and Time formulas

#### Date

Returns the sequential serial number that represents a particular date.

**Syntax:**

_Date(year, month, day)_

Where,

* year can be one to four digits. Year is interpreted based on 1900.

* When a year is between 0 (zero) and 1899 (inclusive), the value is added to 1900 to calculate the year. For example, Date (102, 11, 12) returns as November 12, 2002 (1900+102).

* When a year is between 1900 and 9999 (inclusive), the value is used as it is, for example, Date(2002,11,12) returns as November 12, 2002.

* month is a number representing the month of the year.

* day is a number representing the day of the month.



**Remark:**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, January 1, 1900 is serial number 1 and November 12, 2002 is serial number 37572 because it is 37572 days after January 1, 1900.

#### DateValue

Returns the serial number of the date represented by the date_text.

**Syntax:**

_DateValue(date_text)_

Where,

* date_text is the text that represents a date as a formatted string. For example, 11/12/2002 or 12-Nov-2002 are text strings within quotation marks that represent dates. When the year portion of the date_text is omitted, DateValue uses the current year from your computer's built-in clock. The time information in the date_text is ignored.

**Remarks:**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, January 1, 1900 is serial number 1, and November 12, 2002 is serial number 37572 because it is 37572 days after January 1, 1900.

Most functions automatically convert date values to serial numbers.

#### Day

Returns the day of a date represented by a serial number. The **Day** is given as an integer ranging from 1 to 31.

**Syntax:**

_Day(serial_number)_

Where,

* serial_number is the date of the day you are trying to find. Dates should be entered by using the **Date** function or as results of other formulas or functions. For example, use Date(2002,4,23) for the 23rd day of April, 2002.

#### Days360

Returns the number of days between two dates based on a 360-day year (twelve 30-day months) that is used in some accounting calculations.

**Syntax:**

_Days360(start_date, end_date, method)_

Where,

* start_date and end_date are the two dates between which you want to know the number of days. When start_date occurs after end_date, **Days360** returns a negative number. Dates should be entered by using the **Date** function or as results of other formulas or functions.

* method is a logical value that specifies whether to use the U.S. or European method in the calculation. When method is:

* False or omitted-The calculation uses the U.S. (NASD) method. When the starting date is the 31st of a month, it becomes equal to the 30th of the same month. When the ending date is the 31st of a month and the starting date is earlier than the 30th of a month, the ending date becomes equal to the 1st of the next month, otherwise the ending date becomes equal to the 30th of the same month.

* True-The calculation uses the European method. Starting dates and ending dates that occur on the 31st of a month become equal to the 30th of the same month.



#### EDate

The **EDate** function returns a date that is a specified number of months before or after a supplied start date. 

**Syntax:**

_EDate( startDate, Months )_ 

Where,

* startDate is the initial date from where to count the number of months. 

* Months is the number of months to add to (or subtract from) the startDate.



**Remarks:**

'#VALUE!'-occurs when the supplied startDate is not a valid date.

'#VALUE!'-occurs when the supplied Months argument is non-numeric.

#### EOMonth

The **EOMONTH** function returns the last day of the month that is a specified number of months before or after an initially supplied start date.  

**Syntax:**

_EOMonth(startDate, Months)_ 

Where,

* startDate is the initial date.

* Months is the number of months to add to (or subtract from) the startDate before returning the last day of the resulting month. 



**Remarks:**

'#VALUE!'-occurs when any of the supplied argument is not a numeric value. 

'#NUM!'-occurs when the supplied startDate is not a valid date.

'#NUM!'-occurs when the supplied startDate plus the value of the months argument is not a valid date.

#### Hour

Returns the hour of a time value. The hour is given as an integer, ranging from 0 (12:00 A.M.) to 23 (11:00 P.M.).

**Syntax:**

_Hour(serial_number)_

Where,

* serial_number is the time that contains the hour you want to find. Times may be entered as text strings within quotation marks (for example, "6:00 PM"), as decimal numbers (for example, 0.75, that represents 6:00 PM), or as results of other formulas or functions (for example, TimeValue("6:00 PM")).

#### Minute

Returns the minutes of a time value. The **Minute** is given as an integer ranging from 0 to 59.

**Syntax:**

_Minute(serial_number)_

Where,

* serial_number is the time that contains the minute you want to find. Times may be entered as text strings within quotation marks (for example, "6:00 PM"), as decimal numbers (for example, 0.75, that represents 6:00 PM), or as results of other formulas or functions (for example, TIMEVALUE ("6:00 PM")). 

**Remarks:**

Time values are a portion of a date value represented by a decimal number (for example, 12:00 PM is represented as 0.5).

#### Month

Returns the month of a date represented by a serial number. The **Month** is given as an integer ranging from 1 (January) to 12 (December).

**Syntax:**

_Month(serial_number)_

Where,

* serial_number is the date of the month you are trying to find. Dates should be entered by using the **Date** function or as results of other formulas or functions. For example, use Date(2002,11,12) for the 12th day of November, 2002.

**Remarks**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, January 1, 1900 is serial number 1 and January 1, 2008 is serial number 39448 because it is 39,448 days after January 1, 1900.

#### Now

Returns the serial number of the current date and time. 

**Syntax:**

_Now( )_

**Remarks:**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, January 1, 1900 is serial number 1 and January 1, 2008 is serial number 39448 because it is 39,448 days after January 1, 1900

Numbers to the right of the decimal point in the serial number represent the time; and numbers to the left represent the date. For example, the serial number .5 represents the time 12:00 noon.

#### Second

Returns the seconds of a time value. The **Second** is given as an integer in the range 0 (zero) to 59.

**Syntax:**

_Second(serial_number)_

Where,

* serial_number is the time that contains the seconds you want to find.

**Remarks**

Time values are a portion of a date value and are represented by a decimal number (for example, 12:00 PM is represented as 0.5 because it is half of a day).

#### Networkdays.intl

**Networkdays.intl** calculates the number of whole work days between two supplied dates.

**Syntax:**

_Networkdays.intl(startDate, endDate)_ 

Where,

* startDate is the start of the period where days are counted.

* endDate is the end of the period where days are counted.



**Remarks:**

'#VALUE!'-occurs when the supplied startDate and endDate are not valid dates. 

#### Time

Returns the decimal number for a particular time. The decimal number returned by **Time** is a value ranging from 0 (zero) to 0.99999999, representing the times from 0:00:00 (12:00:00 A.M.) to 23:59:59 (11:59:59 P.M.).

 **Syntax:**

_Time(hour, minute, second)_

 Where,

* hour is a number from 0 (zero) to 23 representing the hour.

* minute is a number from 0 to 59 representing the minute.

* second is a number from 0 to 59 representing the second.



#### TimeValue

Returns the decimal number of the time represented by a text string. The decimal number is a value ranging from 0 (zero) to 0.99999999, representing the times from 0:00:00 (12:00:00 A.M.) to 23:59:59 (11:59:59 P.M.).

**Syntax:**

_TimeValue(time_text)_

Where**,**

* time_text is a text string that represents a time as a formatted string. For example, "6:45 PM" and "18:45" text strings within quotation marks that represent time.

**Remark:**

Date information in time_text is ignored.

#### Today

Returns the serial number of the current date. The serial number is the number of days since Jan 1, 1900.

**Syntax:**

_Today( )_

 **Remark:**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, January 1, 1900 is serial number 1 and January 1, 2008 is serial number 39448 because it is 39,448 days after January 1, 1900.

#### Weekday

Returns the day of the week corresponding to a date. The day is given as an integer, ranging from 1 (Sunday) to 7 (Saturday), by default.

**Syntax:**

_Weekday(serial_number,return_type)_

 Where,

* serial_number is a sequential number that represents the date of the day you are trying to find. Dates should be entered by using the **Date** function or as results of other formulas or functions. For example, use Date (2008, 5, 23) for the 23rd day of May 2008.

* return_type is a number that determines the type of return value.

<table>
<tr>
<td>
<b>Return type  </b></td><td>
<b>Number returned</b></td></tr>
<tr>
<td>
1 or omitted       </td><td>
Numbers 1 (Sunday) through 7 (Saturday).</td></tr>
<tr>
<td>
2</td><td>
Numbers 1 (Monday) through 7 (Sunday).</td></tr>
<tr>
<td>
3</td><td>
Numbers 0 (Monday) through 6 (Sunday).</td></tr>
</table>

**Remark:**

Dates are stored as sequential serial numbers so that they can be used in calculations. By default, 

January 1, 1900 is serial number 1 and January 1, 2008 is serial number 39448 because it is 39,448 days 

after January 1, 1900.

#### Weeknum

For a supplied a date, the **Weeknum** function returns an integer representing the week number (from 1 to 53) of the year. 

**Syntax:**

_Weeknum( serialNum, [returnType] )_ 

Where,

* serialNum is the date that you want to return the week number for. 

* [returnType] is an optional argument that specifies which numbering system should be used and which weekday should be treated as the start of the week.



**Remarks:**

'#VALUE!'-occurs when the supplied serialNum cannot be recognized as a numeric value or a date. 

'#NUM!'-occurs when the supplied [returnType] argument is not one of the above listed permitted values. 

'#NUM!'-occurs when the supplied serialNum argument is numeric, but is out of range for the current date base. 

#### Workday.intl

The **Workday.intl** function returns a date that is a supplied number of working days (excluding weekends and holidays) ahead of a given start date.

**Syntax:**

_Workday.intl (startDate, days, [weekend], [holidays])_ 

Where,

* startDate is the initial date from which to count the number of workdays. 

* days are number of workdays to add onto startDate. 

* [weekend] is an optional argument that specifies the weekdays to be counted as weekends. 

* [holidays] is an optional argument that specifies an array of dates that are not to be counted as working days. 



**Remarks:**

'#NUM!'-occurs when the supplied startDate plus the supplied days argument results in an invalid date.

'#NUM!'-occurs when the supplied [weekend] argument is invalid (see above explanation of this argument).

'#VALUE!'-occurs when the supplied startDate or any of the value in the supplied [holidays] array is not valid dates.

'#VALUE!'-occurs when the supplied days argument is non-numeric.

#### Workday

The **Workday** function returns a date that is a supplied number of working days (excluding weekends and holidays) ahead of a given start date. 

**Syntax:**

_Workday(startDate, Days, [holidays])_ 

Where,

* startDate is the initial date from which to count the number of workdays. 

* Days are number of workdays to add onto startDate. 

* [holidays] is an optional argument, which specifies an array of dates that are not to be counted as working days. 



**Remarks:**

'#NUM!'-occurs when the supplied startDate plus the supplied days argument results in an invalid date. 

'#VALUE!'-occurs when the supplied startDate or any of the value in the supplied [holidays] array is not valid dates, when the supplied days argument is non-numeric.

#### ISOWeekNum

For a given date, the **ISOWeekNum** function returns the ISO week number of that year.

**Syntax:**

_ISOWeekNum( DateTime)_ 

Where,

* DateTime is used for date and time calculation.

**Remarks:**

'#NUM!'-occurs when the date argument is not a valid number.

'#VALUE!'-occurs when the date argument is not a valid date type.

#### Days

The **Days** function retrieves the number of days between two dates.

**Syntax:**

_Days(endDate, startDate)_

Where,

* endDate and startDate are the two dates between which you want to know the number of days.

### Lookup and Reference formulas

#### Address

**Address** function returns the address of a cell in a worksheet when row and column numbers are given.

**Syntax:**

_Address(row_num, column_num, [abs_num], [a1], [sheet_text])_

* row_num: A numeric value that specifies the row number.

* column_num: A numeric value that specifies the column number

* abs_num: This value is optional. A numeric value that specifies the type of reference to return.

* A1: A logical value that specifies the A1 or R1C1 reference style.



#### Areas

The **Areas** function returns the number of areas that make up the reference. 

**Syntax:**

_Areas(reference)_

Where,

* reference is an input argument. 

#### Choose

The **Choose** function returns the value from a range of values on a specific index.

**Syntax:**

_Choose(index, valuearray)_

Where,

* index specifies the index from where you want to retrieve the value.

* valuearray is the array of value from where you want to retrieve the value.



#### Column

The **Column** function returns the column index of the provided column in range.

**Syntax:**

_Column(range)_

 Where,

* range is to provide the column in range.

#### Columns

The **Columns** function returns the number of columns that are contained within the range. 

**Syntax:**

_Columns(array)_ 

Where,

* array argument is the range of the number of columns. 

#### HLookup

Searches for a value in the top row of the array of values and then returns a value in the same column from a row you specify in the array. Use **HLookup** when your comparison values are located in a row across the top of a table of data and you want to look down a specified number of rows. Use **VLookup** when your comparison values are located in a column to the left of the data you want to find.

**Syntax:**

_HLookup(lookup_value, table_array, row_index_num, range_lookup)_

Where:

* **lookup_value** is the value to be found in the first row of the table. **Lookup_value** can be a value, reference, or text string.

* **table_array** is a table of information in which data is looked up. Use a reference to a range or a range name.

* **row_index_num** is the row number in **table_array** from which the matching value returns. A **row_index_num** of 1 returns the first row value in **table_array**, a **row_index_num** of 2 returns the second row value in **table_array**, and so on.

* **range_lookup** is a logical value that specifies whether you want **HLookup** to find an exact match or an approximate match. When **True** or omitted, an approximate match is returned. In other words, when an exact match is not found, the next largest value that is lesser than the **lookup_value** is returned. (This requires your lookup values to be sorted.) when **False**, **HLookup** finds an exact match



#### Hyperlink

The **Hyperlink** function creates a hyperlink to a document in a supplied location.

**Syntax:**

_Hyperlink( linkLocation, friendlyName )_

Where,

* linkLocation is the address of the file to link. 

* friendlyName is the text to display in the cell. 



#### Row

The **Row** function returns the first row number within a supplied reference. When reference is not supplied, the function returns the number of the current row in the currently active spreadsheet.

**Syntax:**

_Row([reference])_ 

Where,

* reference is an optional argument of the row number that you want to return. When [reference] is omitted, the function returns the row number of the current cell (that is, the cell that the function is entered into). 

#### Index

The **Ind**_**e**_**x** function returns the exact value from the provided row index and column index from a specific range.

**Syntax:**

_Index(range,row,col)_

Where,

* range is a string to mention the specific range.

* row is the integer that indicates the specific row index.

* col is the integer that indicates the specific column index.



#### Indirect

The **Indirect** function returns the reference as a string instead of providing the content or range within it.

**Syntax:**

_Indirect(content)_

Where,

* content is the string that provides the textual representation of the cell.

#### Lookup

**Lookup** function returns a value either from one-row or one-column range, or from an array. **Lookup** function has two syntax forms: vector and array.

**Vector Form:** The vector application page of **Lookup** looks in a one-row or one-column range for a value and then returns a value from the same position in a second one-row or one-column range.

**Syntax:**

_=LOOKUP(lookup_value, lookup_vector, result_vector)_

**Array form:** The array application page of **Lookup** looks in the first row or column of an array for the specified value and then returns a value from the same position in the last row or column of the array.

**Syntax:**

_=LOOKUP(lookup_value, array)_

**Remarks:**

When the **Lookup** function cannot find the **lookup_value**, the function matches the largest value in **lookup_vector** that is less than or equal to **lookup_value**.

When **lookup_value** is smaller than the smallest value in **lookup_vector**, **Lookup** returns the #N/A error value.

#### ROWS

The **Rows** function takes a range and returns the number of rows that are contained within the range. 

**Syntax:**

_Rows( array )_ 

Where,

* array argument is the range in which you want to count the number of rows. 

#### Sheet

The **Sheet** function returns the sheet number of the reference sheet.

**Syntax:**

_Sheet(value)_

where,

* value is an optional argument with the name of a sheet for which you want the sheet number.

**Remarks:**

'#REF!'-occurs when value argument is not a valid value.

'#NA'-occurs when value argument is a sheet name that is not valid.

#### Sheets

**Sheets** function returns the number of sheets in a reference.

**Syntax:**

_Sheets(reference)_

Where,

* reference is an optional argument with the name of a sheet for which you want to know the number of sheets.

**Remarks:**

'#REF!'-occurs when reference is not a valid value.

#### Transpose

The **Transpose** function copies a horizontal range of cells into a vertical range and vice versa.

**Syntax:**

_Transpose(array)_

Where,

* array argument is a range of spreadsheet cells. 

#### FormulaText

**FormulaText** function returns the formula as a string.

**Syntax:**

_FormulaText (reference)_

Where,

* reference is the reference to a cell or range of cells.

**Remarks:**

'#N/A'-occurs when the reference argument is to another workbook that is not opened.

'#N/A'-occurs when the reference argument is to a range containing more than one cell.

'#N/A'-occurs when the cell used as the reference argument does not contain a formula.

'#N/A'-occurs when the formula in the cell is longer than 8192 characters.

'#N/A'-occurs when the formula cannot be displayed in the worksheet.

'#N/A'-occurs when an external workbook that contains the formula is not opened.

### Statistical formulas

#### Percentile.Exc

The **Percentile.Exc** function returns the k-th percentile of values in a range, where k is in the range of 0 to 1 exclusively.

**Syntax:**

_Percentile.Exc(array, k)_

Where,

* array is the range of data that defines relative standing.

* k is the percentile value in the range of 0 to 1.



**Remarks:**

'#NUM!'-occurs when k is equal to or lesser than zero, when k is equal to or greater than 1, and when the array is empty.

'#VALUE!'-occurs when k is non-numeric.

#### Percentile.Inc

The **Percentile.Inc** function returns the k-th percentile of values in a range, where k is in the range 0 to 1.

**Syntax:**

_Percentile.Inc (array,k)_

Where,

* array is the range of data that defines relative standing.

* k is the percentile value in the range 0 to 1.



**Remarks:**

'#NUM!'-occurs when k is equal to or lesser than zero, when k is equal to or greater than 1, and when the array is empty.

'#VALUE!'-occurs when k is a non-numeric.

#### Percentrank.Exc

The **Percentrank.Exc** function returns the rank of a value in a data set as a percentage (0 to 1, exclusively) of the data set.

**Syntax:**

_Percentrank.Exc(array, x )_

Where,

* array is the range of data that defines relative standing.

* x is value for which you want to know the rank.



**Remarks:**

'#NUM!'-occurs when this argument is empty.

'#NUM!'-occurs when the argument is lesser than one.

#### STDEV.P

The **STDEV.P** function calculates the standard deviation of a supplied set of values.

**Syntax:**

_STDEV.P(number1,[number2],...])_

Where,

* number1 is the first number argument corresponding to a population.

* number2 ... are the arguments 2 to 254 corresponding to a population.



**Remarks:**

Arguments can either be numbers or names, arrays, or references that contain numbers.

The standard deviation is calculated by using the **n** method.

Arguments that are error values or text that cannot be translated into numbers cause errors.

#### STDEV.S

The **STDEV.S** function calculates the sample standard deviation of a supplied set of values.

**Syntax:**

_STDEV.S(number1,[number2],...])_

where,

* number1 is the first number argument corresponding to a population.

* Number2, ... are the arguments 2 to 254 corresponding to a population.



**Remarks:**

Arguments can either be numbers or names, arrays, or references that contain numbers.

The standard deviation is calculated by using the **n** method.

Arguments that are error values or text that cannot be translated into numbers cause errors.

#### PermutationA

The **PermutationA** function returns the number of permutations for a given number of objects (with repetitions) that can be selected from the total number of objects.

**Syntax:**

_PermutationA(number, number-chosen)_

Where,

* number is an integer that describes the total number of objects.

* number-chosen is an integer that describes the number of objects in each permutation.



 **Remarks:**

'#VALUE!'-occurs when numeric arguments use data types that are non-numeric.

'#NUM!'-occurs when numeric arguments have values that are not valid.

#### Norm.S.Dist

The **Norm.S.Dist** function returns the standard normal distribution.

**Syntax:**

_Norm.S.Dist(val, cumulative)_

Where,

* val is the value for which you want the distribution.

* cumulative is a logical value that determines the form of the function.

#### Norm.S.Inv

The **Norm.S.Inv** function returns the inverse of the standard normal cumulative distribution.

**Syntax:**

_Norm.S.Inv(probability)_

Where,

* probability is a probability that corresponds to the normal distribution.

#### Weibull.Dist

The Weibull.Dist function returns the Weibull Distribution.

**Syntax:**

_Weibull.Dist(x,alpha,beta,cumulative)_

Where,

* x is the value that evaluates the function.

* alpha is a parameter of the distribution.

* beta is a parameter of the distribution.

* cumulative determines the form of the function.



 **Remarks:**

'#NUM!'-occurs when x is lesser than zero and when alpha or beta is equal to or lesser than zero.

'#VALUE!'-occurs when beta is non-numeric.

#### Expon.Dist

The **Expon.Dist** function calculates the value of the probability density function or the cumulative distribution function for the **Exponential Distribution**.

**Syntax:**

_Expon.Dist(x,y,cumulative)_

Where,

* x is the value that evaluates the function.

* y is the parameter value.

* cumulative is a logical value for given function.



**Remarks:**

'#NUM!'-occurs when x is lesser than zero and y is equal to or lesser than zero. 

'#VALUE!'-occurs when x or y is non-numeric.

#### Gamma.Inv

The **Gamma.Inv** function returns the inverse of the Gamma Distribution.

**Syntax:**

_Gamma.Inv(x,y,z,cumulative)_

Where,

* x is the value that evaluates the function.

* y is a distribution parameter.

* z is a distribution parameter.

* cumulative is a logical value that indicates which form of the exponential function to provide.



**Remarks:**

'#NUM!'-occurs when x is lesser than zero, when z is equal to or lesser than zero and occurs when alpha is equal to or lesser than zero. 

'#VALUE!'-occurs when x or y or z is non-numeric.

#### Gammaln.Precise

The **Gammaln.Precise** function returns the natural logarithm of the Gamma Distribution.

**Syntax:**

_Gammaln.Precise(x)_ 

Where,

* x is the positive numeric value that evaluates the function. 


**Remarks:**

'#NUM!'-occurs when x is lesser than zero.

'#VALUE!'-occurs when x is non-numeric.

#### F.INV.RT

The **F.INV.RT** function calculates the inverse of the Cumulative F Distribution for a supplied probability.

**Syntax:**

_F.INV.RT(probability,degFreedom1,degFreedom2)_

Where,

* probability is a probability that corresponds to the normal distribution.

* degFreedom1 is the numerator degrees of freedom.

* degFreedom2 is the denominator degrees of freedom.



**Remarks:**

'#NUM!' - occurs when probability is equal to or lesser than zero and when probability is equal to or greater than one.

'#VALUE!' - occurs when probability or degFreedom1 or degFreedom2 is non-numeric.

#### Lognorm.Dist

The **Lognorm.Dist** function calculates the Log-Normal Probability Density Function or the Cumulative Log-Normal Distribution Function for a supplied value of x.

**Syntax:**

_Lognorm.Dist(x,mean,stdev,cumulative)_

where,

* x is the value that evaluates the function.

* mean is the mean value of ln(x).

* stdev is the standard deviation of ln(x).

* cumulative is a logical value that determines the form of the function. 



**Remarks:**

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when x ≤ 0 or if stdev ≤ 0.

#### Lognorm.Inv

The **Lognorm.Inv** function calculates the inverse of the Cumulative Log-Normal Distribution Function of x for a supplied probability.

**Syntax:**

_Lognorm.Inv(probability, mean, stdev)_

where,

* probability is a probability that corresponds to the lognormal distribution.

* mean is the arithmetic mean of In(x).

* stdev is the standard deviation of ln(x).



**Remarks:**

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when probability &lt;= 0 or probability &gt;= 1 and if Stdev<=0.

#### Confidence.Norm

The **Confidence.Norm** function uses [Normal Distribution](http://en.wikipedia.org/wiki/Normal_distribution) to calculate a confidence value that can be used to construct the confidence interval for a population mean, for a supplied probability, and sample size.

**Syntax:**

_Confidence.Norm(alpha,stdev,size)_

Where,

* alpha is the significance level.

* stdev is the population standard deviation for the data range.

* size is the sample size. 



**Remarks:**

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when alpha and stdev is lesser than or equal to zero or when alpha is greater than or equal to zero.

'#DIV/0!'-occurs when the size is equal to one.

#### CHISQ.DIST.RT

The **Chisq.Dist.Rt** function calculates the right-tailed probability of the [chi-square distribution](http://en.wikipedia.org/wiki/Chi-square_distribution).

**Syntax:**

_Chisq.Dist.Rt(x,degFreedom)_ 

where,

* x is the value that evaluates the function.

* degFreedom is the number of degrees of freedom.



**Remarks:**

'#VALUE!'-occurs when either argument is non-numeric.

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when f degFreedom &lt; 1 or degFreedom &gt; 10^10.

#### F.Dist 

The **F.Dist** function calculates the Probability Density Function or the Cumulative Distribution Function for the **F Distribution**.

**Syntax:**

_F.Dist(x,degFreedom1,degFreedom2,cumulative)_ 

where,

* x is the value that evaluates the function.

* degFreedom1 is the numerator degree of freedom.

* degFreedom1 is the denominator degree of freedom. 

* cumulative is a logical value that determines the form of the function.



**Remarks:**

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when x is negative, when degFreedom1< 1 and when degFreedom1< 1

#### F.Dist.Rt

The **F.Dist.Rt** function calculates the F Probability Distribution that measures the degree of diversity between two data sets.

**Syntax:**

_F.Dist.Rt(x, degFreedom1, degFreedom2)_ 

where,

* x is the value that evaluates the function.

* degFreedom1 is the numerator degree of freedom.

* DegFreedom2 is the denominator degree of freedom. 



**Remarks:**

'#VALUE!'-occurs when any argument is non-numeric.

'#NUM!'-occurs when x is negative, when degFreedom1< 1 and  when degFreedom2< 1.

####  Chisq.Inv

The **Chisq.Inv** function returns the inverse of the left-tailed probability of the chi-squared distribution.

**Syntax:**

_Chisq.Inv(probability,degFreedom)_

where,

* probability is a probability of chi-squared distribution.

* deg_freedom is the number of degrees of freedom.



**Remarks:**

'#NUM!'-occurs when probability is lesser than zero, when probability is greater than 1, and degFreedom is lesser than 1.

'#VALUE!'-occurs when probability or degFreedom is non-numeric.

#### CHISQ.INV.RT

The **Chisq.Inv.Rt** function calculates the inverse of the right-tailed probability of the [chi-square distribution](http://en.wikipedia.org/wiki/Chi-square_distribution).

**Syntax:**

_Chisq.Inv.Rt(probability, degFreedom)_

where,

* probability is a probability of chi-squared distribution.

* degFreedom is the number of degrees of freedom.



**Remarks:**

'#NUM!'-occurs when probability is lesser than zero, when probability is greater than 1, and when degFreedom is lesser than 1.

'#VALUE!'-occurs when probability or degFreedom is non-numeric. 

#### Binom.Dist

The **Binom.Dist** function returns the Binomial Distribution probability for a given number of successes from a specified number of trials. 

**Syntax:**

_Binom.Dist (trial number,sp,value, cumulative)_

Where,

* trial number is the number of Bernoulli trials.

* sp is the probability of a success on each trial.

* value is the criterion value. 

* cumulative is a logical value that determines the form of the function.



**Remarks:**

'#NUM!'-occurs when trial number is lesser than zero, when sp and value are lesser than zero or greater than one.

'#VALUE!'-occurs when trials, sp, and value are non-numeric.

#### Negbinom.Dist

The **Negbinom.Dist** function calculates the probability mass function or the cumulative distribution function for the **Negative Binomial Distribution**.

**Syntax:**

_Negbinom.Dist(F_number,S_number,S_probability,cumulative)_

where,

* (F_number is the number of failures.

* S_number is the threshold number of successes.

* S_probability is the probability of a success.

* cumulative is a logical value that determines the form of the function.



#### Poisson.Dist

The **Poisson.Dist** function calculates the Poisson Probability Mass Function or the Cumulative Poisson Probability Function for a supplied set of parameters.

**Syntax:**

_Poisson.Dist(x,mean,cumulative)_

where,

* x is the number of events.

* mean is the expected numeric value.

* cumulative is a logical value that determines the form of the probability distribution returned.



**Remarks:**

'#VALUE!'-occurs when x is not an integer.

'#NUM!'-occurs when x or mean is non-numeric and s when x < 0.

#### ZTest

**ZTest** function returns the one-tailed probability value of a z-test.

**Syntax:**

_ZTest(a1,T_value,sigma)_ 

where,

* array is an array or range of data.

* T_value is the value to test..

* sigma  is the population (known) standard deviation.



#### Rank.Eq

The **Rank.Eq** function returns the statistical rank of a given value within a supplied array of values.

**Syntax:**

_Rank.Eq(number, ref)_

where,

* number is the value for which you want to find the rank.

* ref is an array of values containing the supplied number.



### Math and Trigonometry formulas

#### Sec

The **Sec** function returns the secant of an angle.

**Syntax:**

_Sec(number)_ 

Where,

* number-angle radians to get the secant value.

**Remarks:**

'#NUM!'-occurs when the number is outside its constraints.

'#VALUE!'-occurs when number is a non-numeric value.

#### Abs

Returns the **Absolute Value** of a number. The **Absolute Value** of a non-negative number is the number itself. The Absolute Value of a negative number is 1 times the number.

**Syntax:**

_Abs(number)_

Where,

* number is the real number for which you want the absolute value.

#### ISeven

**ISeven** function returns **true** when given number is an even number and returns **false** when the given number is odd.

**Syntax:**

_=ISeven (value)_

* The given value must be a numeric value. When it is non-integer value, the value is rounded down.

#### Subtotal

**Subtotal** function returns a subtotal in a list. Once the subtotal list is created, you can modify it by editing the **Subtotal** function.

**Syntax:**

_=Subtotal (function_Number, ref1, (ref2)...)_

Where**,**

* A function_Number is required. This specifies which function to use for calculating subtotals within a list. Here is the list of functions supported by Syncfusion:

_Function numbers_

<table>
<tr>
<td>
<b>Function Numbers</b></td><td>
<b>Function Names</b></td></tr>
<tr>
<td>
1</td><td>
AVERAGE</td></tr>
<tr>
<td>
2</td><td>
COUNT</td></tr>
<tr>
<td>
3</td><td>
COUNTA</td></tr>
<tr>
<td>
4</td><td>
MAX</td></tr>
<tr>
<td>
5</td><td>
MIN</td></tr>
<tr>
<td>
6</td><td>
PRODUCT</td></tr>
<tr>
<td>
7</td><td>
STDEV</td></tr>
<tr>
<td>
8</td><td>
STDEVP</td></tr>
<tr>
<td>
9</td><td>
SUM</td></tr>
<tr>
<td>
10</td><td>
VAR</td></tr>
</table>


* ref1-The first named range that is used for the subtotal. This value is required.

* ref2-This value is optional.



#### MRound

**MRound** function rounds a given number up or down to the nearest multiple of a given number.

**Syntax:**

_= MRound (number, multiple)_

* number-The value to be rounded and the value is required.

* multiple-This value is required.



The number must be greater than or equal to half the value of multiple.

**Remarks:**

'#NUM!'-Occurs when the number and multiple have different signs.

'#VALUE!'-Occurs when any of the given argument is non-numeric.

#### RandBetween

**RandBetween** function returns a random number that is between the given ranges. This function returns a new random number each time in recalculation.

**Syntax:**

_= RandBetween  (start_num, end_num)_

* start_num-This is the smallest required integer value.

* end_num-This is the largest required integer value.



**Remarks:**

'#NUM!'-Occurs when the end_num value is larger than start_num value.

'#VALUE!'-Occurs when any of the given argument is non-numeric. 

#### SQRTPI

**SQRTPI** function returns the square root of a given number multiplied by π. Here π is the constant math value.

**Syntax:**

_=SQRTPI (number)_

Where**,**

* number-This value is required.

**Remarks:**

'#NUM!'-When the number is lesser than zero (0).

'#VALUE!'-Occurs when any of the given argument is non-numeric. 

#### Quotient

**Quotient** function returns the integer portion of a division between two given numbers. The returned value is an integer value.

**Syntax:**

_=Quotient (numerator, denominator)_

* numerator-This value is required.

* denominator-This value is required.



**Remarks:**

'#VALUE!'-Occurs when any of the given argument is non-numeric. 

#### FactDouble

**FactDouble** function returns the double factorial of a given value. The given value is an integer value.

**Syntax:**

_= Factdouble (number)_

Where**,**

* number-This value is required.

**Remarks:**

'#NUM!'-when the number is lesser than zero (0).

'#VALUE!'-Occurs when any of the given argument is non-numeric

#### GCD

**GCD** function returns the greatest common divisor of two or more given values. The values must be of numeric value.

**Syntax:**

_= GCD (number1, number2 ...)_

* number1 – This value is required.

When any value is not an integer, then it is rounded down. 

**Remarks:**

'#NUM!' -When the number is lesser than zero (0). 

'#VALUE!' -Occurs when any of the given argument is non-numeric.

#### LCM

**LCM** function returns the least common multiple of two or more given values. The values must be numeric values.

**Syntax:**

_= LCM (number1, number2 ...)_

Where,

* number1-This value is required.

When any value is not an integer, then it is rounded down. 

**Remarks:**

'#NUM!' -When the number is lesser than zero (0).

'#VALUE!'-Occurs when any of the given argument is non-numeric. 

#### Roman

**Roman** function converts an Arabic number to a Roman numeral. This function returns a text string depicting Roman numeral application page of the given number.

**Syntax:**

_=ROMAN( number, (form) )_

* number-This value is required.

* form-Optional. This value specifies the style of the Roman numeral.

When the number is not an integer, then it is rounded down.

_Roman functions_

<table>
<tr>
<td>
<b>Form</b></td><td>
<b>Type</b></td></tr>
<tr>
<td>
0 or omitted</td><td>
Classic.</td></tr>
<tr>
<td>
1</td><td>
More concise. See example as follows.</td></tr>
<tr>
<td>
2</td><td>
More concise. See example as follows.</td></tr>
<tr>
<td>
3</td><td>
More concise. See example as follows.</td></tr>
<tr>
<td>
4</td><td>
Simplified.</td></tr>
</table>

 **Remark:**

'#VALUE!' -Occurs when any of the given value is non-numeric or for the values lesser than 0 and greater than 3999. 

#### T

The **T** function tests whether the given value is a text or not. When the given value is a text, then it returns the given text. Otherwise, the function returns an empty text string.

**Syntax**

_=T( value )_

* value - This is a required value to be checked. 

When the value is not a number or logical value, then the function returns an empty string. 

#### Clean

**Clean** function is used to remove non-printable characters from the given text represented by numbers 0 to 31 of the 7-bit ASCII code.

**Syntax:**

_=Clean(Text)_

* Text-Required. String or text from which to remove non-printable characters. 

#### Averageif

**Averageif** function finds the average of values in a given array that satisfies a given criteria and returns the average value of the corresponding values in a second given array.

**Syntax:**

_=Averageif(range, criteria, average_range)_

* range: Array of values to be tested against the given criteria.

* criteria: The condition to be tested in each of the values of the given range.

* average_range: Numeric values to be evaluated against the criteria and averaged.



**Notes:**

When range is blank or has text value, **Averageif** returns the #DIV/0! error value.

When a cell in criteria is empty, **Averageif** treats it as 0 value.

When no cell in the range meets the criteria, **Averageif** returns the #DIV/0! error value.

#### Averageifs

**Averageifs** function finds the average of values in a given array that satisfies a set of the given criteria.

**Syntax:**

_= Averageifs( average_range, criteria_range1, criteria1, [criteria_range2, criteria2], ... )_

* average_range: Specific set of values to be averaged if the criteria range meets the provided criteria.

* criteria_range1: Array of values to be tested against the given criteria.

* criteria1: The condition to be tested on each of the value of the given range.



**Notes:**

When average_range is blank or has text value, **Averageifs** returns the #DIV/0! error value.

When a cell in a criteria range is empty, **Averageifs** treats it as a 0 value.

When cells in average_range cannot be translated into numbers, **Averageifs** returns the #DIV/0! error value.

#### Cot

The **Cot** function returns the cotangent of an angle specified in radians.

**Syntax:**

_Cot(number)_

Where,

* number-angle radians to get the cotangent value.

**Remarks:**

'#NUM!'-occurs when the number is out of the range.

'#VALUE!'-occurs when the number is a non-numeric value.

#### CSC

The **CSC** function returns the cosecant of an angle specified in radians.

**Syntax:**

_CSC(number)_ 

where:

* number-angle radians to get the cosecant value.

 **Remarks:**

'#NUM!'-occurs when the number is outside its constraints.

'#VALUE!'-occurs when the number is a non-numeric value.

#### CSCH

The **CSCH** function returns the hyperbolic cosecant of an angle specified in radians.

**Syntax:**

_CSCH(number)_

Where:

* number-angle radians to get the hyperbolic cosecant value.

 **Remarks:**

'#NUM!'-occurs when the number is outside its constraints.

'#VALUE!'-occurs when the number is a non-numeric value.

#### ACOT

The **Acot** function retrieves the principal value of the inverse trigonometric cotangent of a number.

To obtain in degrees, use **Degrees** function before **Acot** function.

**Syntax:**

_ACOT(number) or DEGREES ACOT(number)_

Where,

* number that is to be converted into acotangent.

 **Remark:**

'#VALUE!'-occurs when the number is a non-numeric value.

The returned angle when given in radians in the range of 0 (zero) to pi.

#### Acoth

The **Acoth** function retrieves the inverse hyperbolic cotangent of a number.

**Syntax:**

_Acoth(number)_

Where,

* number that is to be converted into cotangent.

**Remarks:**

'#NUM!'-occurs when number is lesser than one.

'#VALUE!'-occurs when absolute value of number is lesser than one.

#### Trunc

The **Trunc** function truncates a supplied number to a specified number of decimal places.

**Syntax:**

_TRUNC( number, [num_digits] )_

Where,

* number is the initial number that is truncated.

* [num_digits] is an optional argument that specifies the number of decimal places to truncate the supplied number to. The default value is 0.



#### Combina

For a given number of items, the **Combina** function returns the number of combinations.

**Syntax:**

_COMBINA(number1, number2)_

Where,

* number1 is total number of items.

* number2 is total number of items to be chosen.



**Remarks:**

'#NUM!'-occurs when either value is out of range.

'#VALUE!'-occurs when either value is non-numeric.

#### Arabic

A Roman numeral is converted into an Arabic numeral.

**Syntax:**

_ARABIC( romannumeral )_

Where, 

* romannumeral is the text given by you to convert it into Arabic numeral.

**Remarks:**

'#VALUE!'-occurs when text is not a valid value.

'#VALUE!'-occurs when text is not a valid Roman numeral.

Value zero occurs when an empty string is given as an input.

#### Ceiling.Math

The **Ceiling.Math** function returns the number rounded up to a multiple of another number.

**Syntax:**

_Ceiling(number, [significance],  [mode])_

Where,

* number-number that is rounded up to a multiple of significance**.**

* significance-multiple to which the number is rounded.

* mode is for negative numbers; it controls whether the number is rounded toward or away from zero.



#### Decimal

A text representation of a number in a given base to be converted into a decimal number.

**Syntax:**

_DECIMAL(text, radix)_ 

Where,

* text is a string.

* radix is an integer.



**Remarks:**

'#NUM!' or '#VALUE!'-occurs when text or radix is outside the constraints.

#### ISeven

**ISeven** function returns **true** when the given number is an even number and returns **false** when the given number is odd.

**Syntax:**

_=ISeven (value)_

* The given value must be a numeric value. When it is non-integer value, the value is rounded down.

#### N

The **N** function converts the given value into a numeric value.

**Syntax:**

_=N (value)_

* value-A value is required.

Numeric values are converted as numeric values. A date value is converted as a serial number. The Logic operator **true** returns a value of 1. The other values are returned as 0.

#### NA

The **NA** function returns the #N/A error. This error message is produced when a formula is unable to find a value that it needs. This error message denotes **value not available**.

**Syntax:**

_=NA()_

* The NA function syntax has no arguments.

#### SIN

Returns the sine of the given angle.

**Syntax:**

_SIN(number)_

Where,

* number is the angle in radians for which you want the sine.

#### SinH

Returns the hyperbolic sine of a number.

**Syntax:**

_SinH(number)_

Where,

* number is any real number.

### Logical functions

#### And

Returns **true** when all the arguments have a logical value of **True** and returns **false** when at least one argument is **False**.

**Syntax:**

_And(logical1, logical2, ...)_

Where,

* logical1, logical2 ... are multiple conditions to be tested for **true** or **false**.

**Remarks:**

The arguments must evaluate to logical values (True or False).

When an argument does not evaluate to True or false, those values are ignored.

There must be at least one value in the argument list.

#### False

The **False** function returns the logical value for the **false**.

**Syntax:**

_False(stringvalue)_

Where,

* stringvalue is to provide an empty string.

#### If

Returns one value when a condition you specify evaluates to **True** and another value when it evaluates to **False**.

Use **If** to conduct conditional tests on values and formulas.

**Syntax:**

_If(logical_test, value_if_true, value_if_false)_

Where**,**

* logical_test is any value or expression that can be evaluated to **True** or **False**.

* value_if_true is the value that is returned if a logical_test is **True**.

* value_if_false is the value that is returned if a logical_test is **False**.



**Remark:**

Countif and Sumif are additional methods that provide conditional calculations.

#### IfError

**IfError** function tests when an initial given value (or expression) returns an error, and then, this function returns a second given argument. Otherwise, the function returns the initial tested value.

**Syntax:**

_= IfError (value, value_error)_

* value-This value is required to check the error.

* value_error-This value is required and returns when the value has an error.



When the value_error is an empty cell, then the function takes the error value as empty string.  

#### IFNA

**IFNA** function returns the value specified when the formula returns the #N/A error value; otherwise, it returns the result of the given formula.

**Syntax:**

_=IFNA (Formula_value, value_if_na)_

* Formula_value: This value is required and the argument that is checked for the #N/A error value.

* value_if_na: This value is required and the value returned when the formula evaluates to the #N/A error value. 



#### Not

Reverses the value of its argument.

**Syntax:**

_Not(logical)_

Where,

* logical is a value or expression that can be evaluated to **True** or **False**.

#### True

The **True** function returns the logical value for **True**.

**Syntax:**

_True(stringvalue)_

Where,

* stringvalue is to provide an empty string.

#### OR

Returns **True** when any argument is **True**; returns **False** when all arguments are **False**.

**Syntax:**

_OR(logical1, logical2, ...)_

Where,

* logical1, logical2 ... are conditions to test that can be either **True** or **False**.

**Remark:**

The arguments must evaluate to logical values such as **True** or **False** or in arrays or references that 

contain logical values.

#### XOR

**XOR** function returns the exclusive **OR** for the given arguments.

**Syntax:**

_XOR (logical_value1, logical_value2…)_

* Logical_value1: This is a required value and can be either **true** or **false**, and can be logical values, arrays, or references.

When the given arguments do not have the logical values, **XOR** returns the #VALUE! error value. 

### Information functions

#### Cell

The **Cell** function returns information about a given cell. This can be information in relation to the contents, formatting, or location of the cell. 

**Syntax:**

_Cell( infoType, reference)_

Where,

* infoType argument is a text string that specifies the type of information to be returned.

* reference is the cell for which the information is to be returned. 



#### Error.Type

**Error.Type** function returns an integer for the given error value that denotes the type of given error.

**Syntax:**

_= Error.Type(value)_

* Value-The given value is required.

Here is the: 

_Return Value of Function_

<table>
<tr>
<td>
<b>Given Value</b></td><td>
<b>Return Value Of Function</b></td></tr>
<tr>
<td>
#NULL!</td><td>
1</td></tr>
<tr>
<td>
#DIV/0!</td><td>
2</td></tr>
<tr>
<td>
#VALUE!</td><td>
3</td></tr>
<tr>
<td>
#REF!</td><td>
4</td></tr>
<tr>
<td>
#NAME?</td><td>
5</td></tr>
<tr>
<td>
#NUM!</td><td>
6</td></tr>
<tr>
<td>
#N/A</td><td>
7</td></tr>
<tr>
<td>
#GETTING_DATA</td><td>
8</td></tr>
<tr>
<td>
Anything else</td><td>
#N/A</td></tr>
</table>

#### IsBlank

The **IsBlank** function checks for blank or null values.

**Syntax:**

_IsBlank(value)_

Where,

* value is the value that you want to test. When the value is blank, this function returns **true**. When the value is not blank, the function returns **false**.

#### IsErr

The **IsErr** function checks whether a value is an error.

**Syntax:**

_IsErr( value )_

Where,

* value is the value that you want to test. When the value is an error value (except #N/A), this function returns **true/false** to indicate whether a value is an error or not.

#### IsError

Returns **true** when the value is a string that starts with a #.

**Syntax:**

_IsError(value)_

Where,

* value is the value that is to be tested.

#### IsRef

**IsRef** function returns the logical value **true** when the given value is a reference value; otherwise, the function returns **false**.

**Syntax:**

_=IsRef(given_value)_

* given_value: This value is required and is to be tested. The value argument can be a blank (empty cell), error, logical value, text, number, or reference value, or a name referring to any of these.

#### IsLogical

The **IsLogiacl** function checks whether a value is a logical value and returns **true** or **false**.

**Syntax:**

_IsLogical( value )_

 Where,

* This value is the value that you want to test. When the value is a **true** or **false** value, this function returns **true**. Otherwise, it returns **false**.

#### IsNA

The **IsNA** function returns a Boolean value after determining that the provided value is #NA error value.

**Syntax:**

_IsNA(value)_ 

Where,

* value is the function that is tested.

#### IsNonText

The **IsNonText** function returns the Boolean value after determining that the provided value is not a string.

**Syntax:**

IsNonText(text)

Where,

* text is the value you want to test whether it is a string or not.

#### IsNumber

Returns **true** when the value parses as a numeric value.

**Syntax:**

_IsNumber(value)_

Where,

* value is the value that is to be tested.

#### Info

The **Info** function returns a text string containing information about the current operating environment.

**Syntax:**

_Info(infoType)_ 

Where,

* infoType argument is a text string that specifies the type of information to be returned. 

#### Type

The **Type** function receives a value and returns an integer that represents the supplied value's data type. 

**Syntax:**

_Type(value)_

Where,

* value can be input either directly as a value returned from a formula or as a reference to a cell that contains a value. 

#### IsFormula

The **IsFormula** function returns **true** or **false** when there is a reference to a cell that contains a formula.

**Syntax:**

_IsFormula (reference)_

Where,

* Reference is a reference to the cell you want to test.

**Remark:**

'#VALUE!'-occurs when reference is not a valid data type.

#### IsOdd

**IsOdd** function returns **true** when the given number is an odd number and returns **false** when the given number is even.

**Syntax:**

_= IsOdd (value)_

* The given value must be a numeric value. When it is a non-integer value, the value is rounded down.

#### IsRef

**IsRef** function returns the logical value **true** when the given value is a reference value; otherwise, the function returns **false**.

**Syntax:**

_= IsRef(given_value)_

* given_value: This value is required and is to be tested. The value argument can be a blank (empty cell), error, logical value, text, number, or reference value, or a name referring to any of these

#### IsText

The **IsText** function returns a Boolean value after determining that the provided value is a string.

**Syntax:**

_IsText(text)_

where**,**

* text is the value you want to test if it is a string or not.

### Web Functions

#### EncodeURL

The **EncodeURL** function retrieves an URL-encoded string.

**Syntax:**

_EncodeURL(name)_

Where,

* name denotes a string that is to be URL encoded.

