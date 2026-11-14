Worked for 2m 6s

### The logarithmic structure of musical pitch — and what happens when we divide it

There is an interesting mathematical tension at the centre of Western tuning: the ear primarily organizes pitch by frequency ratios, while musical notation organizes those ratios into a finite grid of equally spaced pitch positions.

However, there is an important distinction to make first:

The conventional twelve-tone equal-tempered system does not divide an octave linearly in Hertz. It divides it linearly in logarithmic frequency, which means that adjacent notes have a constant frequency ratio.

That is mathematically elegant, computationally convenient, and musically extremely useful. But it creates compromises when we compare the resulting notes with the natural harmonic series.

Let's unpack the problem.

### 1\. Three different spaces for the same sound

Suppose we start with A4 = 440 Hz.

An octave above is 880 Hz. Another octave above is 1760 Hz.

The absolute frequency difference doubles each time:

| Interval | Frequency |
| -------- | --------- |
| A3       | 220 Hz    |
| A4       | 440 Hz    |
| A5       | 880 Hz    |
| A6       | 1760 Hz   |

Yet we perceive each octave as approximately the same musical distance.

This means that absolute frequency is not a good coordinate system for musical pitch.

We can use three different representations:

A. Linear frequency space

f=220,\\ 440,\\ 880,\\ 1760

B. Logarithmic pitch space

p=\\log_2(f/f_0)

The successive octaves are now equally distant: 0, 1, 2, 3.

C. Equal-tempered note space

We divide each octave into 12 equal logarithmic intervals:

p_n=\\frac{n}{12}

Consequently:

f_n=f_0\\,2^{n/12}

The semitone ratio is approximately 1.059463.

This is the geometric rather than arithmetic subdivision of frequency.

An arithmetic subdivision would produce:

f_n=f_0\\left(1+\\frac{n}{12}\\right)

That would place the midpoint of an octave at 660 Hz rather than approximately 622.25 Hz. It would not have the same musical relationship to the octave endpoints.

Frequency ratio versus subdivision position, from 0 to 12. The geometric curve represents equal-tempered semitones; the straight line represents equal-Hertz steps. Horizontal position is measured in subdivisions.

The logarithmic arrangement is therefore not an arbitrary musical convention. It corresponds to the way musical interval size is normally represented and perceived. There is also a biological connection: the cochlea and auditory system encode frequency tonotopically, with an approximately logarithmic organization over substantial parts of the hearing range. PubMed Central (PMC) +2

### 2\. The harmonic series does not follow the equal-tempered grid

This is where things become interesting.

A vibrating string or an ideal periodic oscillator produces a harmonic series:

f_n=n f_0

If the fundamental is 100 Hz, its harmonics are:

| Harmonic | Frequency | Musical relationship to fundamental |
| -------- | --------- | ----------------------------------- |
| 1        | 100 Hz    | Fundamental                         |
| 2        | 200 Hz    | Octave                              |
| 3        | 300 Hz    | Perfect fifth + octave              |
| 4        | 400 Hz    | Two octaves                         |
| 5        | 500 Hz    | Major third + two octaves           |
| 6        | 600 Hz    | Perfect fifth + two octaves         |
| 7        | 700 Hz    | Harmonic seventh                    |
| 8        | 800 Hz    | Three octaves                       |
| 9        | 900 Hz    | Major second + three octaves        |
| 10       | 1000 Hz   | Major third + three octaves         |

Notice something important.

The harmonic series is equally spaced in Hertz, but its intervals become progressively smaller in logarithmic pitch space.

The interval between successive harmonics is:

I_n=1200\\log_2\\left(\\frac{n+1}{n}\\right)

For example:

* Harmonics 1–2: 1200 cents.

* Harmonics 2–3: 702 cents.

* Harmonics 3–4: 498 cents.

* Harmonics 4–5: 386 cents.

* Harmonics 5–6: 316 cents.

* Harmonics 6–7: 267 cents.

