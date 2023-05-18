# LCprogress
for future use to add to a database on a personal website.leetcodes problems I did and what I learned from them. 

| id  |      Date | Problem Name | Difficulty
|-----|-----------|--------------|-----------
| 1   | 5/14/2023 | TwoSum       | Easy
| 2   | 5/15/2023 | Palindrome Problem | Easy
| 3 | 5/18/2023 | Roman to Integer | Easy


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

## Roman to Integer

```
var romanToInt = function(s) {
    roman = s.split('');
    let totalScore = 0;
    for (let i = 0; i < roman.length; i++) {
        if (roman[i] === 'I' && (roman[i+1] === 'V' || roman[i+1] === 'X')){
            totalScore -= 1;
        }
        else if (roman[i] === 'X' && (roman[i+1] === 'L' || roman[i+1] === 'C')){
            totalScore -= 10;
        }
        else if (roman[i] === 'C' && (roman[i+1] === 'D' || roman[i+1] === 'M')){
            totalScore -= 100;
        }
        else if (roman[i] === 'I'){
            totalScore += 1;
        }
        else if (roman[i] === 'V'){
            totalScore += 5;
        }
        else if (roman[i] === 'X'){
            totalScore += 10;
        }
        else if (roman[i] === 'L'){
            totalScore += 50;
        }
        else if (roman[i] === 'C'){
            totalScore += 100;
        }
        else if (roman[i] === 'D'){
            totalScore += 500;
        }
        else if (roman[i] === 'M'){
            totalScore += 1000;
        }
    };
    return totalScore;
};
```

Terrible brute force method. I must come back to this once i understand hashmaps better.
I shouldve used a dictionary to hold the values as well, and somehow mapped a method that was more efficient.