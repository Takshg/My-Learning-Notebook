# Formulas in spreadsheets

---

# Step by step: Formulas for success

This reading outlines the steps the instructor performs in the next video, [Formulas for success](https://www.coursera.org/learn/ask-questions-make-decisions/lecture/s4RlB/formulas-for-success).  In the video, the instructor explains the basics of using spreadsheet formulas for calculations.

Keep this step-by-step guide open as you watch the video. It can serve as a helpful reference if you need additional context or clarification while following the video steps. This is not a graded activity, but you can complete these steps to practice the skills demonstrated in the video.

### **What you’ll need**

If you’d like to follow along with the first example in this video, choose a spreadsheet tool and open a blank sheet.

If you would like to access the other spreadsheet the instructor uses in this video, click the link to the dataset to create a copy. If you don’t have a Google account, download the data directly from the attachments below.

Link to sales data: [Monthly sales](https://docs.google.com/spreadsheets/d/1XXpOhZu7preCSI9aIhwTXAVwMLjf0CxM-rRZrEdImdk/template/preview)

OR

[Monthly SalesXLSX File](https://d3c33hcgiwev3.cloudfront.net/ktl3n81YTE28QBlSK10L-g_bf3842d4369a4d2ab5ec233ab7cf16e1_Monthly-Sales.xlsx?Expires=1716508800&Signature=h6HaxGtIaAN8OoyTPemEDJhSutOgV1ihmkjlPNEtecN82p~s6ETWeFUqZVULfaDW4Ow7ge5niM1z9UsvLXgwwKbTorzW0oXJdyIHcBXaHFg0xhE~bQDyPGj3BbxH5XbLrCCD-fM1Ffme4kLRjESUFqiS24pnqPIEnO85UBBhN8s_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

## Example 1: Create a formula

Formulas form the groundwork for more complex spreadsheet tasks. Here’s a simple exercise:

1. Open a new spreadsheet.
2. Select cell **A1**.
3. Enter **=2-2** and then press **Enter**. The cell displays the result of **0**.
4. Select cell **A2**.
5. Enter **=31982-17795** and press **Enter**. The cell displays the result 14187.

**Note:** The equal sign (**=**) signifies that you're beginning a formula.

## Example 2: Use cell references in a formula

Cell references make your spreadsheet flexible and responsive to data changes. To implement this:

1. Open the [Monthly sales](https://docs.google.com/spreadsheets/d/1XXpOhZu7preCSI9aIhwTXAVwMLjf0CxM-rRZrEdImdk/template/preview) spreadsheet.
2. To find the total sales for April through July of 2017, select cell **F2**.
3. Enter the formula **=B2+C2+D2+E2** and then press **Enter**. You now have the total sales for this timeframe.
4. But what if the data in one of the cells was incorrect? Select cell **D2** and enter **47002** to correct the entry. Press **Enter**.
5. Notice that your spreadsheet automatically recalculates the sum in cell **F2**.

## Example 3: Copy a formula

Copying and pasting formulas saves time and helps ensure consistency across your calculations. To do this:

1. In the **Monthly sales** spreadsheet, select cell **F2**.
2. From the **Edit** menu, choose **Copy**. You can also use the Windows keyboard shortcut **Ctrl+C** or Mac keyboard shortcut **Command+C** to copy the formula.
3. Select cell **F3** and from the **Edit** menu, choose **Paste**. Alternatively, press **Ctrl+V** (Windows) or **Command+V** (Mac) to paste the formula into cell **F3**.

**Note:** After pasting into cell **F3**, the formula in that cell will be **=B3+C3+D3+E3**.

## Example 4: Calculate the average sales

Use formulas for different calculations, such as finding an average:

1. In the **Monthly sales** spreadsheet, select cell **G1**.
2. Enter **Average Sales** in cell **G1** and press **Enter**.
3. Select cell **G1** again. In the toolbar, select **Bold** to bold the text.	**Note:** Naming columns in spreadsheets enhances clarity by indicating the purpose of the numbers.
4. Select cell **G2**.
5. Enter **=(B2+C2+D2+E2)/4** and press **Enter** to calculate the average sales over this timeframe. 
**Note:** This formula calculates the average of sales for the month, including cases in which there are no sales (blank cells), which are treated as zeroes in the calculation. If the business had zero sales for a month, the blank cell is still included in the calculation to maintain accuracy.
6. Copy and paste the formula from cell G2 into cells **G3** and **G4**.

## Example 5: Calculate the percent change in sales

Use a different formula to calculate percent change:

1. In the **Monthly sales** spreadsheet, select cell **H1**.
2. In cell **H1**, enter **June to July Change**. Bold this text.
3. In cell **H2**, enter **=(E2-D2)/D2** to calculate the percentage change in sales.
4. To format the value as a percentage, on the toolbar, select the **%** button. You now find that the percent change in sales between June and July is 247.5%.
5. Copy this formula to cell **H3**. Notice that the spreadsheet copies both the formula and the percentage formatting.

## Example 6: Correct a formula error

Correcting formula errors ensures your data analysis remains accurate and trustworthy. Here’s how to troubleshoot one common mistake:

1. In the **Monthly sales** spreadsheet, copy the formula from cell **H2** to cell **H4** and press **Enter**.
2. Notice the error displayed in cell **H4**. This error occurs because the formula is trying to divide by a value of zero. The reason for this error is that cell D4 is blank, and in this context, the spreadsheet interprets it as having a value of zero.
3. To resolve the error, type **75866** in cell **D4** and press **Enter**. Notice that the error disappears, and cell **H4** now displays **121.16%**.

---

# Quick Reference: Formulas in spreadsheets

You have been learning a lot about spreadsheets and all kinds of time-saving calculations and organizational features they offer. One of the most valuable spreadsheet features is a **formula**. As a quick reminder, a formula is a set of instructions that does a specific calculation using the data in a spreadsheet. Formulas make it easy for data analysts to do powerful calculations automatically, which helps them analyze data more effectively. Below is a  quick-reference guide to help you get the most out of formulas.

## Formulas

### **The basics**

- When you enter a formula in math, it generally ends with an equal sign (2 + 3 = ?). But with formulas, they always start with one instead (**=A2+A3**). The equal sign tells the spreadsheet that what follows is part of a formula, not just a word or number in a cell.
- After you enter the equal sign, most spreadsheet applications will display an autocomplete menu that lists valid formulas, names, and text strings. This is a great way to create and edit formulas while avoiding typing and syntax errors.
- A fun way to learn new formulas is just by typing an equal sign and a single letter of the alphabet. Choose one of the options that pops up and you will learn what that formula does.

### **Mathematical operators**

- The mathematical operators used in spreadsheet formulas include:
- Subtraction – minus sign ( - )
- Addition – plus sign ( + )
- Division – forward-slash ( / )
- Multiplication – asterisk ( * )

### **Auto-filling**

The lower-right corner of each cell has a fill handle. It is a small *green square* in Microsoft Excel and a small *blue circle* in Google Sheets.

- Click the fill handle square or circle for a cell and drag it down a column to auto-fill other cells in the column with the same value or formula in that cell.
- Click the fill handle square or circle for a cell and drag it across a row to auto-fill other cells in the row with the same value or formula in that cell.
- If you want to create a numbered sequence in a column or row, do the following: 1) Fill in the first two numbers of the sequence in two adjacent cells, 2) Select to highlight the cells, and 3) Drag the fill handle square or circle to the last cell to complete the sequence of numbers. For example, to insert 1 through 100 in each row of column A, enter **1** in cell A1 and **2** in cell A2. Then, select to highlight both cells, click the fill handle square or circle in cell A2, and drag it down to cell A100. This auto-fills the numbers sequentially so you don't have to enter them in each cell.

### **Absolute referencing**

- Absolute referencing is marked by a dollar sign (**$**). For example, **=$A$10** has absolute referencing for both the column and the row value
- Relative references (which is what you normally do, e.g. “**=A10**”) will change anytime the formula is copied and pasted. They are in relation to where the referenced cell is located. For example if you copied “**=A10**” to the cell to the right it would become “**=B10**”. With absolute referencing “**=$A$10**” copied to the cell to the right would remain “**=$A$10**”. But if you copied **$A10** to the cell below, it would change to **$A11** because the row value isn't an absolute reference.
- Absolute references will not change when you copy and paste the formula in a different cell. The cell being referenced is always the same.
- To easily switch between absolute and relative referencing in the formula bar, highlight the reference you want to change and press the **F4** key; for example, if you want to change the absolute reference, **$A$10**, in your formula to a relative reference, A10, highlight **$A$10** in the formula bar and then press the **F4** key to make the change.

### **Data range**

- When you click into your formula, the colored ranges let you see which cells are being used in your spreadsheet. There are different colors for each unique range in your formula.
- In a lot of spreadsheet applications, you can press the **F2** (or **Enter**) key to highlight the range of data in the spreadsheet that is referenced in a formula. Click the cell with the formula, and then press the **F2** (or **Enter**) key to highlight the data in your spreadsheet.

### **Combining with functions**

- **COUNTIF()** is a formula and a function. This means the function runs based on criteria set by the formula. In this case, **COUNT** is the formula; it will be executed IF the conditions you create are true. For example, you could use **=COUNTIF(A1:A16, “7”)** to count only the cells that contained the number 7. Combining formulas and functions allows you to do more work with a single command.

---

# Spreadsheet errors and fixes

This video focuses on troubleshooting common spreadsheet errors, empowering you to identify and resolve them effectively.

**Key Points:**

- **DIV Error:** Occurs when dividing by zero or an empty cell. To avoid this, use the `IFERROR` function to display "Not applicable" in such cases.
- **ERROR:** Indicates a formula parsing error. Ensure correct syntax and delimiters (e.g., commas) are used.
- **N/A Error:** Data not found by the spreadsheet. Check for typos or missing data in formulas like `VLOOKUP`.
- **NAME Error:** Formula name not recognized. Correct spelling and ensure functions are used correctly (e.g., `VLOOKUP` instead of `VLOKUP`).
- **NUM Error:** Formula calculation impossible due to inconsistent data. Verify data accuracy and order (e.g., start date before end date in `DATEDIF`).
- **VALUE Error:** Problem with formula or referenced cells. Check for incorrect data types or text in numerical fields.
- **REF Error:** Referenced cells deleted, making the formula invalid. Adjust formulas to avoid direct cell references or use `SUM` with a range instead.

**Additional Notes:**

- The video emphasizes the importance of troubleshooting skills for data analysts.
- It provides clear explanations and examples of each error type.
- The video demonstrates how to fix these errors using practical solutions.

**Definitions:**

- **Formula:** A set of instructions used to perform calculations in a spreadsheet.
- **Cell:** The basic unit of a spreadsheet where data is entered and calculations are performed.
- **Error:** A message indicating a problem with a formula or data in a spreadsheet.
- **Parsing Error:** An error caused by incorrect syntax or structure in a formula.
- **Delimiters:** Characters used to separate data items in a formula (e.g., commas).
- **Data Type:** The format of data in a cell (e.g., number, text, date).

**Real-Life Examples:**

- **Finance:** Analyzing financial data and identifying errors in calculations.
- **Marketing:** Analyzing marketing campaign data and identifying errors in data entry.
- **Healthcare:** Analyzing patient data and identifying errors in medical records.

---