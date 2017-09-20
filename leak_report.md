# Leak report
Memory errors and leaks happen because we do not free allocated memory;
So in this code we allocated memory for result online 41 (if string is not empty) and we never free it after.
So what i did was i freed this allocated chunk in the "is_empty()" method. But i had to check if (strlen(cleaned) !=0) because if it was empty then we never ***allocated*** memory for that.
