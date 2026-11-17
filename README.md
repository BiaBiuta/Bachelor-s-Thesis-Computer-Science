ABSTRACT
The Nurse Scheduling Problem (NSP) deals with finding the optimal way to as
sign nurses to shifts, while taking into account a set of constraints- both hard con
straints which all solutions must follow in order to be valid (e.g. the maximum
hours a nurse can work per week as imposed by labour laws), as well as soft con
straints which dictate the relative quality of a solution (e.g. the personal preferences
of nurses for shifts/holidays). Traditionally, scheduling is a time-consuming and
challenging task, that is difficult to optimize manually and adapt to dynamic chan
ges of staff, and yet it is critical for the quality of healthcare provided by hospitals.
Furthermore, being anNP-hardproblem, exactmathematicalapproachesfailtopro
duce solutions within practical time limits when applied to large-scale, real-world
scenarios.
With these limitations in mind, the aim of this paper is to develop two hybrid he
uristic algorithms designed to automatically generate high-quality nurse shift sche
dules. The first proposed algorithm integrates local search techniques with periodic
calls to a Mixed-Integer Programming (MIP) solver on restricted subproblems, to
escape local optima and refine key schedule portions. The second algorithm em
ploys a genetic algorithm (GA) for global exploration and integrates both a local
improvement phase where MIP optimization is applied to the most promising chro
mosomes, and a fallback mechanism where a global MIP solver is used when hard
constraint violations stagnate, ensuring solution feasibility. Both strategies achieve
superior solutions by leveraging the diversification capabilities of local and evolu
tionary search, respectively, and the intensification provided by mathematical local
optimization via MIP.
The hybrid genetic algorithm is then integrated into a modern web application
developed with the Djangoframework, whicheasestheeffort of administrative per
sonnel responsible for the nurse scheduling task- it provides the valuable feature
of automatic schedule generation, as well as features for visualizing and manua
lly editing the schedule, managing personal nurse preferences for work shifts, and
administering resources between multiple medical departments.
