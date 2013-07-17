This package is designed to be a simple demonstration of the
principles of matched filtering.  It uses the analogy of LIGO as a
microphone to explain the basic ideas, using a microphone attached to
the computer to study data as a function of time, noise sources, and
real signals, as well as headphones or a speaker to play back those
signals and others.  Examples are given where a signal is buried in
the noise and extracted using matched filtering.  Real LIGO data and
accurate gravitational waveforms are also included with this code, and
used for further examples to complete the analogy.  The concepts
introduced here can be applied far more widely in all areas of data
analysis.

Fourier transforms are introduced, starting with a simple example of a
pure tone (which can be played by the computer), and progressing to
Fourier transforms of noise and gravitational-wave signals.  The
matched filter is then introduced by progressively building the
formula with simple explanations for each term.  Discussion of these
concepts is interwoven with practice using them.

The material is presented as an ipython notebook -- which looks and
acts basically like Mathematica.  The notebook includes text
explaining the concepts and code.  This allows the explanations to be
included (with latex equations) right among the code, and all in a
live python session.  No familiarity with python is necessary for the
student, though the computer will need to be set up by someone with
good technical skills.

A second notebook is also included for more demonstrations of the
Fourier transform.  This notebook makes it easy to record a sound --
tuning forks, musical instruments, or whatever the student is curious
about -- and look at its Fourier transform.  This encourages the
student to play with the ideas a little, experimenting to gain
understanding.



To run the code
===============
If you are reading this README from the github project page, you
should first download the package to your own computer with something
like
```bash
git clone --depth 1 https://github.com/MOBle/MatchedFiltering.git
```
Otherwise, you are presumably reading this in the code itself.

You will need a reasonably current installation of python, along with
[ipython-notebook][1] and [pylab][2].  For full functionality, you
will also need the [pyaudio module][3].

First, go into the top directory of the code: `MatchedFiltering`.  In
it, there should be an executable file called `CreateSounds.py` which
will create a set of WAV files from real gravitational-waveform data.
These files will be needed later.  To create them, run
    python CreateSounds.py
This will run through a set of waveforms it creates.

Now, from that same directory, issue the command
    ipython notebook --pylab
This will start an ipython session, but should switch to your default
web browser, where you will interact with the session.  Next, click on
the file `MatchedFilteringDemonstration.ipynb`, and follow the
instructions in there.  You may need to change the path in the first
cell to the one you actually used.



Notes for classroom use
=======================
There are three reasonable ways to deliver this demonstration to
students: as a presentation, individually on the students' personal
computers, and together in a computer lab.

Most likely, the presentation option is the least useful to students.
Most students benefit enormously from being able to interact with the
notebook personally.  They will be more interested, able to read along
at their own pace, and play with the parameters.  If this is just not
possible, it would be best to go slowly and ask lots of questions of
the students, possibly allowing one student to actually run the
commands while the teacher engages from off to the side.

A more preferable option may be having the students download and run
the code themselves.  The only caveat here is that installation of
ipython, pylab, and pyaudio may be too much to ask of students, unless
they are expected to be very computer literate.  If the students are
capable, there are questions included in the notebook.  Their answers
could be turned in as a homework assignment, or a quiz given on the
material to ensure that students actually go through the notebook.

If this will be presented together in a computer lab, it is best if
things are set up as much as possible on each computer beforehand.
The computers need to be using different accounts (with different home
directories), or ipython will get screwed up and run into errors.

The steps to set up the computer are

0. install all necessary packages
1. get the audio (input and output) working
2. open a terminal
3. `git clone` the repository onto each computer
4. cd into `MatchedFiltering`
5. run `CreateSounds.py`
6. start the ipython session
7. select the demonstration notebook

Steps (0) and (1) in particular are absolutely crucial, and are
sufficiently complicated that these should probably be done well in
advance.  Depending on the computer skills of the students, and their
familiarity with your particular computers, they may be able to help
with steps (2) through (7).




[1]: http://ipython.org/ipython-doc/dev/interactive/htmlnotebook.html
[2]: http://www.scipy.org/PyLab
[3]: http://people.csail.mit.edu/hubert/pyaudio/