# Review

## Info

Reviewer Name: McKell Stauffer

Paper Title: Benchmarking Crimes: An Emerging Threat in Systems Security

## Summary

### Problem and why we care

This paper focuses on common mistakes made by system security papers in the realm of performance benchmarking. 
These mistakes are a serious problem because they compromise performance guarantees and reproducibility/comparability of papers, thereby harming the overall scientific process.
This is especially important because these mistakes are usually not intentional and can be found across time and venues.

### Gap in current approaches

This paper was the first of its kind in system security.
It pointed out 22 benchmarking mistakes and found that the mistakes were commonly made in papers published at top-tier conferences.

### Hypothesis, Key Idea, or Main Claim

This paper claims that the 22 enumerated benchmarking mistakes are common to system security papers.
They also claim that these mistakes should be eliminated from papers, as they are currently harming the scientific process by undermining performance guarantees, reproducibility, and comparability.
They propose that each mistake hurts at least one of the following categories: completeness, relevancy, soundness, or reproducibility.

### Method for Proving the Claim

They have two independent readers read through 50 different papers from top conferences (the traditional "top 4" venues in systems security) from both 2010 and 2015.
Each reader categorized each paper for each crime as correct, flawed, underspecified, or not applicable.'
If the readers did not give the same categorization, they discussed it until they decided on a categorization.

### Method for evaluating

Once all the categorizations were given, the authors evaluated how often each mistake appeared in both 2010 and 2015 papers. They counted the number of papers that commited each individual mistake and split up the count by years. They also included how many of the mistakes were flawed or underspecified. They used a chi-squared test to test for the significance of the results if it can be applied. If it cannot be applied, they used Yates' correction for continuity.

### Contributions: what we take away

Benchmarking "crimes" are common made in system security papers, even at the top conferences. 
These crimes are often not on purpose and could easily be avoided if authors become more conscious of them. 
Avoiding these crimes would lead to more completeness of papers and greater reproducibility and comparability.
This in term would lead to a more fully-realized scientific process.

## Pros (3-6 bullets)

- If benchmarking crimes were eliminated, system security research would become more reproducible.
- If benchmarking crimes were eliminated, researchers could trust performance guarantees of models more.
- The paper set forth a good framework on how to evaluate perceived problems in a research field.

## Cons (3-6 bullets)

- Making sure to commit none of these "crimes" could be time consuming and ardous for the author.
- It would be hard to enforce compliance with all of these rules at conferences.
- Some may argue that novel ideas are worth publishing, even if their evaluations are not up to some perfect standard.

### What is your analysis of the proposed?

These paper did a very good job at evaluating benchmarking mistakes in the field.
I liked that they looked at research at top conferences, did not point fingers at any particular paper, evaluated across two years, and had independent readers.
I also thought they did a wonderful job at delineating what each "crime" was and how one could avoid it.
Their list seemed very relevant and thorough.

I also appreciated that this paper tried hard to also be reproducible. 
From producing chi-squared tests inbetween the 2010 and 2015 results and repeatedly putting forth information that would be useful for reproducibility, I think they set a good example. 
I like that this paper was published as I think works evaluating the current state of research are incredibly important to move the field further. 
I think all conferences should have reproducibility requirements and some sort of keynote of papers like these to talk about what the field could do to improve their research quality.

## Details Comments, Observations, Questions

My favorite part of this paper was definitely when they called out machine learning. 
But, to be honest, I felt like it was a little ill-considered as I've personally never seen ML researchers use training data in their test set. 
I've always seen it be very separated. 
Reproducibility is a ginormous problem in ML research though, so I very much felt like I related to this paper. 
For ML papers, I think code + specifications of hardware and packages must be required of papers for reproducibility. 
The trouble with ML though is you could run their code on a different machine & get wildly different results, so its a little different.

### Discussion Questions:

Review/Understanding
- What are the correct ways to measure overhead? What pitfalls can you recall?
- What is the proper baseline for raw measurements in system defenses? (e.g. runtime, throughput numbers)
- What are some examples of microbenchmarks? Macrobenchmarks?
- Can you think of any benchmarking crimes committed by any papers that we have read this year?

Analysis of paper
- Do you agree with this list of benchmarks? Are there "crimes" that you would take out or add in? Are there crimes that you would change if they are high-impact or not?
- Which "crime" did you find most interesting to learn about? Which "crimes" do you find to be the most important to not commit?
- What would you say is an allowable amount of "crimes" a systems paper may commit? Should all systems papers not commit any "crimes"?
- How realistic do you find it to not commit any benchmarking crimes when pressed by time for paper submissions? Do you feel that they can be done with "relatively little effort" as the author describes?
- How important are performance benchmarking crimes in the realm of security research? If a paper had an awesome security system, but had performance benchmarking crimes, would you accept it (assuming you were reviewing for a conference)? What if it was a novel systems idea?
- Do you feel like you run into these crimes often in papers you read?

More general
- How important do you think papers in this category (e.g. analyzing current research trends and failings) are to academia? Do you feel like papers are the best medium for these discussions? Or would other mediums (keynote talks, blog posts, workshops, etc.) be more appropriate?
- What in your opinion makes a trustworthy paper?
- Do conferences have a responsibility to enforce papers to have reproducible results? As in, should they require papers to have the software, systems used, etc?
