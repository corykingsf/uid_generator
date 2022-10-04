### Overview
Experiment code which generate number by predefined value, which has the same trend.

### Usage

```
import (
	"fmt"

	generator "github.com/corykingsf/uid_generator"
)

func main() {
	var pre int64 = 123
	id := generator.New().Generate(pre)
	fmt.Printf("ID string  ID: %s\n", id)

	parsedPre, err := generator.New().ParseString(id.String())
	if err != nil {
		fmt.Println(err)
		return
	}
	fmt.Printf("parsed Pre is: %d\n", parsedPre)
}

```
