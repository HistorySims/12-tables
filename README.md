# The Sacred Mount

A single-file browser game about the plebeians' struggle in early Rome, from the
debt crisis of 495 BC to the second secession of 449 BC. It is written for students
in grades 7 to 9 and assumes they have never seen a movie about Rome.

**Play it:** open `index.html` in any browser. It needs no install, no server and no
network connection. If you serve the repo with GitHub Pages, that URL is the whole game.

## What it is

The game has four acts and one continuous state. Nothing resets between acts. The
demands you make on the hill in 494 BC decide what the Senate grants, and the wording
you fight for on the Twelve Tables in 450 BC decides what you can do in the Forum when
Appius Claudius claims Verginia.

| Act | | Who you are | What you decide |
|---|---|---|---|
| I | The Debt | Lucius Sicinius, plebeian soldier | A neighbor in chains, who joins you, and the oath on the Field of Mars |
| II | The Sacred Mount | Lucius Sicinius | Food for the camp, the families, **the demands**, how to answer Menenius's fable, the first tribunes |
| III | The Bronze | Gnaeus Sicinius, his grandson | The decemvirs' bargain, and **which tablets of the Twelve Tables to fight for** |
| IV | Verginia | Gnaeus Sicinius | The girl in the Forum, the second secession, and what to do with the Ten |

There are 11 endings. The game can end in any act: bloodshed, a hill that never fills,
running out of grain, or going home on the strength of a good story.

## The Twelve Tables, and why they're not the whole point

The Tables get one act and one mechanic. You can fight for the plebs' wording on only
a few of twelve real provisions: summons, debt chains, the interest cap, liberty
claims, patrons, capital trials, laws against one person, bribed judges, the marriage
ban, funeral limits, a father's power, and neighbors' acorns. The rest go up in the
Fathers' wording. Some of them come back in Act IV. Table VI decides whether a crowd
can point at the bronze when Verginia is seized. Table IX shapes the final trial.

The lesson the game is built around: *a law you can read is a law you can argue
about.* That holds even when the law is harsh.

## Reading the screen

- **Voices:** debtors, the ranks, traders, hearths (mothers, wives and children) and
  the Fathers, with how each currently feels about you.
- **Meters:** *With you* (how many would follow), *Grain* (days of food while camped
  out), *Their fear* (how badly the Senate needs you, which is your leverage), *Your
  name*, and *No blood* (100 means no Roman has killed a Roman). A red cell is a warning.
- **The strip:** the hill, the city and the enemy, drawn from live state. When the
  plebs walk out, the city empties and the enemy's fires creep closer. That is the
  argument of the whole game: the plebs' power was never the hill. It was the gap they
  left behind.

Dotted words open a plain-language definition. Shaded italic boxes are sensory
details: what the scene smells, sounds and feels like.

## History

Every choice card ends with **What really happened**. Those notes follow Livy (Books 2
and 3) and Dionysius, and they say where the story is legend, where the game invents
something (Titus, the grandson Gnaeus), and where it lets you do what the Romans did
not. Verginia surviving is one example. Each act ends with *the annals*, the act told
the way a Roman historian might have told it, built from your choices, plus a ledger
of what each decision did to the meters. The final screen gives a timeline of what came
next (445, 367, 326 and 287 BC) and an **Export the whole record** button that copies
or downloads the run as plain text for a notebook or a teacher.

A content note for teachers: Act IV tells Livy's story of Verginia, including her
father's choice. It happens off-screen, in a few plain sentences, with no graphic detail.

## Accessibility

You can play it entirely by keyboard. Tab moves, and Enter or Space chooses, including
on the demand list, the tablets and the glossary. Focus is visible. All motion stops
under `prefers-reduced-motion`. It works from 320px wide.

## Editing it

Everything is in `index.html`. Beats live in one `BEATS` array tagged `act:1` to
`act:4`. Shared state is one `S` object, with a comment that says which act uses which
field. Beat text can ask about a flag with `{{FLAG?yes|no}}`, and `~~text~~` marks a
sensory aside. The demands are in `TERMS`, the tablets are in `TABLETS`, and the
endings are in `ENDINGS` and `finalEnding()`.
