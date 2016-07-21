***

Where: `Caoguanbiao 208` When: `1:30pm`

***


1. [ ] Xurong, 
2. [ ] Junchi, ----

3. [ ] Jianyu, 


4. [ ] Kai, 

5. [ ] Changting, "Control-Flow Bending: On the Effectiveness of Control-Flow Integrity"

Control-Flow Integrity (CFI) is a defense which pre- vents control-flow hijacking attacks. While recent re- search has shown that coarse-grained CFI does not stop attacks, fine-grained CFI is believed to be secure. 
We argue that assessing the effectiveness of practi- cal CFI implementations is non-trivial and that common evaluation metrics fail to do so. We then evaluate fully- precise static CFI — the most restrictive CFI policy that does not break functionality — and reveal limitations in its security. Using a generalization of non-control-data attacks which we call Control-Flow Bending (CFB), we show how an attacker can leverage a memory corruption vulnerability to achieve Turing-complete computation on memory using just calls to the standard library. We use this attack technique to evaluate fully-precise static CFI on six real binaries and show that in five out of six cases, powerful attacks are still possible. Our results suggest that CFI may not be a reliable defense against memory corruption vulnerabilities.
We further evaluate shadow stacks in combination with CFI and find that their presence for security is nec- essary: deploying shadow stacks removes arbitrary code execution capabilities of attackers in three of six cases.

6. [ ] Fei, 
