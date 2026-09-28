# Chapter 2: Processing Data

## Introduction

Chapter 2 wuxuu ka hadlayaa **Processing Data** iyo sida C# loogu shaqeeyo xogta gudaha application-ka.

Casharkan waxaan ku bartay sida user-ka looga qaato xog, loo kaydiyo, loo beddelo, loo xisaabiyo, kadibna natiijada loogu soo bandhigo user-ka.

## Main Topics

### TextBox

TextBox waxaa loo isticmaalaa in user-ku ku geliyo xog. Xogta laga helo TextBox-ka waxaa lagu akhriyaa `Text` property.

### Variables and Data Types

**Variable** waa meel memory-ga lagu kaydiyo xog. Waxaan bartay data types sida:

* `string`  qoraal
* `int`  whole numbers
* `double`  decimal numbers
* `decimal`  numbers u baahan precision badan

### Calculations

C# waxaa lagu sameeyaa calculations iyadoo la isticmaalo:

text
+   -   *   /   %

`%` wuxuu soo saaraa remainder-ka division-ka.

### Parse and ToString

Xogta TextBox-ka waxay ahaanaysaa `string`. `Parse()` waxaa loo isticmaalaa in string loogu beddelo number.

```csharp
int age = int.Parse(ageTextBox.Text);
```

`ToString()` waxaa loo isticmaalaa in value loogu beddelo string.

csharp
ageLabel.Text = age.ToString();


### Exception Handling

Waxaan bartay sida errors-ka runtime-ka loo maareeyo iyadoo la isticmaalo `try` iyo `catch`.

csharp
try
{
    // code
}
catch
{
    // handle error
}
```

### Constants and Fields

**Constant** waa value aan la beddeli karin inta program-ku socdo.

**Field** waa variable lagu declare-gareeyo gudaha class-ka, laakiin method-ka bannaankiisa.

### Math Class

`Math` class waxaa loo isticmaalaa calculations sida:

* Square root
* Power
* Maximum
* Minimum
* Rounding

### GUI Concepts

Casharka wuxuu kaloo ka hadlay:

* Tab Order
* Focus
* BackColor
* ForeColor
* GroupBox
* Panel

### Debugging

Waxaan bartay **debugging**, oo ah habka lagu raadiyo laguna saxo errors-ka program-ka.

Waxaa ka mid ah:

* Breakpoints
* Single-stepping
* Finding logic errors

## 💻 Small Practical Example

Tusaalahan wuxuu qaadanayaa laba number oo user-ku geliyo, kadibna wuxuu isku darayaa.

```csharp
private void btnAdd_Click(object sender, EventArgs e)
{
    try
    {
        double number1 = double.Parse(txtNumber1.Text);
        double number2 = double.Parse(txtNumber2.Text);

        double result = number1 + number2;

        lblResult.Text = result.ToString();
    }
    catch
    {
        MessageBox.Show("Please enter valid numbers.");
    }
}
```

### How it works

1. User-ku wuxuu geliyaa laba number.
2. `Parse()` wuxuu string-ka u beddelaa `double`.
3. Labada number waa la isku daraa.
4. `ToString()` wuxuu result-ka u beddelaa string.
5. Result-ka waxaa lagu soo bandhigayaa Label.
6. `try-catch` wuxuu qabtaa haddii user-ku geliyo xog aan number ahayn.

## Summary

Chapter 2 wuxuu iga caawiyay inaan fahmo sida **data loo qaato, loo kaydiyo, loo process-gareeyo, loona soo bandhigo** gudaha C# application.

Waxaan bartay variables, data types, calculations, input/output, exception handling, constants, Math class, GUI concepts, iyo debugging.

## Instructor / Coordinator

Yahye Ali Isse
Department of Computer Application
Faculty of Computer & Information Technology
Jamhuriya University of Science & Technology