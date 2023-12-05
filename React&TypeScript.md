stateをpropsで渡す
```
import { Dispatch, SetStateAction } from 'react'

type Props = {
    input: string
    setInput: Dispatch<SetStateAction<string>>
}
```
