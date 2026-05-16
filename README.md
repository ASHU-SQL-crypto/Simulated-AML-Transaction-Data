# Simulated-AML-Transaction-Data
The project is about random AML data set which I have designed to montior the credits of between 8k to 10k done in the UAE via branch and ATM.

SELECT *
  FROM [master].[dbo].[Transactions]
  WHERE TxnType = 'credit'
    AND Amount BETWEEN 8000 AND 10000
    AND Country = 'UAE'
    AND Channel IN ('branch', 'ATM');
