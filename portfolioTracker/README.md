Pre-requisite: Have q installed. To install q, go to www.kx.com.


How to run this portfolio tracker for backtesting purpose:

1.Run ticker plant.

        >q tick.q sym . -p 5010
        
tick.q source code can be downloaded from http://code.kx.com/wsvn/code/kx/ .

2.Run Timer Service. The code is available under /hisTickData directory. 

        >q timersvc.q [csv file] [sym] 
        
        example:
        q timersvc.q tradeGE.N0821.csv GE
 

3.Run execsvc.q.

        >q execsvc.q

4.Run pnlsvc.q

        >q pnlsvc.q
        
        in the q prompt, run
        q)\l insertCCY.q
        
5.Open portfolioTracker.html in your browser.

6.Optional. Run this if you want to save position table.

        >q savePos.q
        
  The saved table will be automatically loaded next time you run pnlsvc.q

