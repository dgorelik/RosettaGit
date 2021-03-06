+++
title = "Egison"
description = ""
date = 2015-02-12T04:37:35Z
aliases = []
[extra]
id = 17123
[taxonomies]
categories = []
tags = []
+++

{{language|Egison
|strength=strong
|safety=safe
|checking=dynamic
|gc=yes
|LCT=yes
|site=http://www.egison.org}}
{{language programming paradigm|Pattern-matching oriented}}
{{language programming paradigm|functional}}
{{implementation|Lisp}}

'''Egison''' is a programming language that realizes non-linear pattern-matching against unfree data types.
We can directly represent pattern-matching against a wide range of data types such as lists, multisets, sets, trees and graphs.
Egison makes programming dramatically simple!

= Pattern Matching Oriented =

Egison proposes a new paradigm pattern-matching-oriented. The combination of all of the following features enables intuitive powerful pattern-matching.

* Non-linear patterns
* Pattern-matching with multiple results
* Modularization of the way of pattern-matching
* Pattern-matching with lexical scoping

= Poker Hands Demonstration =


```egison

;;;
;;;
;;; Poker-hands demonstration
;;;
;;;

;;
;; Matcher definitions
;;
(define $suit
  (algebraic-data-matcher
    {<spade> <heart> <club> <diamond>}))

(define $card
  (algebraic-data-matcher
    {<card suit (mod 13)>}))

;;
;; A function that determins poker-hands
;;
(define $poker-hands
  (lambda [$cs]
    (match cs (multiset card)
      {[<cons <card $s $n>
         <cons <card ,s ,(- n 1)>
          <cons <card ,s ,(- n 2)>
           <cons <card ,s ,(- n 3)>
            <cons <card ,s ,(- n 4)>
             <nil>>>>>>
        <Straight-Flush>]
       [<cons <card _ $n>
         <cons <card _ ,n>
          <cons <card _ ,n>
            <cons <card _ ,n>
              <cons _
                <nil>>>>>>
        <Four-of-Kind>]
       [<cons <card _ $m>
         <cons <card _ ,m>
          <cons <card _ ,m>
           <cons <card _ $n>
            <cons <card _ ,n>
              <nil>>>>>>
        <Full-House>]
       [<cons <card $s _>
         <cons <card ,s _>
           <cons <card ,s _>
             <cons <card ,s _>
               <cons <card ,s _>
                 <nil>>>>>>
        <Flush>]
       [<cons <card _ $n>
         <cons <card _ ,(- n 1)>
          <cons <card _ ,(- n 2)>
           <cons <card _ ,(- n 3)>
            <cons <card _ ,(- n 4)>
             <nil>>>>>>
        <Straight>]
       [<cons <card _ $n>
         <cons <card _ ,n>
          <cons <card _ ,n>
           <cons _
            <cons _
             <nil>>>>>>
        <Three-of-Kind>]
       [<cons <card _ $m>
         <cons <card _ ,m>
          <cons <card _ $n>
            <cons <card _ ,n>
             <cons _
               <nil>>>>>>
        <Two-Pair>]
       [<cons <card _ $n>
         <cons <card _ ,n>
          <cons _
           <cons _
            <cons _
             <nil>>>>>>
        <One-Pair>]
       [<cons _
         <cons _
          <cons _
           <cons _
            <cons _
             <nil>>>>>>
        <Nothing>]})))

;;
;; Demonstration code
;;
(poker-hands {<Card <Club> 12>
                    <Card <Club> 10>
                    <Card <Club> 13>
                    <Card <Club> 1>
                    <Card <Club> 11>});=><Straight-Flush>

(poker-hands {<Card <Diamond> 1>
                    <Card <Club> 2>
                    <Card <Club> 1>
                    <Card <Heart> 1>
                    <Card <Diamond> 2>});=><Full-House>

(poker-hands {<Card <Diamond> 4>
                    <Card <Club> 2>
                    <Card <Club> 5>
                    <Card <Heart> 1>
                    <Card <Diamond> 3>});=><Straight>

(poker-hands {<Card <Diamond> 4>
                    <Card <Club> 10>
                    <Card <Club> 5>
                    <Card <Heart> 1>
                    <Card <Diamond> 3>});=><Nothing>

```

