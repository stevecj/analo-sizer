# Analo-sizer (analog-style synthesizer)

A self-contained analog-style synthesizer that runs within a Web browser.

## Usage

Open your compatible Web browser and navigate to
http://stevecj.github.io/browser-based-apps/analo-sizer/analosizer.html .
Play notes by clicking the keys on the piano keyboard image or by
pressing the corresponding keys on your computer keyboard.

Note that you can play chords using the computer keyboard, subject to
the limitations of your keyboard's ability to distinguish combinations
of simultaneously held keys.

## Known issues and limitations

1. Has very few controls so far.  Does not yet have filtering or provide
   volume envelope control,etc.
2. Is not known to be working properly on any mobile Web browser and visual
   layout is poor on mobile Web browsers.
4. Does not yet attempt to respond to touch events, so does not play chords
   using multi-touch.
5. Text keys don't play notes in Safari or Firefox when the focus is on
   a waveform radio button.
6. There is sometimes a click at the beginning of the playing of a note in
   Firefox as if maybe the attack fade-in starts before the note starts
   playing.

## Contributing

1. Fork it ( https://github.com/<my-github-username>/analo-sizer#fork-destination-box )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Making a Build

Note that the build process requires a `bash`-like environment (generally
the default on Unix, Linux, BSD, OS X, etc.) not a Windows environment.
It should be trivial, however, to modify the script entries in package.son
to work with Windows if you want to run a build on Windows.

### Have node.js and npm Installed

You'll need to use npm to run the build process, so install node.js and
npm if those are not already installed on your system.

See https://nodejs.org and
https://docs.npmjs.com/getting-started/installing-node

### Clone the repository from github

Change to the directory in which you'll want to have the analo-sizer
project directory created, and then clone the analo-sizer repository
from GitHub.

    git clone https://github.com/your-user-name/analo-sizer.git

### Install the build dependencies

Change to the newly created ./analo-sizer directory, and then update the
npm project.

    npm update

### Build the Analo-sizer Run-Time Files

    npm run build

### Open Analo-sizer In Your Browser

Open a compatible Web browser (a modern browser with WebAudio support) and
enter the file URL to the analosizer.html file in your build directory
(e.g. file:///Users/boss/Projects/analo-sizer/build/analosizer.html).

## Development

To list the development tasks, ...

    npm run

To have the project automatically rebuilt when you modify files in the
project's ./src directory, in its own terminal window or pane...

    npm run watch

This project uses the Ractive.js framework for tempating and UI data
binding.  See http://www.ractivejs.org/ for more info.

This project uses Browserify to build a single runnable javascript file
from a number of source module files and npm packages.  See
http://browserify.org/ for more info.

## Publishing A Release

The process of publishing a release is currently manual.

1. Edit the .src/analosizer.js file and update the version string.
2. Commit the change.
3. Tag the commit with the version number in the form of "v&lt;version>".
4. Push the changes to the upstream git repository.
5. Run the build process: `npm run build`.
6. Copy the files from the ./build directory to the location at which
   the files are to be hosted for public access.
