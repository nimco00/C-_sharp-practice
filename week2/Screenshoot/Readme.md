#  Date Display - C# Windows Forms

## 1. Project Overview

This is a simple **C# Windows Forms** project.

The program asks the user to enter:

1. Day of the week
2. Month name
3. Numeric day
4. Year

Then, when the user clicks **Show Day**, the program combines the information and displays the full date.

The project follows the basic:

**Input → Process → Output**

structure.

---

# 2. Step 1 — Create Variables

First, we create variables to store the information.

```csharp
string Dayof_week, name_of_month, Full_Date;
int numeric_day;
int year;
```

### Explanation

- `Dayof_week` → stores the day name, for example `Monday`.
- `name_of_month` → stores the month, for example `September`.
- `numeric_day` → stores the day number, for example `28`.
- `year` → stores the year, for example `2026`.
- `Full_Date` → stores the final complete date.

### Screenshot

![Step 1 - Variables](step1.png)

---

# 3. Step 2 — Input Values

Next, we get the values from the TextBoxes.

```csharp
Dayof_week = txtdayoftheweek.Text;
name_of_month = txtdayofmonth.Text;
numeric_day = int.Parse(txtdayofthenumeric.Text);
year = int.Parse(txtyear.Text);
```

### Explanation

`.Text` gets the information that the user typed into a TextBox.

For example:

```text
txtdayoftheweek.Text = Monday
txtdayofmonth.Text = September
txtdayofthenumeric.Text = 28
txtyear.Text = 2026
```

### Why `int.Parse()`?

`TextBox.Text` returns text (`string`).

But `numeric_day` and `year` are integers (`int`), so we convert the text into a number:

```csharp
int.Parse(...)
```

### Screenshot

![Step 2 - Input Values](step2.png)

---

# 4. Step 3 — Process / Concatenation

After getting the input, we combine all values into one variable.

```csharp
Full_Date = Dayof_week + "," + name_of_month + "," + numeric_day + "," + year;
```

This process is called **string concatenation**.

### Example

If the user enters:

```text
Monday
September
28
2026
```

The result becomes:

```text
Monday,September,28,2026
```

### Screenshot

![Step 3 - Process](step3.png)

---

# 5. Step 4 — Output

Now we display the final result in the Label.

```csharp
lbloutput.Text = Full_Date;
```

### Explanation

`lbloutput` is the Label used to show the result.

`.Text` changes the text displayed by the Label.

So the complete flow is:

```text
TextBoxes
   ↓
Variables
   ↓
Concatenation
   ↓
Full_Date
   ↓
lbloutput
```

### Screenshot

![Step 4 - Output](step3.png)

---

# 6. Step 5 — Clear Button

The **Clear** button removes the information from the TextBoxes and Label.

```csharp
private void btnclear_Click(object sender, EventArgs e)
{
    // clearing textbox and label

    txtdayoftheweek.Clear();
    txtdayofmonth.Text = "";
    txtdayofthenumeric.Text = string.Empty;
    txtyear.Clear();
    lbloutput.Text = "";
}
```

### Explanation — One by One

### 1. Clear day of the week

```csharp
txtdayoftheweek.Clear();
```

Removes the text from the TextBox.

### 2. Clear month

```csharp
txtdayofmonth.Text = "";
```

Sets the TextBox text to an empty string.

### 3. Clear numeric day

```csharp
txtdayofthenumeric.Text = string.Empty;
```

`string.Empty` means an empty string.

It is another way to say:

```csharp
txtdayofthenumeric.Text = "";
```

### 4. Clear year

```csharp
txtyear.Clear();
```

Removes the year from the TextBox.

### 5. Clear output

```csharp
lbloutput.Text = "";
```

Removes the displayed date from the Label.

### Screenshot

![Step 5 - Clear Button](step4.png)

---

# 7. Step 6 — Close Button

The **Close** button closes the Windows Form.

```csharp
private void btnclose_Click(object sender, EventArgs e)
{
    // form close - using this keyword and close function

    this.Close();
}
```

### Explanation

```csharp
this.Close();
```

`this` refers to the current Form.

`Close()` closes the current Form.

Therefore:

```csharp
this.Close();
```

means:

> Close this current Windows Form.

### Screenshot

![Step 6 - Close Button](step5.png)

---

# 8. Complete Program Flow

The complete program works in three main stages.

## Stage 1 — Input

The user enters:

```text
Day of Week
Month
Numeric Day
Year
```

The program stores those values in variables.

## Stage 2 — Process

The program combines the values:

```csharp
Full_Date = Dayof_week + "," + name_of_month + "," + numeric_day + "," + year;
```

## Stage 3 — Output

The program displays the result:

```csharp
lbloutput.Text = Full_Date;
```

---

# 9. Complete Show Day Code

```csharp
private void btnshowday_Click(object sender, EventArgs e)
{
    // stage 1 of input
    // creating variable

    string Dayof_week, name_of_month, Full_Date;
    int numeric_day;
    int year;

    // initial values to variable
    Dayof_week = txtdayoftheweek.Text;
    name_of_month = txtdayofmonth.Text;
    numeric_day = int.Parse(txtdayofthenumeric.Text);
    year = int.Parse(txtyear.Text);

    // stage 2 process - concatenation of full date
    Full_Date = Dayof_week + "," + name_of_month + "," + numeric_day + "," + year;

    // stage 3 output using label
    lbloutput.Text = Full_Date;
}
```

---

# 10. Complete Clear Code

```csharp
private void btnclear_Click(object sender, EventArgs e)
{
    // clearing textbox and label

    txtdayoftheweek.Clear();
    txtdayofmonth.Text = "";
    txtdayofthenumeric.Text = string.Empty;
    txtyear.Clear();
    lbloutput.Text = "";
}
```

---

# 11. Complete Close Code

```csharp
private void btnclose_Click(object sender, EventArgs e)
{
    // form close

    this.Close();
}
```

---

# 12. Example

### Input

```text
Day of Week: Monday
Month: September
Numeric Day: 28
Year: 2026
```

### Output

```text
Monday,September,28,2026
```

---

# 13. Important C# Concepts Used

| Concept | Example | Purpose |
|---|---|---|
| Variable | `string Dayof_week;` | Stores data |
| Integer | `int year;` | Stores whole numbers |
| TextBox | `txtyear.Text` | Gets user input |
| `int.Parse()` | `int.Parse(...)` | Converts text to integer |
| Concatenation | `+` | Joins strings and values |
| Label | `lbloutput.Text` | Displays output |
| `.Clear()` | `txtyear.Clear()` | Clears a TextBox |
| `string.Empty` | `Text = string.Empty` | Makes text empty |
| `this.Close()` | `this.Close();` | Closes the Form |
| Event | `btnshowday_Click` | Runs code when button is clicked |

---

# 14. Final Summary

This project is a basic example of a **C# Windows Forms application**.

It teaches three important programming stages:

### Input
Get information from the user.

### Process
Combine and process the information.

### Output
Display the result.

It also demonstrates how to use:

- Variables
- TextBoxes
- Labels
- Buttons
- Events
- `int.Parse()`
- String concatenation
- `.Clear()`
- `string.Empty`
- `this.Close()`

---

## 📁 Screenshots

The screenshots in this README are included in the same folder so the README can display them correctly.
