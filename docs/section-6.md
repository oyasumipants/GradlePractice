
`gradle hello`

`console`

```
Starting a Gradle Daemon, 1 busy Daemon could not be reused, use --status for details

> Task :hello
Hello world!

BUILD SUCCESSFUL in 4s
1 actionable task: 1 executed
```

`gradle -q hello`

`console`

```
Hello world!
```

左シフト `<<` は使われなくなったので、エラーが起きる

`gradle hello`

`console`

```
task hello << {
	println 'Hello world'
}
```

`console`

```
FAILURE: Build failed with an exception.

* Where:
Build file '/Users/◯◯◯◯/Documents/MyProject/GradlePractice/src/section-6/build.gradle' line: 1

* What went wrong:
A problem occurred evaluating root project 'section-6'.
> Could not find method leftShift() for arguments [build_3l1vbj60gf7qt4qgcxh29oup2$_run_closure1@2528e3a] on task ':hello' of type org.gradle.api.DefaultTask.

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 647ms
```