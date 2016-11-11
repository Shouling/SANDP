#Tracing Information Flows Between Ad Exchanges Using Retargeted Ads

###Spearker  :  Jianyu
##Pre


<font size=4 face="华为彩云"> 1. This paper is from **Usenix Security 2016**, you can know more details [[pdf](https://www.usenix.org/system/files/conference/usenixsecurity16/sec16_paper_bashir.pdf)][[slides](https://www.usenix.org/sites/default/files/conference/protected-files/security16_slides_bashir.pdf)]. </font> 

<font size=4 face="华为彩云"> 2. This paper is related to Ads. You'd better know the meaning of these **key words** in adavance: </font> <br/>
<font size=4 face="华为彩云">Retargetd Ads;<br/> Online tracking; <br/>Cookie matching; <br/>RTB (Real Time Bidding); <br/>HTTP (HyperText Transfer Protocol)</font> <br/>

##Abstract
<font size=4 face="华为彩云"> Pepole are also unaware of the amount of data sharing that occurs between ad exchanges. Recently work have shown ad exchanges perform cookie mathcing with other exchanges. In RTB auctions, cookie matching is a pre-condition for ad exchanges. In this paper, the authors rely on semantics of how exchanges serve ads and develop a method to detect client- and server-side flows of information between arbitrary ad exchanges. They crawled data on 35,448 ad impressions and showed that our methodology can successfully categorize four different kinds of information sharing behavior between ad exchanges,</font> <br/>

##Contribution


<font size=4 face="华为彩云"> 1. For dectcting flows of tracking information bewteen ad exchages, privious methods only relys on cookie matching. In this paper,the authour give an **insight** of retarged ads and detect **comprehensively**. They show privious method will be not worked in the furture.</font>

<font size=4 face="华为彩云"> 2. They rely on **semantics** of how exchanges serve ads, rather than focusing on specific cookie matching mechanisms. Their methods identify **four different categories** of information sharing between ad exchanges, cookie matching is just one of them.</font>

<font size=4 face="华为彩云"> 3. Although it is known that Google’s privacy policy allows it to share data between its services, Tehy provide the first empirical evidence that **Google** uses this capability to serve retargeted ads.</font>

##Future

<font size=4 face="华为彩云"> 1.Priavcy Preserving : how to block ads and tracking</font><br/>

<font size=4 face="华为彩云"> 2. Information Flow Control : sophisicated blocker for cookie mathching folows<br/></font>

<font size=4 face="华为彩云"> 3. The authour opened their [dataset](http://personalization.ccs.neu.edu/); &nbsp; we can do some reaserch using their dataset as groud truth.<br/></font>


