# JSON module Lab

In this module your skills will be tested on what you have learned about JSON.

From the `Programmability IDE` perform the following operations.

## Challenge-1

- In the `food.json` file we have updated information about `apple`, similarly update the remaining information (HINT: Use list of dictionaries):

| fruits | calories | fat | carbs |
| ------ | -------- | --- | ----- |
| apple | 95 | 0.3 | 25 |
| banana | 105 | 0.4 | 27 |
| orange | 45 | 0.1 | 11

```
{
 "Fruits": [
  {
     "apple": {
         "calories": 95,
         "fat": 0.3,
         "carbs": 25
     },
     "banana": {
         "calories":105,
         "fat":0.4,
         "carbs":27
     },
     "orange": {
         "calories":45,
         "fat":0.1,
         "carbs":11
     }
    }
   ]
  }
```

## Challenge-2

- In the `food.json` file update information about `vegetables`, similar to how we have done for `fruits`

| vegetables | calories | fat | carbs |
| ---------- | -------- | --- | ----- |
| carrot | 25 | 0.1 | 6 |
| tomato | 22 | 0.2 | 4.8 |
| cucumber | 8 | 0.1 | 1.9 |

```
{
    "fruits": [
        {
            "apple": {
                "calories": 95,
                "fat": 0.3,
                "carbs": 25
            },
            "banana": {
                "calories":105,
                "fat":0.4,
                "carbs":27
            },
            "orange": {
                "calories":45,
                "fat":0.1,
                "carbs":11
            }
        }
    ],
    "Vegetables": [
        {
            "carrot": {
                "calories":25,
                "fat":0.1,
                "cucumber":8
            },
            "tomato": {
                "calories":22,
                "fat":0.2,
                "carbs":4.8
            },
            "cucumber": {
                "calories":8,
                "fat":0.1,
                "carbs":1.9
            }
        }
    ]
}
```

## Challenge-3

- Create a new file `employee-directory.json` and configure it as below.

- Tom is `30` year old Male working as a `Technical Solutions Engineer` at a firm. Represent Tom's information (`Name`, `Sex`, `Age`, `Title`) in JSON format. Create a dictionary named `Employee` and define properties under it.

```
{
  "Employee": {
     "Name":"Tom",
     "Age": 30,
     "Sex":"Male",
     "Title": "Techincal Solutions Engineer"
   }
}
```

## Challenge-4

- Update the JSON file to represent the `Projects` assigned to Tom. Remember Tom works on Multiple projects - `Automation` and `Support`. So remember to use a list.

```
{
  "Employee": {
     "Name":"Tom",
     "Age": 30,
     "Sex":"Male",
     "Title": "Techincal Solutions Engineer",
     "Project": ["Automation","Support"]
   }
}
```
## Challenge-5

- Update the JSON file to include Tom's pay slips. Add a new property `Payslips` and create a list of pay slip details (Use list of dictionaries). Each payslip detail contains `Month` and `Wage`.

| Month | Wage |
| ----- | ---- |
| October | 4000 |
| November | 4500 |
| December | 4000 |

```
{
 "Employee": {
    "Name":"Tom",
    "Age":30,
    "Sex": "Male",
    "Title":"Technical Solutions Engineer",
    "Projects":["Automation","Support"],
    "Payslips":[
        {
          "month":"October",
           "Wage":4000
        },
        {
          "month":"November",
          "Wage":4500
        },
        {
          "month":"December",
          "Wage":4000
        }
      ]
     }
  }
```

The solutions for these challenges are present under `Solutions` folder, however we would encourage to try to figure our the solution yourself before looking at the solutions.

You can use [JSON Crack](https://jsoncrack.com/) to visualize and validate you JSON files.
