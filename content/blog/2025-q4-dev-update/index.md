+++
type = "blog"
title = '2025 September-December Quarterly Development Update'
date = 2025-12-15
+++

This is the TLA⁺ Foundation quarterly development update ([subscribe via RSS](/blog/index.xml)).
Here we summarize the past three months of development for the benefit of Foundation patrons and interested members of the community.
If your TLA⁺ contribution was missed, worry not - open an issue [here](https://github.com/tlaplus/foundation/issues).

If you're interested in getting involved in the TLA⁺ community:
- Learn TLA⁺ starting [here](https://lamport.azurewebsites.net/tla/learning.html)!
- Join the monthly virtual community meetings [here](https://zoom-lfx.platform.linuxfoundation.org/meetings/tla?view=month)!
- Read the mailing list [here](https://groups.google.com/g/tlaplus)!
- Start hacking on the tools themselves [here](https://github.com/tlaplus/tlaplus)!

### Organizational Updates

- The TLA⁺ Foundation grant program is continuing on a rolling basis; please [submit a proposal](/grants/2024-grant-program/) if you have ideas to improve TLA⁺ so the Foundation can support you financially as you work on them.
  You can find some desired projects listed [here](https://github.com/tlaplus/tlaplus/issues?q=is%3Aissue%20state%3Aopen%20label%3A%22TLA%2B%20Foundation%20Funding%22).
  If you're trying to figure out the next stage of your career and like the sound of being paid a stipend to work on free & open source software in the formal methods space, this is a great opportunity!
- The TLA⁺ Outreach Committee is now hosting general monthly meetings open to the community; see details [here](https://groups.google.com/g/tlaplus/c/f717xF3RGEs/m/fkwID-HLCQAJ)!
  The Committee brings together individuals who are passionate about advancing TLA⁺ and promoting its adoption.

### Posts & Papers

- Murat Demirbas [wrote a post](https://muratbuffalo.blogspot.com/2025/11/tla-modeling-of-aws-outage-dns-race.html) dissecting the October 2025 AWS outage DNS race condition with a TLA⁺ spec.
  He also wrote another post on [TLA⁺ modeling tips](https://muratbuffalo.blogspot.com/2025/12/tla-modeling-tips.html).
- [A. Jesse Jiryu Davis](https://emptysqua.re/blog/leaseguard-raft-leader-leases-done-right/) and [Murat Demirbas](https://muratbuffalo.blogspot.com/2025/12/leaseguard-raft-leases-done-right.html) of MongoDB research both published posts on their collaboration developing [LeaseGuard](https://arxiv.org/abs/2512.15659), a more reliable leadership lease protocol for the Raft consensus protocol. The protocol was [specified in TLA⁺](https://github.com/muratdem/RaftLeaderLeases/tree/c773c123bdbbf9aeb18031feddd6b291317faf5e/TLA).
- William Schultz and Murat Demirbas of MongoDB research presented a paper titled [*Design and Modular Verification of Distributed Transactions in MongoDB*](https://www.vldb.org/pvldb/vol18/p5045-schultz.pdf) at VLDB 2025.
  The cross-shard transaction protocol was [specified in TLA⁺](https://github.com/mongodb-labs/vldb25-dist-txns)
- Lorin Hochstein [posted a write-up](https://surfingcomplexity.blog/2025/12/14/aws-reinvent-talk-on-their-oct-25-incident/) of an AWS talk at re:Invent about the October 2025 AWS outage.
  Interestingly, the original system design was formally specified in TLA⁺ and did not have the race condition; the race condition was introduced by subsequent incremental changes to the system without updating the spec.
  Lorin also wrote a post on [thinking of formal specifications as sets of behaviors](https://surfingcomplexity.blog/2025/07/26/formal-specs-as-sets-of-behaviors/).
- Igor Konnov [wrote a post](https://protocols-made-fun.com/tlaplus/2025/12/15/tftp-symbolic-testing.html) about conformance testing between TLA⁺ specifications and implementations, using model-based testing and trace validation; he [also wrote about](https://protocols-made-fun.com/pbt/2025/12/22/pbt-adversarial-llms.html) applying this to LLM-generated code.
  Another post [summarized a talk he gave](https://protocols-made-fun.com/tlaplus/2025/12/02/small-scope.html) at NVIDIA's internal Formal Methods Week 2025 conference, featuring TLA⁺.
- Cheng Huang [also presented at NVIDIA FM Week 2025](https://zfhuang99.github.io/github%20copilot/formal%20verification/tla+/2025/11/14/lamport-agent.html), on using LLMs to extract TLA⁺ specifications from existing systems.
- Siddhartha Jayanti and Ugur Y. Yavuz published a paper titled [*Formal Machine-Verification of MemSnap: An Efficient, Far-Future Linearizable Snapshot Algorithm*](https://dl.acm.org/doi/10.1145/3694906.3743304), specifying their protocol in TLA⁺ and proving properties [with the TLA⁺ proof system](https://github.com/uguryavuz/memsnap-verification).

### TLA⁺ Docs & Tooling Updates

- In the [TLA⁺ VS Code extension](https://github.com/tlaplus/vscode-tlaplus/), Younes fixed numerous UI & logic bugs in the TLC error trace view, when capturing parser output, and when cancelling out of the TLC options prompt.
  He also added go-to definition support for imported modules, cancellation functionality for TLA⁺ tools runs, and enforced parser validation before running the model-checker.
  Markus Kuppe improved integration with the MCP server and improved display of pre-comments in TLA⁺ definitions.
  Federico Ponzi also contributed a number of bugfixes.
  First-time contributor [tkuramoto33](https://github.com/tkuramoto33) improved PlusCal VS Code snippet support.
- The Java-based [core TLA⁺ tools](https://github.com/tlaplus/tlaplus) saw Markus Kuppe improve the SANY TLA⁺ parser's XML export functionality to better integrate with the VS Code extension, upgrade the Eclipse SDK version used by the TLA⁺ Toolbox, expanded error reporting & documentation, and added a state space exploration feature.
  Younes contributed refactorings of some custom model-checker dataclasses to make them more in line with their familiar counterparts in the Java standard library.
- In the [TLA⁺ Proof Manager](https://github.com/tlaplus/tlapm), 
- The [Apalache](https://github.com/apalache-mc/apalache) symbolic model-checker for TLA⁺ saw Igor Konnov continue development of a JSON RPC server for easier integration with non-JVM programs.
- Federico Ponzi released version 0.1.0 of his [TLA⁺ formatter](https://github.com/FedericoPonzi/tlaplus-formatter/releases/tag/v0.1.0), which uses the Java-based SANY parser.

### TLA⁺ Foundation-Funded Updates

Here are things [Andrew Helwer](https://ahelwer.ca/) (author of this post) worked on - all funded by the TLA⁺ Foundation!
- For my main task of transitioning [TLAPM](https://github.com/tlaplus/tlapm) to use SANY as its parser, I completed translation of the TLAPM syntax tree [into a standardized S-expression format](https://github.com/tlaplus/tlapm/pull/229) for comparison with an expected S-expression parse tree across a standardized set of TLA⁺ parse inputs.
  This ensures both SANY and TLAPM's parse trees can be dumped to the same S-expression format, cross-checking the forthcoming translation between them.
- For the [*Create your own TLA⁺ tools*](https://docs.tlapl.us/creating:start) how-to guide, I finished the chapter on [writing an actual breadth-first search TLA⁺ model-checker](https://docs.tlapl.us/creating:safety)!
  All that remains is a cleanup chapter on the surprisingly subtle method of evaluating operator arguments lazily so that TLA⁺ operators can work like macros expanding into parameter-free expressions.
- In the Java-based [core TLA⁺ tools](https://github.com/tlaplus/tlaplus), 

This past month also saw longtime TLAPM contributor [Karolis Petrauskas](https://github.com/kape1395) receive a TLA⁺ Foundation grant to work on [decomposing TLA⁺ proofs](https://github.com/tlaplus/tlapm/issues/205) in the VS Code extension, by implementing a new LSP code action.
