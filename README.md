# SWE_2021_41_2024_2_week_6

##Week 4 Assignment
> Repository
> > https://github.com/LoftSpace/SWE_2021_41_2024_2_week4.git

<code>
  def isHappy(n: int) -> bool:
    def get_next(number):
        total_sum = 0
        while number > 0:
            digit = number % 10
            total_sum += digit * digit
            number //= 10
        return total_sum

    seen = set()
    while n != 1 and n not in seen:
        seen.add(n)
        n = get_next(n)

    return n == 1

</code>

---python
  
    
---
> ###Description
> > A happy number is defined as a number that reaches 1 when replaced by the sum of the squares of its digits repeatedly. If this process return 1, the number is happy and if the process is in infinite loop, the number is unhappy.


##Week 5 Assignment
> ###Repository
> >  
