Check it WHILE you can (ciwyc - "sci-vic")
==========================================
ECS 289C Project: Different encodings for bounded model checking
------------------------------------------------------------------
This project defines a toy programming language (WHILE, see `src/while_parsing.py`)
and explores several techniques for symbolically representing its transition system
(i.e. its unrolled program graph).


Setup
-----
This project requires Python 3.12 and the pip packages in requirements.txt.  
You can install them using:
```bash
pip3 install -r requirements.txt
```
You can use [mise](https://github.com/jdx/mise) to install the right python version and create a
virtual environment automatically.

Utilities
---------
- `src/compare_encodings.py`: Create and display the SAT/SMT encoding of a WHILE program. Optionally save it in the SMTLIB2 format.
    - SAT encodings only support "+" and binary comparisons.
    - SMT encodings support most operators (see `smt.py`).
    - Both encodings only support single-letter lowercase variables. (This can be extended in `src/transition_relation.py`.)
- `src/transition_system.py`: Create and display a transition system that results from a direct unrolling of a WHILE program.
- `src/while_parsing.py`: Parse and run WHILE programs. Also includes an interactive shell mode.
- `while_programs`: Provides some example programs. Not all examples can be encoded in SAT/SMT.

For usage see:
```bash
python3 src/compare_encodings.py -h
python3 src/transition_system.py -h
python3 src/while_parsing.py -h
```

Tests
-----
Run `pytest` in the project root. Test coverage is currently limited.

[Report](docs/report.pdf) and [slides](docs/slides.pdf).

The LaTeX report sources are preserved in [docs/report-source](docs/report-source/), including the revised report in `final_revised.tex`.
