An example to a pipeline that will run the verify-signed-rpms task and validate the results.
Since the `onError` feature is not working in the task level, but only in the step level
I added another step to our task to extract the exit-code of the verify-signed-rpms step
and another task that will get this exit-code and the output as parameters and validate them.