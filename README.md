<!---

TASK LIST:

  * Use cp -rf *.* to copy all of the files and directories in this repository
    to the starter repository for this assignment
  * Change into the directory for the starer repository
  * Update the header (e.g., #) to only give the name of the assignment
  * Update the first paragraph to include the commented-out content
  * Change the link in the # Problems section to point to this lab's starter
  * Create the assignment in the GitHub Classroom, noting the URL
  * Test the assignment by accepting it with your own GitHub account
  * Check to ensure that your GitHub repository is created correctly
  * Share the assignment link with all of the students using email or Slack

PROBLEMS?

  * Contact Gregory M. Kapfhammer by email or Slack
  * Raise an issue in the GitHub repository for this assignment

-->

# cs600-F2017-project1

This repository contains the starter for project one in Computer Science 600
Fall 2017. The main directory of this repository contains the LaTeX source code
for a project that is designed for use with [GitHub
Classroom](https://classroom.github.com/). To learn more about the course in
which these assignments were completed, please visit the [Computer Science 600
Fall 2017 GitHub
Organization](https://github.com/Allegheny-Computer-Science-600-F2017).

The LaTeX file in this repository is automatically compiled with [Travis
CI](https://travis-ci.org/), thus ensuring that it compiles correctly and,
moreover, that a PDF of the project proposal is available in your GitHub
repository whenever a commit is tagged for a release. Additionally, you can use
a LaTeX compilation command like `pdflatex` or `latexmk` to compile the provided
LaTeX file on your local workstation.

<!---

 Since the Travis builds for this repository will initially fail (as evidenced by
 a red &#x2717; appearing in the commit logs instead of a green &#x2714;), the
 researcher is responsible for completing all of the steps needed to satisfy the
 requirements for the assignment, thus causing a &#x2714; to instead appear in
 the commit logs.

--->

## Introduction

This assignment requires a researcher to write a LaTeX document, stored in the
file `senior_thesis_description.tex`, that explains three key aspects of a
proposed senior thesis research project. First, you should state the tentative
title for your senior thesis. Second, you should write a one-paragraph abstract
that explains your proposed research. Third, you should include a bulleted list
that suggests a potential first and second reader for your thesis research.
Below the bulleted list you should justify your choice of readers with an
additional paragraph.

The researcher is also responsible for writing a one-paragraph reflection,
stored in the file `reflection.md`, that explains the challenges that you faced
and the solutions you developed when completing this project. This is a Markdown
file that must adhere to the standards described in the [Markdown Syntax
Guide](https://guides.github.com/features/mastering-markdown/). Remember, you
can preview the contents of a comitted Markdown file by clicking on the name of
the file in your GitHub repository.

If both your LaTeX source code and your writing meet all of the established
requirements, then you will see a green &#x2714; in the listing of commits in
GitHub. If your submission does not meet the requirements, a red &#x2717; will
appear instead. Your course  instructor will reduce a researcher's grade for
this assignment if the red &#x2717; appears on the last commit in GitHub
immediately before the assignment's due date on September 7, 2017 at 9:00 a.m..

Yet, if the green &#x2714; appears on the last commit in your GitHub
repository, then you satisfied all of the main checks, thereby allowing the
course instructors to further evaluate other aspects of your LaTeX source code
and writing, as further described in the remainder of this assignment sheet.
Unless you provide the course instructors with documentation of the extenuating
circumstances that you are facing, no late work will be considered towards your
grade for this project.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub. You will partially
complete this authorization by following intuitive steps in your web browser.
You will also need to type the command `travis login --pro` in your terminal
window when you are in the root of your GitHub repository.

## Security

In order for Travis to automatically upload a PDF, called
`senior_thesis_description.pdf`, to GitHub when you tag the commit, you need to
created your encrypted access token. To complete this task you must type the
command `travis setup releases --force` in your GitHub repository for this
assignment. Then, when prompted, please type your username and password for
GitHub. When asked to give the filename, you can type
`_build/senior_thesis_description.pdf`. When asked if you want to deploy from a
specific repository, you can respond with the answer of "no". Finally, when
this tool asks if you want to use encryption, please answer with a "yes".

Now, you should have a `.travis.yml` file with a secure access token for your
GitHub repository for this assignment. Use a text editor to edit this file and
place the following lines of code at the bottom of it. Finally, you should ask
Professor Kapfhammer to enable Travis-based continuous integration for your
GitHub repository. Now, you are ready to perform a commit with tags and see your
PDF uploaded to GitHub!

```
  skip_cleanup: true
  on:
    tags: true
```

## Tagging

Since this repository primarily contains LaTeX source code, the Travis CI
configuration for it will compile the source code and automatically release a
PDF of the main file whenever the last commit is associated with a [Git
Tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging). As such, this will
cause a PDF file to become available in the listing of the "Releases" listing
for this repository. All release numbers for your writing in this repository
should adhere to the [Semantic Versioning](http://semver.org/) standard that
all GitHub projects are asked to adopt.

Please note that the faculty members who read the PDF that is generated from the
LaTeX source code will only do so by downloading the "tagged" release of the
file `senior_thesis_description.pdf` that has a version number greater than
1.0.0. That is, if your commit is tagged with
`senior_thesis_description-gkapfham-1.0.0`, then the file
`senior_thesis_description.pdf` should be available for download in the
"Releases" tab in your GitHub repository for this project under the name
`senior_thesis_description-gkapfham-1.0.0`.

Once you have finished making a single small change to the
`senior_thesis_description.tex`, you should commit your file using a `git
commit` command. Now, to create your first tag for this repository you could
type `git tag senior_thesis_description-gkapfham-0.1.0`. Of course, you should
substitute your user name for `gkapfham` when you create the tag. At this point,
you are ready to push your changes with the appropriate tag by typing the
command `git push -u origin master --tags`. After waiting for a period of time,
you should see that your GitHub repository features a new release of the
document that you must create for this project.

When you make subsequent changes to your files and perform commits and you are
ready to release a new version of `senior_thesis_description.pdf`, then you
should again tag your work &mdash; before running a push &mdash; with a tag that
adheres to the [Semantic Versioning](http://semver.org/) standard. Each time
that you correctly execute this sequence of commands you will release a new
version of your document to GitHub that is easily accessible as a PDF to you and
to your first and second readers.

## Updates

If a course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-600-F2017/cs600-F2017-lab1-starter.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever a course instructor needs to provide you
with new source code for this assignment. However, please note that, if you have
edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 600 Project 1
Starter](https://github.com/Allegheny-Computer-Science-600-F2017/cs600-F2017-project1-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. To ensure that your issue is properly resolved,
please provide as many details as is possible about the problem that you
experienced.

Please note that these assignment sheets have been developed and tested on an
Ubuntu 16.04 workstation running a recent version of LaTeX that was manually
installed using the TeXLive installer. It is also worth noting that you can
compile the `senior_thesis_description.tex` file using LaTeX development tools
such as `latexmk` or `pdflatex`. If you are unable to compile this file with
your development tools and your execution environment, then please open a new
issue and we will attempt to resolve your concerns.

Students who find, and use the appropriate GitHub issue tracker to correctly
document, a mistake in any aspect of this laboratory assignment will receive
free laptop stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with either the your first reader or [Professor
Kapfhammer](http://www.cs.allegheny.edu/sites/gkapfham/), as he is the
coordinator for this course. Alternatively, you may ask questions in the Slack
team for this course. Finally, you can schedule a meeting during your first
reader's office hours or, alternatively, during Professor Kapfhammer's office
hours. In particular, if you have questions about your research project, please
see your first reader. However, if you have questions about the use of either
Git or GitHub Classroom, then please talk with Professor Kapfhammer.
# mycs600repository
