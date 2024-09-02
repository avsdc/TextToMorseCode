                                                      **TextToMorseCode**

**History Of Morse Code:**

Morse code is named after Samuel Morse, who developed a system of encoding text characters as a series of dots and dashes, for use in telecommunication. It was widely used in World War 2, and the Korean and Vietnam wars.

International Morse code encodes the letters of the English alphabet from A-Z, the numbers 0-9, and some punctuation marks. Each Morse code symbol is represented by a 
sequence of dots and dashes.

**Morse Code Alphabet**
This Morse code chart shows the series of dots and dashes that make up each letter of the alphabet.
A . _
N _ .
B _ . . .
O _ _ _
C _ . _ .
P . _ _ .
D _ . .
Q _ _ . _
E .
R . _ .
F . . _ .
S . . .
G _ _ .
T _
H . . . .
U . . _
I . .
V . . . _
J . _ _ _
W . _ _
K _ . _
X _ . . _
L . _ . .
Y _ . _ _
M _ _
Z _ _ . .

**Morse Code Numbers**
1 . _ _ _ _
6 _ . . . .
2 . . _ _ _
7 _ _ . . .
3 . . . _ _
8 _ _ _ . .
4 . . . . _
9 _ _ _ _ .
5 . . . . .
0 _ _ _ _ _

Punctuation
Character
Composed of:
Sounds Like



Period .
. _ . _ . _
didahdidahdidah
Comma ,
_ _ . . _ _
dahdahdididahdah
Question mark ?
. . _ _ . .
dididahdahdidit
Parentheses ( )
_ . _ _ . _
dahdidahdahdidah
Apostrophe '
. _ _ _ _ .
didahdahdahdahdit
Semicolon ;
_ . _ . _ .
dahdidahdidahdit
Colon :
_ _ _ . . .
dahdahdahdididit
Quotation marks "
. _ . . _ .
didahdididahdit
Hyphen -
_ . . . . _
dahdididididah
Fraction bar /
_ . . _ .
dahdididahdit
Error
. . . . . . . .
didididididididit
Dollar sign $
. . . _ . . _
didididahdididah





**Description Of The Project:**

The project textToMorseCode in Python converts text to Morse Code and Morse Code to Text. The project consists of a main.py file for automatic program execution, and index.html for user-interface.

The index.html file uses a Flaskform with two TextAreaFields for input and output, and SubmitField for submit. Text typed into the input field, is converted to morse code, and displayed in the output field. Morse code pasted into the input field, is converted to text, and displayed in the output field.

A dictionary called morse_code_dict uses capital letters of the English alphabet, numbers from 0-9, and punctuation marks from the list[', “,  :,  ;,  ?,  !, ,] as keys and a series of dots and dashes representing each of these characters as values, associated with each key.
A list is created from the morse_code_dict keys called keys_list, and another list called values_list for the morse_code_dict values.

The class MyForm takes as parameter FlaskForm and consists of two TextAreaFields for input, and output, and submit for SubmitField.

The program runs on port 5000, and displays the user interface consisting of a form with two text area fields, one for input, one for output, and one for submit. The index() function is executed for app.route(“/”). The form is validated on submit, and input string, string1 is retrieved from the input area of the form. The length of the function re.findall() with pattern 0-9 for numbers in string1 returns the total numbers in the string, and for pattern A-Z for characters in string1 returns the total number of letters in the string.

List comprehension is used to find the index of the last letter in each word in the string.

If there are letters and numbers in the string, the function textToMorseCode() is executed, and if there are dots and dashes in the string, morseCodeToText() is executed. Index.html is rendered on the form, and string2 is displayed in the output text area.

textToMorseCode() converts a text string typed into the input text field into Morse Code and displays in the output.
if char is alphanumeric, and index of char is not in the last_ltr_lst i.e. char is a letter in the beginning or middle of the word, then the
         if block statements are executed, the output string gets concatenated with the morse code encoding for the character and a space.
        In the else part, if character is a space, a / gets concatenated to the output string, if the character is at the end of a word, it is encoded
        using the morse_code_dict. In all other cases, i.e. when there are punctuation marks, the morse_code_dict for punctuation gets encoded and concatenated
        to the output_string.

morseCodeToText converts MorseCode input into the input TextAreaField into text in the output TextAreaField.

if a char in the input string i.e. in_str has a '.' or '-', the dot or dahs gets inserted into the ltr_str. If the char is not a dot or dash, in the else part if the char is a space, the ltr_str is decoded (for a key in the morse_code_dict), and key concatenated to out_str, if the char is a '/', ltr_str is decoded, and key and space is concatenated to the out_str. The ltr_str for the punctaution mark at the end of the string is decoded after the for loop execution completes, and out_str is returned from the morseCodeToText() function.


