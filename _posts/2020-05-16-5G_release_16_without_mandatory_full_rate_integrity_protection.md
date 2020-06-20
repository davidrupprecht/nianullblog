---
layout: post
title:  "5G release-16 without mandatory full-rate integrity protection."
date:   2020-05-16 14:20:58 +0200
author: David Rupprecht
categories: integrity_protection 5G
---

Missing integrity protection is one of the biggest threats to the security of the present (LTE) and future (5G) mobile network generations. As demonstrated with the aLTEr and IMP4GT attack, an attacker only in the vicinity of the victim can break the fundamental security aims [[1][1],[2][2]]. The aLTEr attack allows an attacker to redirect to a malicious website by manipulating the destination address of IP packets. With the IMP4GT attack, an attacker can forge arbitrary and read arbitrary IP packets, which lead to a full impersonation of a victim towards the network and vice versa. With this impersonation, an attacker can bypass any operators' firewall mechanism. Both attacks exploit the lack of integrity protection of the user plane in LTE. However, also, the current 5G specification does not mandate full rate user plane integrity protection, which makes them vulnerable to the same attacks. Those 5G networks will surround us for the next few decades. Therefore, is mandatory user plane integrity protection indispensably connected with the security of 5G.

Responsible for adding mandatory full-rate integrity protection to 5G networks is the 3GPP, a consortium that specifies the 5G standard in the form of releases. In particular, release 16, frozen in June, is the last chance to add mandatory integrity protection to the 5G specification. This is because release 16 is the first feature freeze release for the 5G NR Standalone radio layer. Adding security in a later release, is an inadequate option, as backward compatibility weakens even newer releases. Thus, if mandatory full rate UP IP is not specified for release 16, we face 5G networks that are prone to sustainable attacks, e.g., IMP4GT, and aLTER. 

To mitigate the threat of those attacks in 5G networks, a large group of providers and some vendors have attempted to mandate integrity protection in the 5G specification [[3][3],[4][4]].  This was already in March. However, this attempt was postponed due to some vendors' objection, mainly baseband vendors, e.g., Qualcomm, OPPO, and Samsung [[5][5],[6][6]]. They argue that it is challenging to integrate full-rate integrity protection due to the performance requirements and need more technical discussion on a working group level [[7][7]]. Last week (11-15. May 2020), another attempt tried to add mandatory full rate integrity protection [[8][8],[8a][8a]]. Again this was postponed (3GPP term "noted") by the vendors [[9][9],[10][10],[11][11]]. This was the last chance to secure 5G networks against substantial attacks. Consequently, we will use insecure 5G standalone networks in two years.


#### Personal Comment 
The issue of missing integrity protection is known since March 2018 [[1][1]]. Some 3GPP documents even date back to 2006, stating that missing integrity protection can be a security problem [[12][12]]. This gives the impression that manufacturers are not taking the problem seriously. However, I also understand that securing things is a difficult job, particularly with complex stack architecture and performance requirements. However, this problem is known for at least two years. Thus I ask myself, what is the exact problem? Can we (research and 3GPP community) solve those problems with improved integrity protecting algorithm? Therefore, if you are a vendor facing these problems, please reach out (to me) and describe the exact issues. 

[1]: http://www.alter-attack.net

[2]: http://www.imp4gt-attacks.net

[3]: https://list.etsi.org/scripts/wa.exe?A2=ind2003C&L=3GPP_TSG_RAN&O=D&P=708304

[4]: https://www.3gpp.org/ftp/tsg_ran/TSG_RAN/TSGR_87e/Docs/RP-200505.zip

[5]: https://list.etsi.org/scripts/wa.exe?A2=ind2003C&L=3GPP_TSG_RAN&O=D&P=818676

[6]: https://list.etsi.org/scripts/wa.exe?A2=ind2003C&L=3GPP_TSG_RAN&O=D&P=789090

[7]: https://list.etsi.org/scripts/wa.exe?A2=ind2003C&L=3GPP_TSG_RAN&O=D&P=785131

[8]: https://list.etsi.org/scripts/wa.exe?A2=3GPP_TSG_SA_WG3;324ceb1c.2005B

[8a]: https://www.3gpp.org/ftp/tsg_sa/WG3_Security/TSGS3_99e/Inbox/Drafts/draft_S3-201031-r2.docx

[9]: https://list.etsi.org/scripts/wa.exe?A2=3GPP_TSG_SA_WG3;78288ec9.2005C

[10]: https://list.etsi.org/scripts/wa.exe?A2=3GPP_TSG_SA_WG3;c9fe9ab4.2005C

[11]: https://list.etsi.org/scripts/wa.exe?A2=3GPP_TSG_SA_WG3;352ea8e2.2005C

[12]: https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=2311
