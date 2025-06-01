1. Update package model to include all emails attached to account
2. only pass package to job
3. Job should trigger other jobs to send email 
4. THe compilation of emails should be done in the parent job, filtering for unique instances
5. Create a test for the method that extracts the emails to trigger the job:
   - setup tests, creating objects like the package, account and many users (2)
   - Test for when account and user email is the same (1 email returned)
   - Test for when account and user email is different (2 emails returned)