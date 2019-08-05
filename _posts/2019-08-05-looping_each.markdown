---
layout: post
title:      "LOOPing.each"
date:       2019-08-05 15:59:57 +0000
permalink:  looping_each
---


A useful mechanism when your code needs to be repeated. Looping in the code can be designed to cycle until specific conditions are met by using a loop call such as *.each* ,*loop* or *.times*.  Below are a couple of examples:

If you are trying to return a string more than once..

3.times do
     puts "Ice melts"          *  #=>"Ice melts"*
end                                                 *"Ice melts"*
                                                       *  "Ice melts"*

* OR*

loop do
   counter += 1
	 puts "Iteration #{counter} of the loop"
	 if counter >= 10
   break
	 end
end

