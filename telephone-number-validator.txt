function telephoneCheck(str) {
  
  const regex = /^(1{1}(\s|-)*(\d{3}))(\s|-)*(\d{3})(\s|-)*(\d{4})$|^1{1}(\s|-)*(\()(\d{3})(\))(\s|-)*(\d{3})(\s|-)*(\d{4})$|(?=\d{10})^(\d{10})$|^(\d{3})(\s|-)*(\d{3})(\s|-)*(\d{4})$|^(\()(\d{3})(\))(\s|-)*(\d{3})(\s|-)*(\d{4})$/ig;

  let bool = regex.test(str);
  return bool;
}

/*
regex:

NUMS START WITH 1:
start with 1, but without parantheses
start with 1, use parantheses

NUMS DO NOT START WITH 1:
numbers with 10 digits, without space
numbers with parantheses
numbers without parantheses

*/