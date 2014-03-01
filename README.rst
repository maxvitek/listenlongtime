ListenLongTime
==============

ListenLongTime is a python module which uses PyAudio
to create a listening object which is capable of listening
for long periods of time.  When it hears a sound (hopefully
speech)above its configurable silence threshold, it captures
the audio until it hears some period of silence.  At this
point, it will transform the snippet into a flac format and
sends it to Google's undocumented web-to-speech api, and
finally it returns a dictionary containing Google's
transcription.

Usage:
------

.. code-block:: pycon

    >>>from llt import LongListener
    >>>lstr = LongListener(vis=True)
    >>>lstr.listen()
    ...

Contribute
----------

Please contribute!

Inspiration
-----------

This was inspired by a Gist that I found previously, but
now I can't find it to give credit.