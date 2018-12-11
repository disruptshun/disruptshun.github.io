---
layout: post
title: You're up and running!
---

Validation of CC's: "Validate they are the correct length, used for validatoin of CC numbers on an order form"
####Visa:

Visa card numbers start with a 4. New cards have 16 digits. Old cards have 13 ^4[0-9]{12}(?:[0-9]{3})?$
####MasterCard:

MasterCard numbers either start with the numbers 51 through 55 or with the numbers 2221 through 2720. All have 16 digits. ^(?:5[1-5][0-9]{2}|222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12}$
####American Express:

American Express card numbers start with 34 or 37 and have 15 digits. ^3[47][0-9]{13}$
####Diners Club:

Diners Club card numbers begin with 300 through 305, 36 or 38. All have 14 digits.
There are Diners Club cards that begin with 5 and have 16 digits. These are a joint venture between Diners Club and MasterCard, and should be processed like a MasterCard. ^3(?:0[0-5]|[68][0-9])[0-9]{11}$
####Discover: -Discover card numbers begin with 6011 or 65. All have 16 digits. ^6(?:011|5[0-9]{2})[0-9]{12}$

####JCB:

CB cards beginning with 2131 or 1800 have 15 digits. JCB cards beginning with 35 have 16 digits. ^(?:2131|1800|35\d{3})\d{11}$ J
Used to determine if a CC looks valid and does not determine the brand
''' (?:4[0-9]{12}(?:[0-9]{3})? # Visa | (?:5[1-5][0-9]{2} # MasterCard | 222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12} | 3[47][0-9]{13} # American Express | 3(?:0[0-5]|[68][0-9])[0-9]{11} # Diners Club | 6(?:011|5[0-9]{2})[0-9]{12} # Discover | (?:2131|1800|35\d{3})\d{11} # JCB )$ '''

Search documents for CC numbers: "Replace the ^ .. & with a #word boundry \b
''' \b4[0-9]{12}(?:[0-9]{3})?\b # Visa \b(?:5[1-5][0-9]{2}|222[1-9]|22[3-9][0-9]|2[3-6][0-9]{2}|27[01][0-9]|2720)[0-9]{12}$\b # MasterCard \b3[47][0-9]{13}\b # American Express \b3(?:0[0-5]|[68][0-9])[0-9]{11}\b # Diners Club \b6(?:011|5[0-9]{2})[0-9]{12}\b # Discover \b(?:2131|1800|35\d{3})\d{11}\b # JCB '''
