[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/NK_8GSMb)
# Project-4-Brevets

Reimplement the RUSA ACP control time calculator with flask
and ajax.

## Objectives:

* Understand written specifications and convert them to
  a working code.
* Write unit tests to ensure the integrity of the
  written code.

## Dependencies:

* Designed for Unix, mostly interoperable on Linux or macOS.
  May also work on Windows, but no promises. A Linux
  virtual machine may work. You may want to test on shared
  server (if available).
* You must install [docker](https://www.docker.com/products/docker-desktop/).

## What is ACP Control Times?

Controls are points where a rider must obtain proof of passage,
and control<u>e</u> times are the minimum and maximum times by
which the rider must arrive at the location.   

The algorithm for calculating control times is described
here (https://rusa.org/pages/acp-brevet-control-times-calculator).
Additional background information is given here
(https://rusa.org/pages/rulesForRiders). The description is
ambiguous, but the examples help. Part of finishing this project
is clarifying anything that is not clear about the requirements,
and documenting it clearly.  

We are essentially replacing the calculator here
(https://rusa.org/octime_acp.html). We can also use that
calculator to clarify requirements and develop test data.

## Instructions:

* The RUSA control time calculator is a Perl script that takes an
HTML form and emits a text page in the above link. 
* The implementation that you will do will fill in times as the
  input fields are filled using Ajax and Flask. Currently, the
  km to miles (and vice versa) is implemented with Ajax.
* Each time a distance is filled in, the corresponding open
  and close times should be filled in using Ajax. We implement
  most of this functionality for you. All you need to do is to
  link front-end to the back-end correctly. These are the
  `brevets.html` and `flask_brevets.py` files.
* You'll also implement the logic in `acp_times.py` based on the
  algorithm given in the documentation. We will leave much of
  the design to you. All we ask for is that you keep the functions
  signatures as they are. Any change to the signature will cause
  our grader to fail immediately.
* You are required to write some nose test cases test you code.
  To see some example, check project-3 test cases. Also check
  [nose testing documentation](https://nose.readthedocs.io/en/latest/testing.html)
  for more information. More on testing below. 

## Testing

A suite of nose test cases is a requirement of this project.
Design the test cases based on an interpretation of rules
described in the
[RUSA website shared before](https://rusa.org/pages/acp-brevet-control-times-calculator).

Be sure to test your test cases:
* You can use the [current brevet time calculator](https://rusa.org/octime_acp.html)
  to check that your expected test outputs are correct.
* While checking these values once is a manual operation,
  re-running your test cases should be automated in the usual
  manner as a Nose test suite. 
* We should be able to run your test suite by changing to the
  "brevets" directory and typing `nosetests`. All tests should
  pass. Therfroe, it is recommended to put the test cases under
  a new directory named `brevets/tests`.
* You should have at least 5 test cases, and more
  importantly, your test cases should be chosen to distinguish
  between an implementation that correctly interprets the ACP
  rules and one that does not.

## Grading Rubric

* **[50 Points]** For passing our test cases (not given) that
  exercise your implementation of the `acp_times.py`. We will 
  write our test cases based on the requirements described on the
  given documentation links.
* **[30 Points]** For writing at least 5 **distinguishable** test 
  cases that exercise your code (6 points each).
* **[20 Points]** For a working docker container!

## Bonus Points

* **[30 Points]** For improving the front functionality to validate
  and communicate the typing of any invalid inputs. You decide what
  is invalid based on the documentation, and you decide how you will
  help the user understand what they did wrong, so they can correct
  their inputs.   
