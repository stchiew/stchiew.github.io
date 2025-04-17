---
layout: default
title: PowerApps
---

# PowerApps

### Create collection

```
ClearCollect(
    col_MyCollection,
    {Id:1, Title: "Lorem ipsum", Screen: AppScreen, Status: false},
    {Id:2, Title: "Lorem ipsum", Screen: AppScreen, Status: false},
    {Id:3, Title: "Lorem ipsum", Screen: AppScreen, Status: true},
    {Id:4, Title: "Lorem ipsum", Screen: AppScreen, Status: false},
    {Id:5, Title: "Lorem ipsum", Screen: AppScreen, Status: false}
);
```

### Add a running row number to a collection

```
ClearCollect(
    col_Titles,
    ForAll(
        Sequence(CountRows(col_Titles)) As Seq,
        Patch(
            Last(
                FirstN(
                    col_Titles,
                    Seq.Value
                )
            ),
            {Id: Seq.Value}
        )
    )
)
```
