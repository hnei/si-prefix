# si_prefix #

Functions for formatting numbers according to SI standards.

Example usage:

    from si_prefix import si_format

    print(si_format(.01331))
    # 13.31 m

    print(si_format(1331))
    # 1.33 k

    print(si_format(1331, format_str='{value:.1f} {prefix}')) # Reduce to 1 decimal place
    # 1.3 k

# Changelog #

 - **1.0:** use unicode strings and use µ (i.e., ``\N{MICRO SIGN}``) to denote
   micro (not u).
     - **Note: switching to unicode strings is an API-breaking change and may
       break code expecting a `str` return type.**
     - See [issue #4][i4] for more details.
 - **0.5:** change license to 3-clause BSD
 - **0.4.1:** add space before unit prefix
 - **0.4:** add Python 3 support, `si_parse` function
 - **0.2:** bug fixes
 - **0.1:** initial release

# Credits #

Written by Christian Fobel <christian@fobel.net>

Ported from [C version][1] written by Jukka “Yucca” Korpela
<jkorpela@cs.tut.fi>.

## Contributors ##

Python 3 support: [olehermanse][2]

License
-------
This project is licensed under the terms of the [BSD 3-clause license](/LICENSE.md)

[1]: http://www.cs.tut.fi/~jkorpela/c/eng.html
[2]: https://github.com/olehermanse
[i4]: https://github.com/cfobel/si-prefix/issues/4
