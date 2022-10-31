# Week 5 lab report


# -h
`grep -h 'medicine' biomed/*.txt`
```
          medicines of the same class as the blinded drugs, see
        prescription of open-label medicines of the same class as
        advancing the fields of biology and medicine. Most
        activities and have been utilized extensively in medicine,
        activity, more use of health services and medicines and
        how long it would take for prescribed medicine to work, did
        medicine, St. Agnes Hospital, Baltimore, MD 21229. An
        a nuclear medicine scan with 1.5 mCi of 111indium
        WHM - performed and interpreted the nuclear medicine
          medicine (n = 7) and internal medicine (n = 5)
          views on the nature and goals of preventive medicine, use
          medicine in the health care arena. Physicians offered
          preventive medicine, highlighted primary, secondary, and
          to have a liver side effect if they take a medicine ...
        and the separation of preventive from curative medicine,
        budget) for preventive medicine and public health
        specialty skills of a palliative medicine physician. Two
        We asked internal medicine residents caring for severely
            medicine residents, a social worker, and chaplain and,
            year internal medicine residents over a one-month
        medicine as a "culture of action" - it is better to do
          their bush medicine remedies. One research hazard was the
          Hunters' ethnoveterinary medicines
```

This is the output, but every instance of 'medicine' is highlighted red. -h made
it so much nicer to read since it blocks the output of the filename so all you
see is the actual text.

`grep -h 'one' biomed/*.txt`
```
          telephone interview.
          subscale, one point is assigned for each medication used
          during the past 2 weeks, with one additional point for
          asthma [ 31]. The physical and mental component summary
          As shown in Figures 1and 2, fibroblasts alone
          cultured alone released no gelatinolytic activity (data
          MMP-2 to the 66 kDa form in fibroblasts cultured alone
          activity in monocytes cultured alone (data not
          monocytes (Fig. 3). In fibroblasts alone, a trace of
          of monocytes or fibroblasts alone.
```
Here I have a similar search, but with short text as the full copy is a waste of space
but this highlighted every instance of 'one' making it much easier to have text output
without the constant file names.

`grep -h 'one' biomed/*.txt`
```
        NO production despite the increase in NOS expression. There
        NO production and increased NOS expression
        previous studies, the plasma NO metabolite content in the
        account for the slight increase in plasma NO metabolites
        and pulmonary vasculatures can both contribute to plasma NO
        metabolite levels, if NOS was downregulated in the systemic
        increased NO metabolites could also be due to decreased NOS
        investigators did not observe any difference in plasma NO
        NOS was downregulated, but did observe a decrease in
        acetylcholine-stimulated NO release from aortic rings. The
        pattern of NOS expression in vascular beds other than the
        In summary, we identified a unique pattern of NOS
        considering studies using NOS-deficient mice. The present
        eNOS = endothelial nitric oxide synthase; iNOS =
        inducible nitric oxide synthase; nNOS = neuronal nitric
        oxide synthase; NO = nitric oxide; NOS = nitric oxide
```
The same search with -h but it makes the output very clean, and easy to find what 
you're looking for if you just want the text.

# -o

`grep -o 'super' biomed/*.txt`
```
biomed/gb-2003-4-9-r57.txt:super
biomed/rr166.txt:super
biomed/rr166.txt:super
biomed/rr166.txt:super
biomed/rr166.txt:super
biomed/rr167.txt:super
biomed/rr167.txt:super
biomed/rr171.txt:super
biomed/rr171.txt:super
```
This too has all of super highlighted, but it seems -o gives the piece that you
searched for and nothing else. This would be useful if you had to search for 
multiple things and put them all in a file so you could keep track of your
findings.

`grep -o 'super' biomed/*.txt`
```
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
super
```
Combining -o with -h I thought was pretty funny since all you get is a list of the 
item you looked for. I suppose the only use would be to see how many instances 
there were of the item, but other than that this combiniation doesn't seem too
helpful.


