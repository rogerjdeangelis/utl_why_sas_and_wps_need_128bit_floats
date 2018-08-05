# utl_why_sas_and_wps_need_128bit_floats
Why sas and wps need 128bit floats. Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverflow SAS community.

     Why sas and wps need 128bit floats

     One of the great accomplisments of SAS is the comversion of floats to other datatypes.
     128bit floats solves many problems. (ie packed decimal, pib, ib, rb8 . ...)

     REASONS

        1, Relatively easy to add 128bit floats to input/output  SAS datasets (eliminates for integer and decimal types)
           Very natural and easy for INTEL/AMD to add 128bit cores(engines). Already possible with CUDA?

        2. Although 64bit floats have more range than 64bit integers, floats have less precision.

        3. 128bit floats represent 64bit integers exactly

        4. 128bit floats represents 64bit decimals exactly. (decimal arithmetic)

        5. In pysics when we know the closed form solution, 64bit floats may fail to converge,
           when 128bit floats converge,  especiall in the case of 1 + .1*-300 issues.

        6. 64bit addresses cannot be easily added or substracted. Peek and Poke..

        7. With all the recent SAS competition 128bit floats would be a differentiator

        8. Better universal keys

        9. Helps to eliminate 'Proc ds2', less is more.

       10. When dealing with dollars and cents it is often necessay to mutiply by 100,
           so that numeric vales are represented exactly and products and sums are exact.
           This further reduces the range of 'integers'

       11. Much fewer rounding problems.

       12. Longer streams of random numbers.


     One of the great accomplisments of SAS is the comversion of floats to other datatypes.
     128bit floats solves many problems.

     Cannot represent a futute US national debt exactly in pennies.

      19,000,000,000,000.67  * can be represented exactly in pennies;
                             * too close to the precipice of rounding even at 19 trillion;

      99,000,000,000,000.67  * cannot be represented exactly in pennies;

     data _null_;

       * exact in pennies;
       x=  16000000000000.67;
       z=  100*round(x,.01);
       put z= 18.;

       * not exact in pennies;
       x=  99000000000000.67;
       z=  100*round(x,.01);
       put z= 18.;

    run;quit;

       Z=1600000000000067  ** exact pennies;
       Z=9900000000000068  ** one penny off;



