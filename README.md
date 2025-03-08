java c
CEG8526: Hydrosystems Modelling and Management 
P3: Time series modelling exercises 
Practical summary 
In   this practical   you   will   test   your knowledge   of   time   series models   acquired in   the lectures. By   answering   some   short   tutorial   questions   you   will   assess   your understanding   of   the material   and identify   areas   for   clarification   and reinforcement.   You   will   also use   a simple, pre-existing   Markov   model   coded   in   Python   to   generate   stochastic   rainfall   time series   and   explore how   the parameters   of   the model   change   the   characteristics   of   the simulated   series.
Aim and learning outcomes 
By   the   end   of   this practical   you   should be   able   to:
•          Understand   the   principles   of   Markov   models   and   their   applications   in   modelling rainfall   time   series.
•          Use   a   pre-built   Markov   and   rainfall   generator   model   to   simulate   rainfall   data based   on historical input.
•          Adjust   the   input   parameters   of   the   Markov   model   and   rainfall   generator   to simulate   various   scenarios, including under   climate   change.
•          Analyse   the   output   from   a   Markov   model   and   rainfall   generator   to   derive meaningful   insights   about   rainfall   behaviour.
•          Recognise   the   importance   and   limitations   of   using   stochastic   models   in environmental   sciences   and   engineering   and   for   decision-making.
Tasks 
1 Short questions 
1.1 Which   of   the   following   factors   is   typically   simulated   by   a   weather   generator?
a.      Temperature
b.      Precipitation
c.      Wind   speed
d.      All   of   the   above
1.2 Weather   generators   are   statistical models   that replicate   weather   sequences based   on   historical   data.
True/False
1.3 A   weather   generator   can   be   used   to   assess   the   impact   of   climate   change   on   local agriculture.
True/False
1.4 What   type   of   data   is   essential   for   calibrating   a   stochastic   rainfall   model?
a.      Satellite   images
b.      Historical   rainfall   records
c.      Climate   change   factors   for   daily rainfall
d.      Wind   direction   data
1.5 How   does   a   stochastic   rainfall   model   differ   from   a   deterministic   rainfall   model?
1.6 What   are   the   assumptions   of   the   AR(1) model?
2 A simple Markov model 
Analysis tool 
You   should   use   the   Google   Colab   notebook   (P3_Rainfall_model.ipynb) provided   on Canvas   for   analysis   and   plots. It   is   recommended   that   you   don’t   use   Microsoft   Edge   due    to   caching   issues. Upload   the   Python   notebook   file   and   input   files   provided   on   Canvas   to your   own   Colab   environment. 
Part A 
Review   the   code   in Part A and   then   run   the   Markov   model.
2.1 Which   two   probability   distributions   are   sampled   in   the   model?   You   might   need   to       look up   the   function np.random.rand() to   find   out   one   of   these.   What is   each distribution used   to   represent?
Run   the   code   with   the   default   values   of pww and pdd to produce   the   time   series   and   the   next   block   of   code   to   plot   the   frequency   distribution.
Next, run   the model   again.   You   should   see   that   the   time   series is   different   even   though   you   haven’t   changed   anything.   Why   is   this   the   case?
2.2 Using   the   two   plots   shown,   describe   the   frequency   distribution   of   rainfall   amounts.
Now   change   the   parameters   of   the   Markov   model   so   that   this   time pww =   0.9   and pdd = 0.1 and rerun   the model.
2.3 When   you   change   these parameters, how   do   the   characteristics   of   the   time   series   and   distribution   of   rainfall   change,   and   why?
Next,   see if   you   can   download   the   simulated rainfall   time   series   as   a .csv file.
Open   the   file   in   Excel   and   calculate   the   mean   rainfall   in   the   simulation.   Then,   go back   to   the   model   in   your   notebook   and   change   the inverse_lambda parameter and   rerun   the   model.
2.4 What   do   you   note   happens   to   the   rainfall   distribution? How   does   increasing   and decreasing   the parameter   value   change   the rainfall   distribution?Download   this   data   (using   a   different   filename)   and   calculate   the mean rainfall   for that   data   and   compare it   with   your previous   simulation   with   a   different lambda_inverse value. How   do   the代 写CEG8526: Hydrosystems Modelling and Management P3: Time series modelling exercisesPython
代做程序编程语言   values   compare?
Part B 
The next   section   of   code   for   an input rainfall   series   calculates   the   transition matrix,   some summary   statistics   and   also   calculates   the   scale parameter   of   a   fitted   exponential   distribution. 
Run   this   section   of   code
2.5 What   are   the   6   values   in   the   first   line   of   output?   We   can   use   these   to   see   how   well the   time   series   simulation has reproduced   the required   characteristics   of   the   time   series   from   the previous   section.   What   are   the   values   of pww and pwd in   the   simulated   series?
Part C So   far,   we have   simply input   the parameters   we   wanted   to   generate   the rainfall   series with. In   practice,   we   want   to   produce   simulations   with   statistical   properties   that   match some   observed   time   series.   The next   section   of   code   calculates   the   wet/dry   transition   matrix based   on   an   observed   data   series.
Using   Section C   of   the   worksheet import   the rainfall   data   for   the   Wansbeck   catchment (wansbeck-daily-rainfall-4stations-2003-2012.csv, provided   on   Canvas).   You   will   need   to either   copy   this   file   into   your   workspace   or   use   the   code   provided   to   upload   it   to   your workspace   automatically.
Run   the   code in Part   C   and   compare   the   summary   statistics   and   transition matrix   from   the   observed   data   and   the   simulated   rainfall   series. Run   3   simulations   in total   and   write   down   the   statistics   for   each   simulation in   the   table provided.

