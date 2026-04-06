ReadSpeed
A minimal, single-file reading speed tester you can host on GitHub Pages — no build tools, no dependencies, no server required.
Features

4 reading passages across Science, History, Nature, and Psychology
Live timer that starts the moment you begin reading
Comprehension quiz after each passage to test retention, not just speed
Results breakdown with your WPM, time taken, and comprehension score
Speed comparison chart showing where you land vs. average adults, college students, and speed readers
Local history — your last 10 results are saved in the browser so you can track improvement over time
"Hide text" mode — blurs the passage until you're ready, so the timer only starts when you do

What counts as a good score?
SpeedLevelUnder 150 wpmBelow average200–250 wpmAverage adult250–350 wpmAbove average350–600 wpmSkilled / speed reader600+ wpmExceptional (check your comprehension!)
Hosting on GitHub Pages

Create a new GitHub repository
Upload index.html to the root of the repo
Go to Settings → Pages
Under Source, select the main branch and / (root) folder
Click Save — your app will be live at https://yourusername.github.io/your-repo-name within a minute or two

Running locally
No setup needed. Just open index.html directly in any modern browser:
open index.html
Or drag the file into a browser window.
Customising
All content lives in a single index.html file. To add or edit passages, find the PASSAGES array near the top of the <script> block. Each passage follows this structure:
js{
  id: 'unique-id',
  tag: 'Category',
  title: 'Passage Title',
  words: null,          // calculated automatically, leave as null
  text: `Your passage text here...`,
  questions: [
    {
      q: 'Your question?',
      options: ['Option A', 'Option B', 'Option C', 'Option D'],
      answer: 0         // index of the correct option (0-based)
    }
  ]
}
License
