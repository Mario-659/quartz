
**Idea**
Input: https://www.reddit.com/r/ChatGPT/comments/1pt91zd/your_year_with_chatgpt/
Output: https://www.urlshort.com/61Gj8
and Vice Versa

### Design
1. Take URL
2. Save in Database
3. Return shortened ULR based on PRIMARY KEY

Tradeoffs:
Growing DB with each shortening
Multiple ID's for the same value

Constraints:
Input length depends on hashing algorithm

In DB 3 columns:
`PRIMARY KEY ID | SHORTENED ID | VALUE`

> I'm not sure how to create PRIMARY KEY ID with constraint applicable to shortening algorithm


PRIMARY KEY ID <- pg_hashids -> SHORTENED ID

When User enters new new URL it is being saved in DATABASE and shortened ID is returned.

When User enters shortened URL, shortened ID decodes PRIMARY KEY which is used to fetch URL VALUE.


**References:**
PostgreSQL extension that converts number into short id -> https://github.com/iCyberon/pg_hashids
It's a port of a port of this https://sqids.org/faq

### Safe and unreserved URL characters
```
A-Z, a-z, -, _, ., ~, 0-9
26 + 26 +4 = 56 - number of safe characters to use in shortened URL
```

Combinations:
66 ** 5 =    1 252 332 576
66 ** 6 = 82 653 950 016

62 combinations with A-Z, a-z, 0-9


# References
Counter argument to URL shortener (?) - [blog post](https://saneengineer.com/posts/2026-02-10-url-shortener/index.html), got from [LinkedIn post](https://www.linkedin.com/posts/anivan_were-training-engineers-to-solve-imaginary-share-7426911498863767552-j9bz?utm_source=share&utm_medium=member_desktop&rcm=ACoAADV8KpIBaZ1JLEeKUDwNpr78r6cTMYwZEtg)