Mean rainfall 
Max 
rainfall 
pdd 
pww 
pdw 
pwd 
pwet 
pdry 
Observed series 








Simulated series 








2.7 Note   down   some   comments   on   the   skill   of   the   model   in   reproducing   the   observed rainfall   characteristics.
2.8 Why   do   the   simulated   statistics   vary   each   time?   Why might   generating multiple   simulations   to produce   an   ensemble   of   rainfall   series be useful?
2.9 What   are   the   limitations   of   this   model   and   how   might   you   try   to   improve   these simulations?
Next   download   your   simulated   file,   open it in Excel   and   calculate   the mean rainfall   amount. Note that because the input file had a header the output file has one too and this should not be included in your calculation. 
Now,   we   want   you   to perturb   the rainfall   to   account   for   climate   change.   You   will note   a parameter   called mean_rainfall_change_factor which   we   can use   to   scale   the inverse_lambda parameter. Initially   this   is   set   to   a   value   of   1.0   which   means   if   applied there   is   no   change.   If   we   want   to   produce   a   simulated   rainfall   series   with   an   increase   in mean   rainfall   of   10%   we   can   change   it   to   a   value   of   1.1. If   we   wanted   to   decrease   it   by 10%   we   could   set   the   value   to   0.9.
We   can use   this   approach   therefore   to   downscale   coarse-resolution projections   from climate   models   like   those   provided   by   UKCP18 by   identifying   a   (series   of)   change factor(s)   to   perturb   our   model   and   then   applying   these   to   our   simulation   of   an   observed series   for   a   specific location.Using   output   from   UKCP18, identify   a   plausible   set   of   climate   change   factors   for mean   precipitation   for   this   catchment   and   then   use   those   to   perturb   the   model    by   adjusting   the mean_rainfall_change_factor.   You   could use   the   output   shown      in Figure 1,   or   alternatively   derive   projections   from   the   UKCP18   website   yourself using   an   appropriate   product. Download   the   simulation   and   open   it   in   Excel   and compare   the mean rainfall   amount   for   the previously   downloaded   file   without   climate   change   with   this perturbed   file.
2.10 The   changes   shown   in Figure 1 represent   a   change   factor   calculated   on   annual amounts. Looking   at Figures 2 and 3,   which   represent   projected   future   seasonal changes,   what   do   you note   about   the   difference in projected   changes   for   summer   and winter? How   might   you   improve   the   rainfall   model   to   reflect   these   changes?   What   other features   of   rainfall might   change in   the   future under   climate   change   as   well   as   the mean   amount? How   might   you   incorporate   this   in   the   model? 



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
