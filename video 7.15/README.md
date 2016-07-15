***

Where: `Caoguanbiao 208` When: `1:30pm`

***


1. [ ] Xurong, Measuring Real-World Accuracies and Biases in Modeling Password Guessability

Abstract:
Parameterized password guessability?how many guesses a particular cracking algorithm with particular training data would take to guess a password?has become a common metric of password security. Unlike statistical metrics, it aims to model real-world attackers and to provide per-password strength estimates. We investigate how cracking approaches often used by researchers compare to real-world cracking by professionals, as well as how the choice of approach biases research conclusions. We find that semi-automated cracking by professionals outperforms popular fully automated approaches, but can be approximated by combining multiple such approaches. These approaches are only effective, however, with careful configuration and tuning; in commonly used default configurations, they underestimate the real-world guessability of passwords.
We find that analyses of large password sets are often robust to the algorithm used for guessing as long as it is configured effectively. However, cracking algorithms differ systematically in their effectiveness guessing passwords with certain common features (e.g., character substitutions). This has important implications for analyzing the security of specific password characteristics or of individual passwords (e.g., in a password meter or security audit). Our results highlight the danger of relying only on a single cracking algorithm as a measure of password strength and constitute the first scientific evidence that automated guessing can often approximate guessing by professionals.

2. [ ] Junchi, EVILCOHORT: Detecting Communities of Malicious Accounts on Online Services

3. [ ] Jianyu, Finding Unknown Malice in 10 Seconds: Mass Vetting for New Threats at the Google-Play Scale 

Abstract:

An app market’s vetting process is expected to be scal- able and effective. However, today’s vetting mechanisms are slow and less capable of catching new threats. In our research, we found that a more powerful solution can be found by exploiting the way Android malware is constructed and disseminated, which is typically through repackaging legitimate apps with similar malicious com- ponents. As a result, such attack payloads often stand out from those of the same repackaging origin and also show up in the apps not supposed to relate to each other.
Based upon this observation, we developed a new technique, called MassVet, for vetting apps at a mas- sive scale, without knowing what malware looks like and how it behaves. Unlike existing detection mecha- nisms, which often utilize heavyweight program analy- sis techniques, our approach simply compares a submit- ted app with all those already on a market, focusing on the difference between those sharing a similar UI struc- ture (indicating a possible repackaging relation), and the commonality among those seemingly unrelated. Once public libraries and other legitimate code reuse are re- moved, such diff/common program components become highly suspicious. In our research, we built this “Diff- Com” analysis on top of an efficient similarity compar- ison algorithm, which maps the salient features of an app’s UI structure or a method’s control-flow graph to a value for a fast comparison. We implemented MassVet over a stream processing engine and evaluated it nearly 1.2 million apps from 33 app markets around the world, the scale of Google Play. Our study shows that the tech- nique can vet an app within 10 seconds at a low false detection rate. Also, it outperformed all 54 scanners in VirusTotal (NOD32, Symantec, McAfee, etc.) in terms of detection coverage, capturing over a hundred thou- sand malicious apps, including over 20 likely zero-day malware and those installed millions of times. A close look at these apps brings to light intriguing new observations: e.g., Google’s detection strategy and malware authors’ countermoves that cause the mysterious disap- pearance and reappearance of some Google Play apps.

4. [ ] Kai, Trustworthy Whole-System Provenance for the Linux Kernel(https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/bates)

5. [ ] Changting, Eclipse Attacks on Bitcoin’s Peer-to-Peer Network

6. [ ] Fei, ----
