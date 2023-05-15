# LCprogress
for future use on leetcodes problems I did and what I learned from them

| id  |      Date | Problem Name | Difficulty
|-----|-----------|--------------|-----------
| 1   | 5/14/2023 | TwoSum       | Easy
| 2   | 5/15/2023 | Palindrome Problem | Easy


<!-- title -->
## TwoSum problem
```
var twoSum = function(nums, target) {
    for (let i=0; i < nums.length-1; i++){
        for (let x=i+1; x < nums.length; x++){
            if ((nums[i]+nums[x]) == target) {
                return [i,x];
            }
        }
    }
};
```

I learned about arrays and parsing through them.
I should go back to this problem once i have a better understanding of Hashmaps.
I should also go and study how to read time compelxity

## Palindrome Number

```
var isPalindrome = function(x) {
    backward = x.toString().split('').reverse().join('');
    forward = x.toString();
    if (forward === backward) {return true;}
    else {return false;}
};
```

Learned how to convert from int to string
splitting string into array
fairly easy question.
