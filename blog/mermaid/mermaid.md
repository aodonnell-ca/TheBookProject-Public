``` mermaid
graph TD;
    CTO[Frank - CTO]
    VP_Engineering[Jennifer - VP Engineering]
    Director_QA[Charlie - Director of QA]
    QA_Tester1[Joe - QA Tester]
    QA_Tester2[Bob - QA Tester]
    QA_Tester3[Glue - QA Tester]
    SW_Engineer1[Charlotte - SW Engineer]
    SW_Engineer2[April - SW Engineer]
    SW_Engineer3[Roger - SW Engineer]

    CTO --> VP_Engineering
    VP_Engineering --> Director_QA
    VP_Engineering --> SW_Engineer1
    VP_Engineering --> SW_Engineer2
    VP_Engineering --> SW_Engineer3
    Director_QA --> QA_Tester1
    Director_QA --> QA_Tester2
    Director_QA --> QA_Tester3
```
