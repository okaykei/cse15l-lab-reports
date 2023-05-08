# Lab 3 Report by kei
## Command `less`
I will try 4 different options for the command `less` on 8 examples.  
All of these are sourced from https://man7.org/linux/man-pages/man1/less.1.html.
## less -N
This option displays the line numbers of each line in the file and makes it easier to reference specific lines in the file.  
`less -N rr74.txt` outputs like this(Only the first few lines are shown):
```
      1 
      2   
      3     
      4       
      5         Introduction
      6         NO, which may be synthesized by any of the three
      7         isoforms of NOS, is a vasodilator of the pulmonary
      8         circulation in many mammals. NO has been proposed as a
      9         modulator of vascular tone and structure in the pulmonary
     10         circulation, and previous studies using NOS inhibitors [ 
     10 1,
     11         2] suggested that inhibition of NO increases acute hypoxi
     11 c
     12         pulmonary vasoconstriction. Chronic NOS inhibition did no
     12 t
     13         lead to development of pulmonary hypertension [ 3],
     14         however, possibly because of a decrease in cardiac output
```
`less -N rr73.txt` outputs
```
      1 
      2   
      3     
      4       
      5         Introduction
      6         Three-dimensional (3D) collagen gel culture has been
      7         used as an 
      8         in vitro model of 
      9         in vivo tissue contraction, a common
     10         feature of fibrosis, as well as the resolution of
     11         granulation tissue that characterizes repair [ 1, 2].
     12         Short-term co-cultures of monocytes with fibroblasts resu     12 lt
     13         in the inhibition of collagen gel contraction [ 3], while
     14         co-cultures of fibroblasts with neutrophils, or with
     15         neutrophil elastase (NE), augment contraction [ 4].
     16         Results in the linked study [ 5] demonstrated that 3D
     17         collagen gel contraction was augmented
```
## less -S
This option prevents lines that are longer than the width of the terminal from wrapping to the next line. Instead, they are truncated and displayed as a single line.  
`less -S rr74.txt` shows
```
    
      
        Introduction
        NO, which may be synthesized by any of the three
        isoforms of NOS, is a vasodilator of the pulmonary
        circulation in many mammals. NO has been proposed as>
        modulator of vascular tone and structure in the pulm>
        circulation, and previous studies using NOS inhibito>
        2] suggested that inhibition of NO increases acute h>
        pulmonary vasoconstriction. Chronic NOS inhibition d>
        lead to development of pulmonary hypertension [ 3],
        however, possibly because of a decrease in cardiac o>
        These discrepancies have been addressed in recent st>
        using mice that are deficient in NOS isoforms.
        Three isoforms of NOS are found in the lung. The

```
`less -S rr73.txt` shows
```
    
      
        Introduction
        Three-dimensional (3D) collagen gel culture has been
        used as an 
        in vitro model of 
        in vivo tissue contraction, a common
        feature of fibrosis, as well as the resolution of
        granulation tissue that characterizes repair [ 1, 2].
        Short-term co-cultures of monocytes with fibroblasts>
        in the inhibition of collagen gel contraction [ 3], >
        co-cultures of fibroblasts with neutrophils, or with
        neutrophil elastase (NE), augment contraction [ 4].
        Results in the linked study [ 5] demonstrated that 3D
        collagen gel contraction was augmented in extended
        co-cultures of fibroblasts and monocytes. Since MMPs>
        prominent role in connective tissue degradation [ 6,>
        the current study, an extension of this linked study>
        designed to explore the potential role of MMPs in th>

```
## less -r
This option displays control characters as raw characters so it is useful when working with binary files.  
`less -r rr74.txt` displays
```

  
    
      
        Introduction
        NO, which may be synthesized by any of the three
        isoforms of NOS, is a vasodilator of the pulmonary
        circulation in many mammals. NO has been proposed as a       modulator of vascular tone and structure in the pulmonary    circulation, and previous studies using NOS inhibitors [ 1,  isoforms could contribute to modulation of pulmonary
        vascular tone. Studies using knockout mice for each of
        these isoforms [ 9, 10, 11, 12] suggest that eNOS-derived
        NO is important in modulating basal pulmonary vascular
        tone, as well as in attenuating the development of
        pulmonary hypertension.
        Severe sustained hypoxia causes pulmonary hypertension
        in many animals. Upregulation of all three NOS isoforms
        following severe hypoxia has been reported in rats [ 4, 13,
        14, 15, 16]. Less is certain about the expression of NOS in
        the murine lung following hypoxia, with previous reports [
```
`less -r rr73.txt` displays
```
  
    
      
        Introduction
        Three-dimensional (3D) collagen gel culture has been
        used as an 
        in vitro model of 
        in vivo tissue contraction, a common
        feature of fibrosis, as well as the resolution of
        granulation tissue that characterizes repair [ 1, 2].
        Short-term co-cultures of monocytes with fibroblasts result  in the inhibition of collagen gel contraction [ 3], while    co-cultures of fibroblasts with neutrophils, or with
        neutrophil elastase (NE), augment contraction [ 4].
        Results in the linked study [ 5] demonstrated that 3D
        collagen gel contraction was augmented in extended
        co-cultures of fibroblasts and monocytes. Since MMPs play a  prominent role in connective tissue degradation [ 6, 7, 8],  the current study, an extension of this linked study, was    designed to explore the potential role of MMPs in this       process.

```
## less -P string
This option allows you to customize the prompt string that is displayed at the bottom of the screen when running less. This can be useful for additional info.
`less -P "End of the file here" rr73.txt` displays
```
  
    
      
        Introduction
        Three-dimensional (3D) collagen gel culture has been
        used as an 
        in vitro model of 
        in vivo tissue contraction, a common
        feature of fibrosis, as well as the resolution of
        granulation tissue that characterizes repair [ 1, 2].
        Short-term co-cultures of monocytes with fibroblasts 
result
        in the inhibition of collagen gel contraction [ 3], w
hile
        co-cultures of fibroblasts with neutrophils, or with
        neutrophil elastase (NE), augment contraction [ 4].
        Results in the linked study [ 5] demonstrated that 3D
        collagen gel contraction was augmented in extended
        co-cultures of fibroblasts and monocytes. Since MMPs 
play a
        prominent role in connective tissue degradation [ 6, 
7, 8],
        the current study, an extension of this linked study,
 was
        designed to explore the potential role of MMPs in thi
s
        process.
      
      
        Materials and methods
        
          Cells and cultures
          See Supplementary material.
        
        
          Preparation of collagen gels for three-dimensional
End of the file here
```
`less -P "Press q to quit less" rr73.txt` displays
```
    
      
        Introduction
        Three-dimensional (3D) collagen gel culture has been
        used as an 
        in vitro model of 
        in vivo tissue contraction, a common
        feature of fibrosis, as well as the resolution of
        granulation tissue that characterizes repair [ 1, 2].
        Short-term co-cultures of monocytes with fibroblasts result
        in the inhibition of collagen gel contraction [ 3], while
        co-cultures of fibroblasts with neutrophils, or with
        neutrophil elastase (NE), augment contraction [ 4].
        Results in the linked study [ 5] demonstrated that 3D
        collagen gel contraction was augmented in extended
        co-cultures of fibroblasts and monocytes. Since MMPs play a
        prominent role in connective tissue degradation [ 6, 7, 8],
        the current study, an extension of this linked study, was
        designed to explore the potential role of MMPs in this
        process.
      
      
        Materials and methods
        
          Cells and cultures
          See Supplementary material.
        
        
          Preparation of collagen gels for three-dimensional
Press q to quit less
```
