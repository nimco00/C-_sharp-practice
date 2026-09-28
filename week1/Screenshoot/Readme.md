#  Visual C# Chapter 1 Practice

##  first picture
Gudaha qeybtan waxaa ku xusan tusaale aasaasi ah oo ku saabsan sida koodh loogu xiro **Event Handler** leh `MessageBox` gudaha Visual C#.



## Dulmar Koodhka (Code Overview)

Koodhkan wuxuu maamulayaa `button3_Click` event-ka. Marka uu user-ku riixo batanka ama PictureBox-ka, wuxuu soo baxaysaa daaqad yar (Pop-up Box) oo muujinaysa farriin soo dhoweyn ah.



##  Visual C# Code

csharp
private void button3_Click(object sender, EventArgs e)
{
    // Shows a welcoming message box when the user clicks the picture
    MessageBox.Show("welcome best class");
}

## second picture

# C# Hello World GUI Project

Welcome to my simple C# Windows Forms application! This is a basic introductory project that demonstrates how to display a message box using an event handler in C#.

## Project Overview

The main purpose of this small application is to show how button click events work in C# GUI apps. When the user clicks on the main button (`button1`), a standard pop-up message box appears with the text `"Hello World"`.

## Source Code

Here is the event handler code used for the button click event:

csharp
private void button1_Click(object sender, EventArgs e)
{
    // Displays dialog box containing the message "Hello World"
    MessageBox.Show("Hello World");
}

## third picture

# C# Label Display Application

Kani waa mashruuc yar oo aasaasi ah oo lagu muujinayo sida loogu isticmaalo **Label Control** gudaha C# Windows Forms application. Mashruucan wuxuu muujinayaa sida qoraal loogu soo bandhigo Label marka uu user-ku riixo Button.



##  Dulmar Koodhka (Code Overview)

Marka uu user-ku riixo batanka (`button2`), koodhku wuxuu si toos ah u beddelayaa ama u siinayaa qoraalka `"Jamhuuriya University"` hantida **Text property** ee Label-ka loo bixiyay `answerlabel`.


##  C# Event Handler Code

csharp
private void button2_Click(object sender, EventArgs e)
{
    // Assigns the string "Jamhuuriya University" to the Text property of answerLabel
    answerlabel.Text = "Jamhuuriya University";
}
