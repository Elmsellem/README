# DOCKER SOLUTIONS
## wait for container script

```bash
 #!/bin/bash

CMD="curl -sf http://localhost"

for i in {1..30}
do
	${CMD}
	if [ $? -eq 0 ]
	then
		exit 0
	fi
	echo "Waiting for backend..."
	sleep 3
done

exit 1
```
