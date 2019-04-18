# fizzbuzz
 const fizzBuzzer = startNumber =>
{
  if (!Number.isInteger(startNumber))
  {
    return "Invalid Input, only numbers allowed";
  }
  
  if (startNumber < 1 || startNumber > 100)
  {
    return "Invalid Input, enter number between 1 - 100";
  }

  const initialPrimes = [2, 3, 5, 7, 11];

  for (let index = startNumber; index < 10; index++) 
    
  {
    let message = "  ";
    
    if (
      
  (index !== 1 && initialPrimes.includes(index)) ||
      (index !== 1 &&
        index % 2 !== 0 &&
        index % 3 !== 0 &&
        index % 5 !== 0 &&
        index % 7 !== 0)
    )
      
    {
      message = index + " is prime";
      
    } else if (index % 3 === 0 && index % 5 === 0)
    {
      message = index + " is fizzbuzz";
    } 
    else if (index % 3 === 0)
    {
      message = index + " is fizz";
    } 
    else if (index % 5 === 0) 
    {
      message = index + " is buzz";
    } 
    else
    {
      continue;
    }
    console.log(message);
  }
};

console.log(fizzBuzzer("string"));
console.log(fizzBuzzer(120));
console.log(fizzBuzzer(100));
console.log(fizzBuzzer(-1));
console.log(fizzBuzzer(1));
console.log(fizzBuzzer(5));
