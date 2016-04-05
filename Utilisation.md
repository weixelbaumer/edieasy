1/ Receive EDIFACT messages
- The EDIFACT file must have UNB and UNZ segment (please see UNECE documentation)
- The EDIFACT file must have minimum 1 Message (UNH-UNT).

2/ In your PHP source :
- Include "initialize.php" file (define contant and add class EDIFACT)
- Creat a new EDIFACT class
- Load EDIFACT file for analize structure (return TRUE or FALSE)
- Position the pointer of message in the first UNH (FindUNH methode)
- Load Message EDIFACT structure for referentiel structure message UNECE

- Choose I: Ckeck the message with methode ValidMessage()

- Choose II : Read Direct the message (The validation will be done at each read data segment).. more slow process....

While Read is TRUE do your work ....

See file index.php for more example...