# Windows 11 Copy-Paste Issue or Virus? Regex Pattern Blocking Copy Functionality

I am experiencing a copy-paste issue on Windows 11, and I'm not sure if it's a bug or a potential virus infection. The problem arises when the following two processes are running:

- `C:\Users\Wanten\AppData\Local\DesignInno Innovations\jsc.exe`
- `C:\Users\Wanten\AppData\Local\TradeSecure Innovations\jsc.exe`

The copy-paste functionality becomes problematic as long as these processes are active. Specifically, any string that matches the following regular expression cannot be copied:

```regex
^[13][a-km-zA-HJ-NP-Z1-9]{26,}$
```

Explanation:

- `^[13]`: The first character of the string must be 1 or 3.
- `[a-km-zA-HJ-NP-Z1-9]`: Following characters can be any alphanumeric, excluding 0, lowercase l, uppercase I, and O.
- `{26,}`: The length of the string must be greater than or equal to 27.

Examples of strings that cannot be copied:

```
1TxFiUzvv6YjB1augKJvRzknfG9
1gBNwEEvX1neGi2uvwJxSu1bq6P
1dqj6NNKWLyW4WhVwRGBbJpaZqn
155uvJ2Te7sJebUCHGXpBNTgk43
1Du9VHTn23jznkSEqZEHoBPNSy2
1A58tBordfn8mXyLn29hJYok9ST
13su1kBFZr3JobGWH5JxiR53TGi
1C1P1yF2PWPk6nfAcmAk4SMJvta
1wWKJzvBg2GbS4qVNc6v7mShZzv
1J5dSVxf7RdmkQTqucGV1Gdpbsm
1Z86UUNaZGzihZUhzN2xhsnXJBR
1qUTqC7LTa9rwuLHwRvXPwqjQg9
1wkDFS2mn87LCGYYaa7Tnbz2aVg
18fj8Yi3ecFfK3nZLHp15A2TXF6
1hQVL6BnY2Sf2mE6tvfSxrroEKW
3HBXExyxKnx4E6y416V2MXeFyuV
3cE5FdmtoUiyfGvuMPrYhTtk1kp
32FgKUMdkcMJUYw3zEFwbQY1B4q
32UoEdhnGETQPfKzCDS7e4as3gn
3ApPLHESbgmqRgbCaYm12k8U1a1
3henVS9g2miD3ZoUan2wfphVTNG
3pkmkbxZVfEKVqSUjgq3dTARanr
3Pp8auHSYJBczGRqu9qrP8K5SWW
3zKqEBPHLP3UYBZz4MKrszWMKwn
3W65vzfc77BpvJ9Z44na3hqw4sf
3wk8fqww6jsEXESoEXf7zYCJJeg
38vaR6WQUbZiWjBKUAFvnhWKBkk
3Sp4Majk7ag8i4eTLsexyBXSqKH
3gSzrLBjsuxst92SaXkfWNmNdJn
31wrgiqHafQnHfXzVvN4WdwLJr1
```

If any string contains these patterns, it fails to copy. For instance, copying the text `Some text followed by 31wrgiqHafQnHfXzVvN4WdwLJr1 additional text` results in: `31ihnFtf5667WgCJhobHRLVLiJrE9wHM8s`.

However, if I close these two processes in the Task Manager, the copy-paste functionality returns to normal.

I am uncertain about the origin of these processes – whether they are native to Windows or related to another application, or possibly a virus. When I pause their execution and delete the files, I receive a Windows Script Host error after some time.

![erros](./0-imgs/script%20host%20errors.png)

Any insights or guidance on identifying and resolving this issue would be greatly appreciated.

Here is the video demonstration link: https://www.youtube.com/watch?v=pi8Zz0tJMpA
