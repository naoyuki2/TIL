既存の配列を条件によって新しい配列に作り直すことができる。
```
import allResults from "./results.js";

const Grouping = (grade) => {
    const newResults = allResults.filter((result) => {
        return result.grade === grade;
    })
    return newResults;
}

console.log(Grouping(2));
```
