# Translator

I. used modules
-------------------
PyQt5 (pip install pyQt5)
watson_developer_cloud ($ pip install --upgrade watson-developer-cloud)

II. File List
-------------------
controller.py                 Controlling all the tasks.
gui.py                        Painting the GUI and repainting and updating it with the results.
main.py                       Initializing the controller and starting the program
translation_watson.py         Translating the inputs using watson language translator API

III. Function
-------------------
The idea for my program is to show that one sentence can have
many different meaning when it is translated into other languages
and the back to the original language. It shows that machine
translation has to handle many issues and that the results
often vary.

What this program does is that it takes the sentence that was
put in by the user and translates it. For this translation it
uses the "watson speech translate" API. The language into the
input is going to be translated is chosen randomly. The number
of languages the text is translated into increases from one to
eleven. The number of iterations is also shown in the user
interface.


IV. Design
-------------------
I wanted to keep the Design as simple as possible so that the
focus is on the translation results. I used "Google Hot
Searches" as an inspiration for my user interface.
To minimize the latency for the user I decided that
the results should be displayed when they are done.


V. Expected Bottlenecks
-------------------
1. User interface
Because I never used PyQt5 for making user interfaces so it was
was hard to create the interface.



VI. Unexpected Bottlenecks
-------------------
1. Translation API

The biggest problem was to find a translation API that on the
one hand had enough languages so that my algorithm makes sense
and return interesting results. On the other hand the API had
to be free so that it can be used properly.

2. Time for translation

I did not expect that the API would need much time to give
back the results. That is not a big issue when the number of
iterations is not very high but when the number increases it
takes relatively long to give back a result.

3. Updating the interface

It was difficult to make the interface update the text because
I had to interrupt the algorithm.