`grep -o 'doctor' biomed/*.txt`
```
biomed/1471-2458-2-25.txt:doctor
biomed/1471-2458-3-20.txt:doctor
biomed/1471-2458-3-9.txt:doctor
biomed/1472-6793-2-19.txt:doctor
biomed/1472-684X-2-2.txt:doctor
biomed/1472-6882-1-12.txt:doctor
biomed/1472-6882-2-5.txt:doctor
biomed/1472-6920-2-1.txt:doctor
biomed/1472-6947-1-2.txt:doctor
biomed/1472-6963-1-8.txt:doctor
biomed/1472-6963-3-14.txt:doctor
biomed/1478-7954-1-3.txt:doctor
```
Just another example of finding words easily with their respective file 
for easy sight without the entire blocks of text.

# -i

`grep -i 'NO' biomed/*.txt`
```
biomed/rr73.txt:        fibroblasts and monocytes augmented collagen gel
biomed/rr73.txt:        this context, fibroblasts are known to express cell surface
biomed/rr73.txt:        This study demonstrates that monocytes and fibroblasts
biomed/rr73.txt:            between cell passages 14 and 16. Blood monocytes were
biomed/rr73.txt:            isolated from blood cells of healthy blood donors [
biomed/rr73.txt:            32]. Cell suspensions were >96% monocytes by the
biomed/rr73.txt:            cytosmears. Monocytes were stored at 4°C and were used
biomed/rr73.txt:            Technologies, Grand Island, NY, USA). Fetal calf serum
biomed/rr73.txt:            concentrations of ethanol (from 50% to 100%), type I
biomed/rr73.txt:            no detectable protein other than type I collagen.
biomed/rr73.txt:            ethanol precipitation and resuspension in distilled H
biomed/rr73.txt:            pH6.8, 2% SDS, 20% glycerol, 0.1% bromophenol blue),
biomed/rr73.txt:            blue and rapidly destained with 30% (v/v) methanol, 10%
biomed/rr73.txt:            Immunoblot analysis of metalloproteinases
biomed/rr73.txt:            10-fold by precipitation with ethanol, resuspended in
biomed/rr73.txt:            buffer (0.5 M Tris-HCl, pH6.8, 2% SDS, 0.1% bromphenol
biomed/rr73.txt:            blue, 0.5% β-mercaptoethanol, 20% glycerol). After
biomed/rr73.txt:            Tris-HCl, pH8.0, 150 mM glycine, 20% methanol) at 20 V
biomed/rr74.txt:        NO, which may be synthesized by any of the three
biomed/rr74.txt:        isoforms of NOS, is a vasodilator of the pulmonary
biomed/rr74.txt:        circulation in many mammals. NO has been proposed as a
biomed/rr74.txt:        circulation, and previous studies using NOS inhibitors [ 1,
```
-i is a very nice command as it allows for the string to be searched without
worry of the casing of the letters. Very useful for finding all instances of a
string.

`grep -i -o -h 'NO' biomed/*.txt`
```
NO
NO
NO
NO
no
no
NO
NO
NO
NO
NO
NO
NO
NO
NO
NO
no
NO
no
NO
NO
NO
no
NO
NO
```
Another command set that I just wanted to try, but it shows each instance of NO no matter
the casing and without the file. Not sure what it would be used for.


`grep -i 'DoCtOr' biomed/*.txt`
```
biomed/1471-2458-3-9.txt:        that a doctor's recommendation to have breast cancer
biomed/1472-6793-2-19.txt:        author DER (doctoral candidate) and contributed to the
biomed/1472-684X-2-2.txt:        suggest different attitudes of doctors and policies of
biomed/1472-6882-1-12.txt:        case management increases patient-doctor interaction and
biomed/1472-6882-2-5.txt:        their doctor or pharmacist. The most commonly consulted CAM
biomed/1472-6920-2-1.txt:          course, Patient-Doctor II [ 4 ] . The course is taught
biomed/1472-6920-2-1.txt:            patient-doctor interaction techniques (patient
biomed/1472-6947-1-2.txt:        treatment options with their doctors. A recent study
biomed/1472-6963-1-8.txt:        who typically received influenza vaccination in a doctor's
biomed/1472-6963-3-14.txt:            effect when none exists. A doctor who knows that the
biomed/1478-7954-1-3.txt:        doctors [ 28 ] . An important aspect in the analyzing the
```
The nice part about using -i is that, if you're using it to automate something,
you don't have to worry about it missing words since it will grab all of them 
no matter the case.
