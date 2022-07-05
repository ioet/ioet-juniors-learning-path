# Static Code Analysis

## Contributors

- [Jipson Murillo](https://github.com/Jobzi)
- [Josué Cando](https://github.com/JosueOb)

## Content

- [Introduction](#introduction)
- [Static and dynamic analysis approaches](#static-and-dynamic-analysis-approaches)
- [Benefits](#benefits)
- [Limitations](#limitations)
- [Tools](#tools)
- [Conclusions](#conclusions)
- [References](#references)

## Introduction

In the beginning of software development there was no conscience on how necessary and effective a
review might be, but in the 1970’s, formal review and inspections were recognized as important to
productivity and product quality, and thus were adopted by development projects.
This new approach to software development acknowledges defect removal in the early stages of the
development process proved to produce more reliable and efficient programs.
Therefore, as far as the source code is concerned, it is in the programmer's best interest to
static analysis. Although this does not imply that other forms of software analysis should be
discouraged, on the contrary, the best way to certify that an implementation has the least number of
bugs or defects. The best way to certify that an implementation has the least number of bugs or
defects is to combine static and dynamic analysis measures.

## Static and dynamic analysis approaches

The static analysis approach aims at reviewing the source code, checking for compliance with
specific rules, use of arguments, etc.; the dynamic approach is essentially the execution of the
code, running the program and dynamically checking is essentially the execution of the code, running
the program and dynamically checking for inconsistencies in the results obtained. inconsistencies in
the results obtained. This means that testing and code review are separate and distinguishable
things. are separate and distinguishable things, but it is not advisable for one to occur without
the other. without the other.

## Benefits

There are several benefits of static code analysis tools — especially if you need to comply with an
industry standard.
The best static code analysis tools offer speed, depth, and accuracy.

- **Speed**
  It takes time for developers to do manual code reviews. Automated tools are much faster. Static
  code checking addresses problems early on. And it pinpoints exactly where the error is in the
  code. So, you’ll be able to fix those errors faster. Plus, coding errors found earlier are less
  costly to fix.
- **Depth**
  Testing can’t cover every possible code execution path. But a static code analyzer can.It checks
  the code as you work on your build. You’ll get an in-depth analysis of where there might be
  potential problems in your code, based on the rules you’ve applied. Here's an example of in-depth
  code analysis in Helix QAC.
- **Accuracy**
  Manual code reviews are prone to human error. Automated tools are not. They scan every line of
  code to identify potential problems. This helps you ensure the highest-quality code is in place —
  before testing begins. After all, when you’re complying with a coding standard, quality is
  critical.

## Limitations

Static code analysis is used for a specific purpose in a specific phase of development. But there
are some limitations of a static code analysis tool.
**No Understanding of Developer Intent**

```java
int calculateArea(int length, int width)
{
    return (length + width);
}
```

A static analysis tool may detect a possible overflow in this calculation. But it can’t determine
that function fundamentally does not do what is expected!

**Rules That Aren’t Statically Enforceable**

Some coding rules depend on external documentation. Or they are open to subjective interpretation.

**Possible Defects Lead to False Positives and False Negatives**

In some situations, a tool can only report that there is a possible defect.

```java
int divide(void)
{
    int x;
    if(foo())
    {
        x = 0;
    }
    else
    {
        x = 5;
    }
    return (10/x);
}
```

If we know nothing about foo(), we do not know what value x will have.
The result is undecidable. That means that tools may report defects that do not actually exist (
false positives). Or they may fail to report real defects (false negatives).

### Tools

Static analysis tools compare favorably with manual reviews because they are faster, meaning they
can evaluate programs much more frequently, and they encapsulate some of the knowledge needed to
perform this type of code analysis, so the tool operator is not required to have the same level of
expertise as a human auditor.
Good static analysis tools should be easy to use, which means that their results should be
understandable to ordinary developers who may not know much about security and who educate their
users about good programming practices.

| Language / framework                 | Scan tool                       |
|--------------------------------------|---------------------------------|
| .NET Core                            | Security Code Scan              |
| .NET Framework                       | Security Code Scan              |
| Apex (Salesforce)                    | PMD                             |
| C                                    | Semgrep                         |
| C/C++                                | Flawfinder                      |
| Elixir (Phoenix)                     | Sobelow                         |
| Go                                   | Gosec, Semgrep                  |
| Groovy (Ant, Gradle, Maven, and SBT) | SpotBugs + find-sec-bugs        |
| Helm Charts                          | Kubesec                         |
| Java (Ant, Gradle, Maven, and SBT)   | SpotBugs + find-sec-bugs        |
| Java (Android)                       | MobSF (beta)                    |
| JavaScript                           | ESLint security plugin, Semgrep |
| Kotlin (Android)                     | MobSF (beta)                    |
| Kotlin (General)                     | SpotBugs + find-sec-bugs        |
| Kubernetes manifests                 | Kubesec                         |
| Node.js                              | NodeJsScan                      |
| Objective-C (iOS)                    | MobSF (beta)                    |
| PHP                                  | phpcs-security-audit            |
| Python (pip)                         | bandit                          |
| Python                               | Semgrep                         |
| React                                | ESLint react plugin, Semgrep    |
| Ruby                                 | brakeman                        |
| Ruby on Rails                        | brakeman                        |
| Scala (Ant, Gradle, Maven, and SBT)  | SpotBugs + find-sec-bugs        |
| Swift (iOS)                          | MobSF (beta)                    |
| TypeScript                           | ESLint security plugin, Semgrep |

A tool can also produce false negatives (the program contains errors that the tool does not report)
or false positives (the tool reports errors that the program does not contain). False positives are
a problem because of the time it may take for the developer to understand that there is no error
after all, but false negatives are much more dangerous because they lead to a false sense of
security. A good static analysis tool is one that, although it sometimes shows a false positive,
never misses a false negative.

## Conclusions

* Static analysis examines program code and reasons over all possible behaviors that might arise at
  run time.
* Tools based on static analysis can be used to find defects in programs.
* Every day new tools are developed and existing tools are improved, offering customers an
  increasingly higher quality service by building confidence in the static analysis results and
  enabling them to avoid certain code defects and improve their software solution.
* Static code analysis tools look for a specific set of patterns or rules in the source code, much
  in the same way that antivirus programs detect viruses.
* Static analysis tools are used to generate reports and to point out certain deviations from the
  prescribed code quality standards. However, these tools do not allow automatic modifications to
  the source code. The decision to change the structure of previously written code rests with the
  software developers.

## References

* [Metrics and Models in Software Quality Engineering, 2nd Edition by Stephen H. Kan](https://www.pearson.com/us/higher-education/program/Kan-Metrics-and-Models-in-Software-Quality-Engineering-2nd-Edition/PGM134821.html)
* [Static Code Analysis: All You Need to Know [in 2022]](https://www.perfomatix.com/static-code-analysis/)
* [Static Code Analysis Overview](https://www.perforce.com/blog/sca/what-static-analysis)
* [Why You Should Care About Static Code Analysis](https://alexwking.medium.com/why-you-should-care-about-static-code-analysis-633fe1075fa0)
* [Static Code Analysis](https://medium.com/@felipedutratine/static-code-analysis-930247a56cae)