## Pharmacy

#### Pharmaceutics

How chemical entities are transferred to medication.

#### Pharmacokinetics

Pharmacokinetics studies how organisms process drugs.

  - **Absorption (A)**: how drugs get into the bloodstream

  - **Distribution (D)**: how drugs are reversibly transferred from one location to another within the body. some drugs tend to concentrate in part of the body like adipose tissue, raising potential risks for clinical usage.

  - **Metabolism (M)**: how drugs are broken down and modified inside the body.

  - **Excretion (E)**: how drugs and their metabolites (a metabolised form of drugs) are removed from the body.

  - **Toxicity (T)**: a pharmacodynamic property of drugs. Since its assessment protocol shares something similar with ADME, they are referred to as a whole in many cases.

#### Pharmacodynamics

Pharmacodynamics studies what a drug does to the body. Pharmacodynamics focus on the molecular, biochemical and physiological effects or actions of the studied drug.

#### Medicinal Chemistry

Medicinal chemistry refers to designing and synthesizing small molecules as a pharmaceutical agent.

  - **Hit-lead-candidate**: A hierarchical description to describe the potential precursor of a registered medication entity.

  - **Hit**: Promising candidates from preliminary screening, typically with a micro-molar EC50 (median effect concentration) values, or top scores from virtual screening.

  - **Lead**: Candidates demonstrating further potential to become drugs. Lead compounds normally require extensive modification and assessment before becoming a drug candidate.

  - **Drug candidate**: A well-studied compound, showing sufficient evidence in potency, selectivity, safety, and other drug-like properties. Drug candidates will become registered drugs after thorough clinical trials（usually including thousands of volunteers, tens of years, and investment in the order of billions of dollars)

#### Synthetic Route Design

Given a promising drug candidate, plan/design of the synthetic routine is performed to find more efficient processes with suitable starting materials to finally yield the product.

#### Retrosynthesis

Retrosynthesis is a recursion method to design a synthesis pathway for target organic molecules. The target is split into simpler precursors, and the precursor is split in the same manner until the building blocks are commercially available.

#### Bioisostere

Chemical substitutions or groups with similar physical or chemical properties to produce broadly similar biological effects. Bioisostere replacement from one compound to another is mainly applied in the situation where the parent compound is unsuitable for safe use, and/or bio-availability etc while possessing ideal druggability characteristics.

#### Reaction Output Prediction

Predict the product(s) with given reactants. There are reaction rules and preference reaction sites to be followed and studied in order to achieve this goal. Organic reactions are very dirty: a system can react in a different manner (e.g. substitution reaction & elimination reaction share very similar reagents and reaction condition), and at different sites (e.g. there can be two oxhydryls in one reagent, change the reaction condition can influence the preference during reaction.

#### Patent recognition/Literature information extraction

Collections of patent filings or literature contain a plethora of information that can guide drug development. On the other hand, novel compounds need to avoid violating existing intellectual property. Chemical patents are quite intricate, requiring sophisticated training and significant time to understand. Thus, automated information extraction via computer vision or natural language processing technology is quite necessary, although the evaluation would be a challenge.

#### Property Prediction for Ligands

A drug-like ligand requires favourable properties concerning pharmacokinetics issues (which means it can arrive the target properly) and pharmacodynamics issues (which means it can act with the target properly). These properties will be checked closely and separately below. However, medicinal chemists have come up with a few straight-forward and system-independent guidelines for drug design, to filter out risky molecules for downstream development. Below are some classic samples:

  - Lipinski rules of five (RO5) / bRO5: The most classic drug-like guideline. But these rules are being questioned all the time. See Rule of five in 2015 and beyond: Target and ligand structural limitations, ligand chemistry structure and drug discovery project decisions

  - Pan-assay interference compounds (Pan-assay interference compounds) Some molecules can always show a positive signal in high-throughput screening, but so far no one has successfully turned them into registered drugs. Such molecules share some intricate similarity, but how to describe them sharply remains a problem.

  - dosage form: the form drug is marketed for use. e.g. capsule, syrup, injection, etc

  - excipient: inactivate component in a drug product. The purpose of excipients may be to: make the drug stable, soluble, absorbable; change the absorption behavior(e.g. Controlled-release technique); some new excipients are suggested to change the distribution behavior of drug (like liposome).

  - pharmaceutical formulation design: choose the proper dosage form, find out the suitable combination of excipient and their ratio, decide the protocol of manufacturing

  - crystal structure of drugs: the arrangement of the molecules in a crystal. It can affect both physical and chemical (rare) properties of drug product.

#### Bioactivity

Bioactivity refers to the fraction (%) of an administered drug that reaches systemic circulation.

#### Druggability

If a protein is suitable to be a drug target. Studies on druggability don’t focus on ’determination of a good target’, but rather on ’how to filter out the unsuitable/difficult targets’. Two ’tangible’ sub-project in this topic: if a target can be modulated by small molecules (containing suitable pocket / covalent modification site / etc for molecule binding); if the inhibition / activation of a target can cause downstream (at least cellular-level) changes (rather than be antagonised and eliminated due to intracellular homeostasis)

#### Druggability Prediction for Receptors

Define whether certain kind of receptors could serve as a drug target that could be specifically addressed by a drug to take action for certain disease. It is also commonly to detect whether newly identified receptors could be targeted by existing drugs for re-orientated therapeutic purposes (under the circumstances of drug re-purposing/repositioning).

#### Pharmacophore

(according to IUPAC) an ensemble of steric and electronic features that is necessary to ensure the optimal supramolecular interactions with a specific biological target and to trigger (or block) its biological response. In short: when we perform a QSAR study, we consider a part of a molecule as a group, and describe it by it’s chemical property (charge, hydrophobicity, aromaticity, steric hindrance, etc). Such group will be ’scored’ and replaced as a whole.

#### Prediction of structure-activity relationship

structure-activity relationship (SAR) is the relationship between the structure and the biological activity. It tries to answer 2 question: 1.which parts in a bioactive compound / which combination between these parts matters (certain pharmacophore in a certain topology / geometry structure); 2.how to modify a molecule according to information gained above (infer a stronger pharmacophore / scaffold to replace the old one)

#### Molecule Generation

Design a new chemical entity satisfying all demands above (have ideal property, can be synthesised easily, haven’t been patented) is considered as the holy grail of drug discovery. Since the inference of the above properties is still underdeveloped, there is still a long way to go for this ambition. However, today’s development of generative chemistry models can also serve a practical role in settings like library generation (generate at least novel and ’drug-like’ molecule) and conditional design (generate molecule satisfying certain explicit constraint). For more information see in Generative Models for De Novo Drug Design.

#### Formulation Design

Design of the optimal form of drugs based on the effective compound. Further reading could be referred to: 1.State-of-the-Art Review of Artificial Neural Networks to Predict, Characterize and Optimize Pharmaceutical Formulation; 2.Crystal structures of drugs: advances in determination, prediction and engineering

#### Regenerative medicine

Regenerative medicine seeks the way to replace the damaged tissues or organs from disease, trauma, or congenital issues, in contrast to the traditional clinical ideas that focus only on alleviating or treating the symptoms.