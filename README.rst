.. image:: https://raw.githubusercontent.com/bhagya-ct/molbery/master/molbery.png

A tool for designing Molecular beacons with 3' overhang.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
`Molbery`_ is a python based tool which identifies 29mer probes with 7 bases in stem, 8 in loop and 7 overhang bases from a fasta sequence. This is based on the method developed by Zuo, Xiaolei, et al. [Ref1]_ which is based on Exo III aided target recycling method for nucleic acid signature amplification. It uses the formula suggested by Howley, Peter M., et al. [Ref2]_ for calculation of melting temperature of the probes. Other than general criteria like GC content & Tm, there are special considerations in the property of the probe sequence which are reported to be optimal.

Features
~~~~~~~~
The latest release includes:

    supports Fasta & multi-Fasta format

    BLAST connect with parallel execution

    Optional GC content & Tm range

    reStructuredText Output

Sample Output
~~~~~~~~~~~~~

Sequence ID - gid

+---------+-------------------------------+----------+----------+---------------+---------------+
|   Probe | Probes (29mers)               |   GC (%) |   Tm (C) |   Stem Tm (C) |   Loop Tm (C) |
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

Authors and Contributors
~~~~~~~~~~~~~~~~~~~~~~~~

 The tool is designed and developed by Bhagya C T, Scientist-Biotechnology, Omix  Research & Diagnostics Labs and Manu S, Institute of Bioinformatics & Applied Biotechnology. The authors are grateful to Dr. Sudeshna Adak, CEO & Director, Omix Research & Diagnostics Labs for providing important technical supervision and discussions.

Source code
~~~~~~~~~~~

 The source codes of Molbery are available via git
 https://github.com/bhagya-ct/molbery

Compatibility
-------------
 We support both Linux and Windows platforms with the latest major releases of python 2 & 3.

License
-------

 Molbery is an open source tool available under the MIT license.

 Copyright (c) 2016 Bhagya C T
 
 Copyright (c) 2016 Manu S

 Please read the license content `here`_.

Installation
------------

 All the Python packages required for Molbery will be installed with pip.

 ::

    $ pip install molbery
    
 You can manually download the Molbery repository or simply clone it.

 ::

    $ git clone https://github.com/bhagya-ct/molbery

Credits
-------

Thanks to the Pythonistas for some wonderful plugin modules and libraries which saves a lot of Caffeine and Code!

  * `joblib`_
  * `argparse`_
  * `tabulate`_
  * `regex`_
  * `biopython`_

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
.. _here: https://github.com/bhagya-ct/molbery/blob/master/LICENSE
.. _page: https://github.com/bhagya-ct/molbery/issues
.. _joblib: https://pypi.python.org/pypi/joblib
.. _argparse: https://pypi.python.org/pypi/argparse
.. _tabulate: https://pypi.python.org/pypi/tabulate
.. _regex: https://pypi.python.org/pypi/regex
.. _biopython: https://pypi.python.org/pypi/biopython
