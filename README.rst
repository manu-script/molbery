.. image:: https://raw.githubusercontent.com/bhagya-ct/molbery/master/molbery.png

MOLecular Beacons powered by ExonucleaseIII RecYcling.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
`Molbery`_ is a python based tool which identifies 29mer probes with 7 bases in stem, 8 in loop and 7 overhang bases from a fasta sequence. This is based on the method developed by Zuo, Xiaolei, et al. [Ref1]_ which descibes an Exo III aided target recycling method for nucleic acid signature amplification. It uses the formula suggested by Howley, Peter M., et al. [Ref2]_ for calculation of melting temperature of the probes. Other than general criteria like GC content & Tm, there are special considerations in the property of the probe sequence which are reported to be optimal.

Features
--------
The latest release includes:

    Support for Fasta & multi-Fasta format

    Manual specification of GC content, Tm range & Salt Conc.

    reStructuredText Output

    BLAST connect with parallel execution


Compatibility
-------------
 Molbery is a cross platform tool which runs on Windows, Linux and OS X with the latest & major releases of python 2 & 3.

License
-------

 Molbery is an open source tool available under the OSI approved MIT license.

 Copyright (c) 2016 Bhagya C T

 Copyright (c) 2016 Manu S

 Please read the license content `here`_.

Installation
------------

 All the Python packages required for Molbery will be installed with `pip`_.

 Run cmd with Administrator permissions in Windows.
 ::

    > pip install molbery

 Run command with sudo permissions in Linux and OS X.
 ::

    $ sudo pip install molbery


 You can manually download the Molbery repository or simply clone it.

 ::

    $ git clone https://github.com/bhagya-ct/molbery

Usage
-----
 After succesful installation refer command help for all available options.
 ::

    $ molbery --help

 For a single FASTA input run
 ::

    $ molbery <path_to_fasta> --blast --out <output> -g <GC_min> -c <GC_max> -t <Tm_min> -m <Tm_max> -s <salt_conc_in_molar_units>

 For a multi-FASTA input run (Output cannot be specified for multiple seq. Default is sequence ID present in multi-FASTA)
 ::

    $ molbery <path_to_fasta> --blast --multi -g <GC_min> -c <GC_max> -t <Tm_min> -m <Tm_max> -s <salt_conc_in_molar_units>

Sample Output
-------------

 Sequence ID - <gid_of_sequence>

+---------+-------------------------------+----------+----------+---------------+---------------+
|   Probe | Molberys (29mer Probes)       |   GC (%) |   Tm (C) |   Stem Tm (C) |   Loop Tm (C) |
+=========+===============================+==========+==========+===============+===============+
|       1 | ACCGTAGAGCTACGACTACGGTACATTAC |    48.28 |     69.9 |            22 |            24 |
+---------+-------------------------------+----------+----------+---------------+---------------+
|       2 | AGTCGTATGCATACGTACGACTAAGCTAC |    44.83 |     68.9 |            20 |            24 |
+---------+-------------------------------+----------+----------+---------------+---------------+
|       3 | ACTTTTCGTGCTGAAGAAAAGTGAAAGCG |    41.38 |     66.9 |            18 |            24 |
+---------+-------------------------------+----------+----------+---------------+---------------+
|       4 | AGCTTAGACGTACGACTAAGCTACGACTA |    44.83 |     68.9 |            20 |            24 |
+---------+-------------------------------+----------+----------+---------------+---------------+
|       5 | AGATTCGAAGCGAACCGAATCTGCATACG |    48.28 |     69.9 |            20 |            24 |
+---------+-------------------------------+----------+----------+---------------+---------------+

Note: Blast Outputs are written to <Output>_blast_results/ folder with individual text file for every probe.

Authors and Contributors
------------------------

 The tool is designed and developed by Bhagya C T, Scientist-Biotechnology, Omix  Research & Diagnostics Labs and Manu S, Institute of Bioinformatics & Applied Biotechnology. The authors are grateful to Dr. Sudeshna Adak, CEO & Director, Omix Research & Diagnostics Labs for providing important technical supervision and discussions.

Source code
-----------

 The source codes of Molbery are available

 via git: https://github.com/bhagya-ct/molbery

 via Pypi: https://pypi.python.org/pypi/molbery



Credits
-------

Thanks to the Pythonistas for some wonderful plugin modules and libraries which saves a lot of Caffeine and Code!

  * `joblib`_
  * `argparse`_
  * `tabulate`_
  * `regex`_
  * `biopython`_

FAQs
----
 Q1) pip command not found?

  Ans. You probably don't have the latest release of Python. Update Python or install `pip`_.

 Q2) Installation was successful but could not find molbery command?

  Ans. You would not have given Admin or sudo permissions while installing. Run $ pip uninstall molbery and reinstall with Admin or sudo permissions.

Bugs
----

If you find a bug in molbery (pypi), please try to reproduce it with latest python 2.7 and 3.5.

If the problem persists, please file a bug in the github issue tracking system in the repository `page`_.
For questions, troubleshooting and requests, please feel free to contact us at bhagyathimmappa@gmail.com or smanu@ibab.ac.in

References
----------
.. _Molbery: https://github.com/bhagya-ct/molbery
.. [Ref1] Zuo, X., Xia, F., Xiao, Y., & Plaxco, K. W. (2010). Sensitive and selective amplified fluorescence DNA detection based on exonuclease III-aided target recycling. Journal of the American Chemical Society, 132(6), 1816-1818.
.. [Ref2] Howley, P. M., Israel, M. A., Law, M. F., & Martin, M. A. (1979). A rapid method for detecting and mapping homology between heterologous DNAs. Evaluation of polyomavirus genomes. Journal of Biological Chemistry, 254(11), 4876-4883.
.. _here: https://opensource.org/licenses/MIT
.. _page: https://github.com/bhagya-ct/molbery/issues
.. _pip: https://pypi.python.org/pypi/pip
.. _joblib: https://pypi.python.org/pypi/joblib
.. _argparse: https://pypi.python.org/pypi/argparse
.. _tabulate: https://pypi.python.org/pypi/tabulate
.. _regex: https://pypi.python.org/pypi/regex
.. _biopython: https://pypi.python.org/pypi/biopython
