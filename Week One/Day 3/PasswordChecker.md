```bash
#!/bin/bash

echo -n "Enter Your Password: "
read -s password
echo

length=${#password}
score=0

# +2 points: Minimum length 8
[[ $length -ge 8 ]] && ((score+=2))

# +1 point: Has lowercase letter
echo "$password" | grep -q '[a-z]' && ((score++))

# +1 point: Has uppercase letter
echo "$password" | grep -q '[A-Z]' && ((score++))

# +2 points: Has digit
echo "$password" | grep -q '[0-9]' && ((score+=2))

# +2 points: Has special character
echo "$password" | grep -q '[!@#$%^&*()_+{}\[\]:;<>,.?/~\\-]' && ((score+=2))

# +2 points: Length ≥ 12 (bonus for longer pass)
[[ $length -ge 12 ]] && ((score+=2))

# Cap score at 10
[[ $score -gt 10 ]] && score=10

# Strength classification
if [[ $score -le 4 ]]; then
    strength="Weak"
elif [[ $score -le 7 ]]; then
    strength="Medium"
else
    strength="Strong"
fi

echo "Password Strength: $strength"
echo "Score: $score / 10"

```