This is a fundamental asymmetry between the physical production of harmonic sound and the construction of conventional scales.

The harmonic series does not contain twelve equally spaced pitch positions. Its intervals progressively contract.

![The Harmonic Series Infographic | LivePhysics™](https://images.openai.com/static-rsc-4/9vK2z8IlpV8T6da5qwc8dEbwMZlsjCgESCcXS8bZho3SGl0lh6WKl94lMIj9QwX5K5eXL8Z6q9xv1wG45MzA2OJEBvOEHGwGfNOE7gvuZ7fdSOFXERa40EyN6ofOSJ-hr-bkQa-U4dMreHRjuZdWpQJZ_FpuofsAEzmagjN6Ql7jrvDGas19bHfBO_9DjZWd?purpose=fullsize)

### The consequences for chords

Consider a major triad built on C.

Its ideal just-intonation frequency ratios are:

C:E:G=4:5:6

Normalizing to C:

1:\\frac54:\\frac32

This is not an arbitrary aesthetic convention. It creates particularly convenient alignments between the harmonics of the three notes.

For instance:

* The fifth harmonic of C coincides with the fourth harmonic of E.

* The third harmonic of C coincides with the second harmonic of G.

* The sixth harmonic of E coincides with the fifth harmonic of G.

These relationships produce a strongly integrated harmonic structure.

Now compare that with twelve-tone equal temperament:

C:E:G=
1:2^{4/12}:2^{7/12}

Or numerically:

| Note | Just intonation | 12-TET   |
| ---- | --------------- | -------- |
| C    | 1.000000        | 1.000000 |
| E    | 1.250000        | 1.259921 |
| G    | 1.500000        | 1.498307 |

The fifth is remarkably close to its just ratio. The major third is not.

The equal-tempered major third is 400 cents, whereas the just major third is approximately 386.31 cents.

That is a difference of almost 13.69 cents.

It means the relevant harmonics do not coincide exactly. Instead, they produce slight frequency separations, potentially perceived as beating, roughness or reduced harmonic fusion.

The same problem appears in other intervals. The equal-tempered minor third is 300 cents, compared with approximately 315.64 cents for the 6:5 just ratio.

This does not mean equal temperament sounds bad. It means its chords are compromises between different harmonic relationships.

There is a trade-off: we gain the ability to transpose music between keys without changing the tuning system, but lose some exact low-integer frequency relationships.

The distinction between harmonic fusion, roughness and learned musical consonance is important here. They are related, but not identical phenomena. PubMed Central (PMC) +2

### 3\. A deeper problem: harmonic numbers become increasingly crowded

Think about where the harmonics sit on a logarithmic pitch axis.

Their positions are:

p_n=\\log_2(n)

The distance between harmonic 1 and 2 is one octave.

The distance between 100 and 101 is only:

1200\\log_2(101/100)
\\approx17.23\\text{ cents}

So the higher we go in the harmonic series, the more densely packed the partials become in musical pitch space.

This has several consequences:

* A fixed musical grid cannot represent every harmonic relationship accurately.

* The higher harmonics of an individual note can fall between conventional note positions.

* The way a chord sounds depends partly on which of its harmonics are prominent, not merely on the fundamental frequencies.

* Different instruments can make the same nominal chord sound considerably different because their spectral envelopes emphasize different partials.

This is one reason why tuning a chord using only its fundamental frequencies is an incomplete model of its acoustical behaviour.

The auditory system also has finite frequency resolution. Some higher harmonics are resolved individually, whereas others fall within overlapping cochlear filters. PubMed Central (PMC) +1

### 4\. What happens if we subdivide the logarithmic octave differently?

Here is the interesting alternative: rather than assuming twelve divisions, retain the logarithmic geometry but change the number of divisions.

This gives us the family of N equal divisions of the octave, usually called N-EDO (or N-ET).

The general equation is:

\\boxed{f_n=f_0\\,2^{n/N}}

Each step has the same ratio:

r=2^{1/N}

And its size in cents is:

s=\\frac{1200}{N}

Nothing requires N to be 12.

We could use 19, 31, 53, 72, or other divisions.

### Some interesting alternatives

12-EDO — conventional tuning

### 100¢

12 divisions per octave

Good general-purpose compromise, but its major and minor thirds deviate considerably from simple harmonic ratios.

19-EDO — an alternative harmonic balance

### 63.16¢

19 divisions per octave

A five-step interval approximates the just minor third (6:5) to within 0.15 cents. It is particularly interesting for minor harmony.

31-EDO — improved major thirds

### 38.71¢

31 divisions per octave

Its ten-step major third is approximately 0.78 cents away from the 5:4 ratio. Its harmonic seventh is also particularly well approximated.

53-EDO — very precise fifths

### 22.64¢

53 divisions per octave

Its 31-step fifth is within approximately 0.07 cents of a pure 3:2. Its major third is within approximately 1.41 cents of 5:4.

72-EDO — fine-grained pitch geometry

### 16.67¢

72 divisions per octave

Six divisions per conventional semitone. Useful for exploring quarter-tone and finer inflections, as well as approximating a wide variety of intervals.

These systems are not simply different resolutions of the same keyboard. They can produce different harmonic languages and different possibilities for chord construction. Tuning +1

### Comparing the harmonic approximations

Here are the actual errors, in cents, when the nearest available step is used.

Positive means the tuned interval is wider than the pure ratio; negative means narrower.

| System | Major 3rd 5:4 | Minor 3rd 6:5 | Fifth 3:2 |
| ------ | ------------- | ------------- | --------- |
| 12-EDO | +13.69        | −15.64        | −1.96     |
| 19-EDO | −7.37         | +0.15         | −7.22     |
| 31-EDO | +0.78         | −5.96         | −5.18     |
| 53-EDO | −1.41         | +1.34         | −0.07     |
| 72-EDO | −2.98         | +1.03         | −1.96     |

This reveals something important: there is no universally optimal equal division.

Different EDOs distribute their approximation errors differently. Even a system that represents the major triad exceptionally well might represent another set of intervals less successfully.

### An even more radical possibility: logarithmic scales without octaves

Why insist that the interval repeating the scale must be 2:1?

The Bohlen–Pierce scale takes a different approach. It uses the tritave, a frequency ratio of 3:1, divided into 13 equal logarithmic steps.

Its step ratio is:

r=3^{1/13}

The resulting period is approximately 1901.96 cents.

This is particularly interesting because it offers a musical organization based around relationships involving odd-numbered harmonics, rather than ordinary octave equivalence.

It demonstrates that logarithmic tuning does not intrinsically require an octave as its repeating interval. Tuning +1

### 5\. A more literal logarithmic model: build scales from harmonic relationships

I think there is an even more interesting direction than simply increasing the number of equal divisions.

Instead of deciding in advance that an octave should have 12, 19, 31 or 53 steps, we could derive note positions from the harmonic series itself.

The natural coordinate transformation is:

p(r)=1200\\log_2(r)

This converts a frequency ratio into a position on a logarithmic pitch axis.

For example:

| Harmonic ratio | Pitch position |
| -------------- | -------------- |
| 9:8            | 203.91 cents   |
| 6:5            | 315.64 cents   |
| 5:4            | 386.31 cents   |
| 3:2            | 701.96 cents   |
| 7:4            | 968.83 cents   |
| 11:8           | 551.32 cents   |

Notice that these are not multiples of 100 cents.

The natural harmonic system therefore generates its own irregular pitch lattice.

We could construct a scale by:

* Selecting a set of relevant harmonic ratios.

* Transforming them into logarithmic pitch coordinates.

* Folding them into one octave using modulo 1200 cents.

* Sorting the resulting positions.

* Selecting which relationships are important enough to retain.

This is closely related to just intonation and harmonic-limit tuning.

An important mathematical complication is that allowing arbitrary integer ratios generates an increasingly dense collection of pitch positions. A practical system therefore needs to limit harmonic complexity, for example by restricting the prime factors of its ratios (5-limit, 7-limit, 11-limit tuning).

The advantage is that the resulting scale is derived from harmonic relationships instead of imposed upon them.

### 6\. What about adaptive logarithmic tuning?

There is another possibility that I find particularly promising.

Why should a note have one immutable frequency regardless of its musical context?

Suppose we play a C major chord. We might choose:

C:E:G=4:5:6

But when we move to another chord, the most useful frequency ratios might change.

An adaptive tuning system could continuously calculate the optimal positions of the notes according to the currently sounding chord.

It would work approximately as follows:

### Adaptive harmonic tuning

* Analyse the incoming notes

    Identify fundamentals, pitch estimates and their spectral partials.

* Generate harmonic candidates

    Look for small-integer relationships between the frequencies, especially those associated with prominent partials.

* Calculate logarithmic deviations

    Compare candidate ratios in cents, rather than absolute Hertz.

* Minimize harmonic conflict

    Find frequency adjustments that bring important partials into useful alignment while controlling beating and roughness.

* Apply continuous corrections

    Move notes smoothly rather than abruptly switching between tuning tables.

One possible mathematical objective would be:

E=\\sum_{i,j}\\sum_{m,n}
w_{im}w_{jn}\\,
\\phi(|mf_i-nf_j|)

Here, are the fundamentals, are harmonic numbers, and represents the strength of each partial. The function penalizes undesirable separations between partials.

A realistic implementation would also account for cochlear critical-band filtering, spectral masking, roughness and tuning continuity.

This would be more sophisticated than simply tuning every chord to a fixed just-intonation table.

### 7\. An interesting consequence for musical perception

There is a potentially important distinction between two ways of thinking about musical harmony:

The conventional model:

* Notes occupy predefined positions.

* Chords are collections of those positions.

* Intervals are measured against a fixed tuning grid.

* Harmonic deviations are accepted as part of the temperament.

A harmonic-geometric model:

* Notes are frequency relationships.

* Chords are configurations of interacting harmonic spectra.

* The tuning grid is a convenient coordinate system, not necessarily an acoustic authority.

* Pitch positions can move according to harmonic context.

The second model is particularly interesting for polyphonic electronic instruments, where individual voices can be tuned independently and continuously.

It also suggests that a musical instrument need not have one immutable tuning system. It could use a coarse logarithmic grid for navigation but a continuous harmonic optimizer for actual sound production.

One could even retain conventional note names while allowing the actual frequencies to adapt.

### 8\. My preferred experimental direction

I would investigate three simultaneous representations rather than choosing one tuning philosophy:

Layer 1

Logarithmic pitch coordinate

p=1200\\log_2(f/f_0)

A universal coordinate system for pitch, transposition and interval measurement.

Layer 2

Harmonic coordinate

h_n=\\log_2(n)

Represents the actual positions of partials on the pitch axis. This is where harmonic relationships emerge.

Layer 3

Adaptive tuning coordinate

p_i(t)=p_{i,\\mathrm{reference}}+\\Delta_i(t)

Permits individual notes to deviate from their nominal tuning positions according to the current chord, timbre and spectral interactions.

The key insight is that equal temperament is a uniform coordinate grid, not a fundamental law of acoustics.

The logarithmic transformation is extremely useful because it turns multiplicative frequency relationships into additive distances. But there is no reason to assume that the best musical scale must have uniformly spaced points in that transformed space.

I would particularly investigate nonuniform logarithmic scales whose positions are selected by minimizing the weighted mismatch between the harmonic spectra of simultaneously sounding notes.

That would connect tuning theory, auditory perception, harmonic analysis and optimization into one computational model, rather than treating scale construction and chord acoustics as separate problems.
