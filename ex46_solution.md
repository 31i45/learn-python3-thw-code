Since it's Python 3.11.4 now, the way to create virtual environment would no longer work and cuase error like "Atttribute not callable" 
something. Here you an follow the new method.

This link explain why it happens and how tofix it. https://forum.learncodethehardway.com/t/ex46-nosetests-error/5683

And I make an example of "Creating virtual environment". Enjoy your  Python hard way!



```
PS C:\Users\zheng> cd ~
PS C:\Users\zheng> python
Python 3.11.4 (tags/v3.11.4:d2340ef, Jun  7 2023, 05:45:37) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> quit()
PS C:\Users\zheng> pip list
Package                       Version
----------------------------- ---------
2to3                          1.0
alabaster                     0.7.13
Babel                         2.12.1
certifi                       2023.7.22
charset-normalizer            3.2.0
colorama                      0.4.6
coverage                      7.2.7
distlib                       0.3.7
docutils                      0.20.1
filelock                      3.12.2
idna                          3.4
imagesize                     1.4.1
iniconfig                     2.0.0
Jinja2                        3.1.2
MarkupSafe                    2.1.3
nose-py3                      1.6.2
numpy                         1.25.1
packaging                     23.1
pip                           23.2.1
platformdirs                  3.10.0
pluggy                        1.2.0
Pygments                      2.15.1
pytest                        7.4.0
requests                      2.31.0
six                           1.16.0
snowballstemmer               2.2.0
Sphinx                        7.1.1
sphinxcontrib-applehelp       1.0.4
sphinxcontrib-devhelp         1.0.2
sphinxcontrib-htmlhelp        2.0.1
sphinxcontrib-jsmath          1.0.1
sphinxcontrib-qthelp          1.0.3
sphinxcontrib-serializinghtml 1.1.5
urllib3                       2.0.4
virtualenv                    20.24.2
PS C:\Users\zheng> pip install virtualenv
Requirement already satisfied: virtualenv in c:\users\zheng\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (20.24.2)
Requirement already satisfied: distlib<1,>=0.3.7 in c:\users\zheng\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from virtualenv) (0.3.7)
Requirement already satisfied: filelock<4,>=3.12.2 in c:\users\zheng\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from virtualenv) (3.12.2)
Requirement already satisfied: platformdirs<4,>=3.9.1 in c:\users\zheng\appdata\local\packages\pythonsoftwarefoundation.python.3.11_qbz5n2kfra8p0\localcache\local-packages\python311\site-packages (from virtualenv) (3.10.0)
PS C:\Users\zheng>
PS C:\Users\zheng> python -m venv .\PycharmProjects\lphw\
PS C:\Users\zheng>
PS C:\Users\zheng> PycharmProjects\lphw\Scripts\activate.ps1
(lphw) PS C:\Users\zheng> pip list
Package    Version
---------- -------
nose       1.3.7
pip        23.2.1
setuptools 65.5.0
(lphw) PS C:\Users\zheng> pip uninstall nose
Found existing installation: nose 1.3.7
Uninstalling nose-1.3.7:
  Would remove:
    c:\users\zheng\pycharmprojects\lphw\lib\site-packages\nose-1.3.7.dist-info\*
    c:\users\zheng\pycharmprojects\lphw\lib\site-packages\nose\*
    c:\users\zheng\pycharmprojects\lphw\man\man1\nosetests.1
    c:\users\zheng\pycharmprojects\lphw\scripts\nosetests-3.4.exe
    c:\users\zheng\pycharmprojects\lphw\scripts\nosetests.exe
Proceed (Y/n)? y
  Successfully uninstalled nose-1.3.7
(lphw) PS C:\Users\zheng> pip install nose-py3
Collecting nose-py3
  Obtaining dependency information for nose-py3 from https://files.pythonhosted.org/packages/fe/85/f431f78a37e88d71edd3841c2dc94c8daba10d744949103f0bcbc26ad98f/nose_py3-1.6.2-py3-none-any.whl.metadata
  Using cached nose_py3-1.6.2-py3-none-any.whl.metadata (2.0 kB)
Collecting numpy (from nose-py3)
  Obtaining dependency information for numpy from https://files.pythonhosted.org/packages/2f/2a/34fe0b64e78347f4ea128868df0034a97e0f92b476f62947b0976caba820/numpy-1.25.1-cp311-cp311-win_amd64.whl.metadata
  Using cached numpy-1.25.1-cp311-cp311-win_amd64.whl.metadata (5.7 kB)
Collecting coverage (from nose-py3)
  Obtaining dependency information for coverage from https://files.pythonhosted.org/packages/b1/96/c12ed0dfd4ec587f3739f53eb677b9007853fd486ccb0e7d5512a27bab2e/coverage-7.2.7-cp311-cp311-win_amd64.whl.metadata
  Using cached coverage-7.2.7-cp311-cp311-win_amd64.whl.metadata (9.9 kB)
Collecting six (from nose-py3)
  Using cached six-1.16.0-py2.py3-none-any.whl (11 kB)
Collecting sphinx (from nose-py3)
  Obtaining dependency information for sphinx from https://files.pythonhosted.org/packages/c7/64/c3d5a265ebc2e96a6d1c1b3f5d23abdd3dde547d8638a4d06383aa8d2059/sphinx-7.1.1-py3-none-any.whl.metadata
  Using cached sphinx-7.1.1-py3-none-any.whl.metadata (5.8 kB)
Collecting 2to3 (from nose-py3)
  Using cached 2to3-1.0-py3-none-any.whl (1.7 kB)
Collecting sphinxcontrib-applehelp (from sphinx->nose-py3)
  Using cached sphinxcontrib_applehelp-1.0.4-py3-none-any.whl (120 kB)
Collecting sphinxcontrib-devhelp (from sphinx->nose-py3)
  Using cached sphinxcontrib_devhelp-1.0.2-py2.py3-none-any.whl (84 kB)
Collecting sphinxcontrib-jsmath (from sphinx->nose-py3)
  Using cached sphinxcontrib_jsmath-1.0.1-py2.py3-none-any.whl (5.1 kB)
Collecting sphinxcontrib-htmlhelp>=2.0.0 (from sphinx->nose-py3)
  Using cached sphinxcontrib_htmlhelp-2.0.1-py3-none-any.whl (99 kB)
Collecting sphinxcontrib-serializinghtml>=1.1.5 (from sphinx->nose-py3)
  Using cached sphinxcontrib_serializinghtml-1.1.5-py2.py3-none-any.whl (94 kB)
Collecting sphinxcontrib-qthelp (from sphinx->nose-py3)
  Using cached sphinxcontrib_qthelp-1.0.3-py2.py3-none-any.whl (90 kB)
Collecting Jinja2>=3.0 (from sphinx->nose-py3)
  Using cached Jinja2-3.1.2-py3-none-any.whl (133 kB)
Collecting Pygments>=2.13 (from sphinx->nose-py3)
  Using cached Pygments-2.15.1-py3-none-any.whl (1.1 MB)
Collecting docutils<0.21,>=0.18.1 (from sphinx->nose-py3)
  Obtaining dependency information for docutils<0.21,>=0.18.1 from https://files.pythonhosted.org/packages/26/87/f238c0670b94533ac0353a4e2a1a771a0cc73277b88bff23d3ae35a256c1/docutils-0.20.1-py3-none-any.whl.metadata
  Using cached docutils-0.20.1-py3-none-any.whl.metadata (2.8 kB)
Collecting snowballstemmer>=2.0 (from sphinx->nose-py3)
  Using cached snowballstemmer-2.2.0-py2.py3-none-any.whl (93 kB)
Collecting babel>=2.9 (from sphinx->nose-py3)
  Using cached Babel-2.12.1-py3-none-any.whl (10.1 MB)
Collecting alabaster<0.8,>=0.7 (from sphinx->nose-py3)
  Using cached alabaster-0.7.13-py3-none-any.whl (13 kB)
Collecting imagesize>=1.3 (from sphinx->nose-py3)
  Using cached imagesize-1.4.1-py2.py3-none-any.whl (8.8 kB)
Collecting requests>=2.25.0 (from sphinx->nose-py3)
  Obtaining dependency information for requests>=2.25.0 from https://files.pythonhosted.org/packages/70/8e/0e2d847013cb52cd35b38c009bb167a1a26b2ce6cd6965bf26b47bc0bf44/requests-2.31.0-py3-none-any.whl.metadata
  Using cached requests-2.31.0-py3-none-any.whl.metadata (4.6 kB)
Collecting packaging>=21.0 (from sphinx->nose-py3)
  Using cached packaging-23.1-py3-none-any.whl (48 kB)
Collecting colorama>=0.4.5 (from sphinx->nose-py3)
  Using cached colorama-0.4.6-py2.py3-none-any.whl (25 kB)
Collecting MarkupSafe>=2.0 (from Jinja2>=3.0->sphinx->nose-py3)
  Obtaining dependency information for MarkupSafe>=2.0 from https://files.pythonhosted.org/packages/be/bb/08b85bc194034efbf572e70c3951549c8eca0ada25363afc154386b5390a/MarkupSafe-2.1.3-cp311-cp311-win_amd64.whl.metadata
  Using cached MarkupSafe-2.1.3-cp311-cp311-win_amd64.whl.metadata (3.1 kB)
Collecting charset-normalizer<4,>=2 (from requests>=2.25.0->sphinx->nose-py3)
  Obtaining dependency information for charset-normalizer<4,>=2 from https://files.pythonhosted.org/packages/91/6e/db0e545302bf93b6dbbdc496dd192c7f8e8c3bb1584acba069256d8b51d4/charset_normalizer-3.2.0-cp311-cp311-win_amd64.whl.metadata
  Using cached charset_normalizer-3.2.0-cp311-cp311-win_amd64.whl.metadata (31 kB)
Collecting idna<4,>=2.5 (from requests>=2.25.0->sphinx->nose-py3)
  Using cached idna-3.4-py3-none-any.whl (61 kB)
Collecting urllib3<3,>=1.21.1 (from requests>=2.25.0->sphinx->nose-py3)
  Obtaining dependency information for urllib3<3,>=1.21.1 from https://files.pythonhosted.org/packages/9b/81/62fd61001fa4b9d0df6e31d47ff49cfa9de4af03adecf339c7bc30656b37/urllib3-2.0.4-py3-none-any.whl.metadata
  Using cached urllib3-2.0.4-py3-none-any.whl.metadata (6.6 kB)
Collecting certifi>=2017.4.17 (from requests>=2.25.0->sphinx->nose-py3)
  Obtaining dependency information for certifi>=2017.4.17 from https://files.pythonhosted.org/packages/4c/dd/2234eab22353ffc7d94e8d13177aaa050113286e93e7b40eae01fbf7c3d9/certifi-2023.7.22-py3-none-any.whl.metadata
  Using cached certifi-2023.7.22-py3-none-any.whl.metadata (2.2 kB)
Using cached nose_py3-1.6.2-py3-none-any.whl (160 kB)
Using cached coverage-7.2.7-cp311-cp311-win_amd64.whl (204 kB)
Using cached numpy-1.25.1-cp311-cp311-win_amd64.whl (15.0 MB)
Using cached sphinx-7.1.1-py3-none-any.whl (3.2 MB)
Using cached docutils-0.20.1-py3-none-any.whl (572 kB)
Using cached requests-2.31.0-py3-none-any.whl (62 kB)
Using cached certifi-2023.7.22-py3-none-any.whl (158 kB)
Using cached charset_normalizer-3.2.0-cp311-cp311-win_amd64.whl (96 kB)
Using cached MarkupSafe-2.1.3-cp311-cp311-win_amd64.whl (17 kB)
Using cached urllib3-2.0.4-py3-none-any.whl (123 kB)
Installing collected packages: snowballstemmer, 2to3, urllib3, sphinxcontrib-serializinghtml, sphinxcontrib-qthelp, sphinxcontrib-jsmath, sphinxcontrib-htmlhelp, sphinxcontrib-devhelp, sphinxcontrib-applehelp, six, Pygments, packaging, numpy, MarkupSafe, imagesize, idna, docutils, coverage, colorama, charset-normalizer, certifi, babel, alabaster, requests, Jinja2, sphinx, nose-py3
Successfully installed 2to3-1.0 Jinja2-3.1.2 MarkupSafe-2.1.3 Pygments-2.15.1 alabaster-0.7.13 babel-2.12.1 certifi-2023.7.22 charset-normalizer-3.2.0 colorama-0.4.6 coverage-7.2.7 docutils-0.20.1 idna-3.4 imagesize-1.4.1 nose-py3-1.6.2 numpy-1.25.1 packaging-23.1 requests-2.31.0 six-1.16.0 snowballstemmer-2.2.0 sphinx-7.1.1 sphinxcontrib-applehelp-1.0.4 sphinxcontrib-devhelp-1.0.2 sphinxcontrib-htmlhelp-2.0.1 sphinxcontrib-jsmath-1.0.1 sphinxcontrib-qthelp-1.0.3 sphinxcontrib-serializinghtml-1.1.5 urllib3-2.0.4
(lphw) PS C:\Users\zheng> pip list
Package                       Version
----------------------------- ---------
2to3                          1.0
alabaster                     0.7.13
Babel                         2.12.1
certifi                       2023.7.22
charset-normalizer            3.2.0
colorama                      0.4.6
coverage                      7.2.7
docutils                      0.20.1
idna                          3.4
imagesize                     1.4.1
Jinja2                        3.1.2
MarkupSafe                    2.1.3
nose-py3                      1.6.2
numpy                         1.25.1
packaging                     23.1
pip                           23.2.1
Pygments                      2.15.1
requests                      2.31.0
setuptools                    65.5.0
six                           1.16.0
snowballstemmer               2.2.0
Sphinx                        7.1.1
sphinxcontrib-applehelp       1.0.4
sphinxcontrib-devhelp         1.0.2
sphinxcontrib-htmlhelp        2.0.1
sphinxcontrib-jsmath          1.0.1
sphinxcontrib-qthelp          1.0.3
sphinxcontrib-serializinghtml 1.1.5
urllib3                       2.0.4
(lphw) PS C:\Users\zheng> pip install pytest
Collecting pytest
  Obtaining dependency information for pytest from https://files.pythonhosted.org/packages/33/b2/741130cbcf2bbfa852ed95a60dc311c9e232c7ed25bac3d9b8880a8df4ae/pytest-7.4.0-py3-none-any.whl.metadata
  Using cached pytest-7.4.0-py3-none-any.whl.metadata (8.0 kB)
Collecting iniconfig (from pytest)
  Using cached iniconfig-2.0.0-py3-none-any.whl (5.9 kB)
Requirement already satisfied: packaging in c:\users\zheng\pycharmprojects\lphw\lib\site-packages (from pytest) (23.1)
Collecting pluggy<2.0,>=0.12 (from pytest)
  Obtaining dependency information for pluggy<2.0,>=0.12 from https://files.pythonhosted.org/packages/51/32/4a79112b8b87b21450b066e102d6608907f4c885ed7b04c3fdb085d4d6ae/pluggy-1.2.0-py3-none-any.whl.metadata
  Using cached pluggy-1.2.0-py3-none-any.whl.metadata (4.4 kB)
Requirement already satisfied: colorama in c:\users\zheng\pycharmprojects\lphw\lib\site-packages (from pytest) (0.4.6)
Using cached pytest-7.4.0-py3-none-any.whl (323 kB)
Using cached pluggy-1.2.0-py3-none-any.whl (17 kB)
Installing collected packages: pluggy, iniconfig, pytest
Successfully installed iniconfig-2.0.0 pluggy-1.2.0 pytest-7.4.0
(lphw) PS C:\Users\zheng> ls


    目录: C:\Users\zheng


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2023/7/18     12:05                .fleet
d-----         2023/7/27     19:54                .idlerc
d-----         2023/7/16     13:19                .vscode
d-r---          2023/7/4     14:35                3D Objects
d-----          2023/7/6      9:22                Apple
d-r---          2023/7/5     16:39                Contacts
d-r---         2023/7/25     11:38                Desktop
d-r---          2023/7/6     11:11                Documents
d-r---         2023/7/30     17:38                Downloads
d-r---          2023/7/5     16:39                Favorites
d-r---          2023/7/5     16:39                Links
d-r---          2023/7/6      8:15                Music
dar--l         2023/7/10     19:46                OneDrive
dar--l         2023/7/10     20:02                OneDrive - MSFT
d-r---         2023/7/10     16:19                Pictures
d-----         2023/7/31     11:05                PycharmProjects
d-r---          2023/7/5     16:39                Saved Games
d-r---          2023/7/5     16:39                Searches
d-r---          2023/7/5     17:49                Videos


(lphw) PS C:\Users\zheng> cd .\PycharmProjects\lphw\skeleton\
(lphw) PS C:\Users\zheng\PycharmProjects\lphw\skeleton> ls


    目录: C:\Users\zheng\PycharmProjects\lphw\skeleton


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2023/7/30     21:50                bin
d-----         2023/7/30     21:50                docs
d-----         2023/7/31     21:05                NAME
d-----         2023/7/31     21:05                tests
-a----         2023/7/31     21:11           3472 ex46_ReadMe.txt
-a----         2023/7/30     21:05            439 setup.py


(lphw) PS C:\Users\zheng\PycharmProjects\lphw\skeleton> nosetests-3.11.exe

----------------------------------------------------------------------
Ran 0 tests in 0.016s

OK
(lphw) PS C:\Users\zheng\PycharmProjects\lphw\skeleton>
```


###### To solve this refrence to the discussion ######
https://forum.learncodethehardway.com/t/ex46-nosetests-ran-0-tests-or-ran-1-tests-with-error/3869/7
"I ran nosetests again, fail. Than i move Name_tests.py out of \tests, directly under \skeleton, this time nosetests succeed."
=======================================================

```
(lphw) PS C:\Users\zheng\PycharmProjects\lphw\skeleton> nosetests .\tests\NAME_tests.py
.
----------------------------------------------------------------------
Ran 1 test in 0.016s

OK
(lphw) PS C:\Users\zheng\PycharmProjects\lphw\skeleton> cd ..
(lphw) PS C:\Users\zheng\PycharmProjects\lphw> nosetests-3.11.exe .\simplegame\tests\game_tests.py
...
----------------------------------------------------------------------
Ran 3 tests in 0.000s

OK
(lphw) PS C:\Users\zheng\PycharmProjects\lphw>
```
