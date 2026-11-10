# Programmer De-Anonymization through Coding Style

A C++ source-code authorship project that builds programmer profiles from stylistic characteristics and uses them to attribute source files. Developed as Software Project Lab 1, it explores how repeated formatting and coding choices can become a computational signature.

## Feature analysis

The implementation separates style extraction into dedicated analyzers:

- Brace placement and brace-related patterns.
- Indentation characteristics.
- Empty-line and whitespace usage.
- Spacing around symbols.
- Function-signature characteristics.

`profiler.cpp` coordinates these analyzers, manages programmer profiles, and performs attribution. Supporting statistics and clustering modules provide the profile-comparison machinery.

## Console workflow

1. Load existing profiles from the supplied profile store.
2. Choose **Create profile** to process source associated with a programmer.
3. Choose **De-anonymize** to compare source characteristics against profiles.
4. Exit to write the resulting profile data.

## Build and run

Use a C++ compiler, or open `Project Source Codes/SPL1.cbp` in Code::Blocks. A command-line build can be run from the source directory:

```bash
cd "Project Source Codes"
g++ *.cpp -o /tmp/programmer-attribution
/tmp/programmer-attribution
```

Use the source directory as the working directory so profile files resolve as expected. The menu guides the interactive profiling and attribution steps.

## Research artifacts

The repository includes `profiles.csv`, `results.txt`, [report.pdf](report.pdf), a document version of the report, and project presentation slides. These artifacts accompany the implementation and explain the project's authorship-analysis context.

## Technical contributions

The project brings together source scanning, feature engineering, statistical profile representation, and interactive attribution. Its modular analyzers make individual stylistic signals inspectable while the profiler combines them into a programmer-level representation.
