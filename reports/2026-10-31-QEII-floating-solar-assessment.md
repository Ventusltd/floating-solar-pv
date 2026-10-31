# Floating solar PV on the Queen Elizabeth II Reservoir: an assessment of the electrical design, earthing, fire record and the standards that govern it

Compiled: Saturday 31 October 2026, 02:15 UTC (Europe/London, GMT)

Status: study notes, critical in intent, without warranty of accuracy. Every factual claim below is tied to a source in the final section. Where something could not be verified it is said so.

## 1. Bottom line

The 6.3 MWp floating array on the Queen Elizabeth II (QEII) reservoir near Walton-on-Thames has run since March 2016 and was still being described in Parliament in June 2025 as supplying roughly a fifth of the adjacent treatment works' electricity. On the electrical fundamentals it is conventional: an unearthed (IT) DC array feeding inverters, with insulation and residual-current monitoring doing the protective work, exactly as every transformerless PV plant on land is built. Earthing the metalwork is a solved design problem under IEC 62548-1:2023; what water changes is the maintenance burden of proving the bonding is still continuous on a structure that never stops moving.

The genuine weakness is not the earthing. It is the combination of combustible HDPE floats, thousands of DC connectors and string cables crossing flexing raft-to-raft interfaces, and, in a 2016 design, almost certainly no arc-fault detection. On 26 May 2020 an electrical fault at a platform junction started a fire, floats and modules sank into a raw drinking-water reservoir, repairs waited roughly four months for approvals, and the cause was never published. The only clause in IEC 62548-1 that addresses DC arc fires recommends protection for building-integrated PV and says nothing about plastic rafts.

Verdict: floating PV is not a dumb technology and QEII is not a disaster as built, but the 2016 design would not pass a critical review today without arc-fault protection on every string, fire-rated cable management at every raft junction, a float specification that includes a reaction-to-fire rating, a documented earth-continuity test regime, and an incident-disclosure obligation. Ten gigawatts have been built worldwide before any of those became standard requirements, and the international standard meant to close the gap (IEC TS 63496) is a year late.

## 2. The installation

The array was built on the shore, pushed out onto the reservoir and fixed by 177 anchors placed by divers. It carries 23,046 modules on about 61,000 floats, covers roughly 57,000 m² (under 10 % of the 128 ha reservoir), and was designed to produce about 5.8 GWh a year. Construction cost was reported at £6.5 m against £9 m of developer funding; the output is sold under a private-wire power purchase agreement to the water company for the neighbouring treatment works, and the project was confirmed eligible for Renewables Obligation Certificates.

The float system is Ciel & Terre Hydrelio Classic, with the float supplier responsible for engineering of the floating plant and its anchoring. Main and secondary floats are UV-stabilised HDPE, connection pins are glass-fibre-reinforced polypropylene, and the module fixing rail is either aluminium or glass-reinforced polypropylene depending on configuration. Module tilt is 12°. At 6,338 kWp over 23,046 modules the modules are roughly 275 W each, which is consistent with 60-cell p-type product of 2016. Hydrelio is certified to BS 6920 for contact with drinking water. The reservoir itself dates from 1962, is about 18 m deep where the array sits, and its embankments were built from gravel dredged from the floor and compacted only by construction plant.

Mooring hardware on Hydrelio installations is shackled chain and cable onto aluminium spreader bars, with bottom or bank anchors. The electrical architecture used by the float supplier on comparable projects puts all wiring in reinforced conduit above the water line, runs strings to combiner boxes on the raft and brings a floating conduit ashore to inverters on land. Whether QEII used shore inverters or inverters on technical floats, and whether they were galvanically isolated, is not published; those are the first items to establish from the as-built drawings.

Specific yield works out at roughly 915 kWh/kWp, respectable for Surrey at 12° tilt and consistent with the cooling benefit offsetting the low tilt. Construction cost works out at roughly £1.03/Wp in 2016 money.

## 3. Operating record

Points in the array's favour: it has survived more than nine UK winters on first-generation HDPE floats, and a June 2025 Commons debate recorded that it has been feeding the treatment works continuously since 2016 and described it as supplying around 20 % of the site's electricity. The reservoir has long been a major gull roost (100,000 gulls were counted there in the winter of 1963) and more than 10,000 black-headed gulls took to roosting on the array, so a laser bird deterrent was installed to protect the modules from guano.

Against it: the fire of 26 May 2020, described in section 8, and the fact that the operator has never disclosed its cause.

## 4. Electrical architecture and the "water plus DC" question

The DC side of a modern string-inverter plant is an IT system: neither pole is intentionally earthed. That is not a floating-solar peculiarity; it is the normal and safer arrangement. A first insulation fault on an IT array produces no fault current, and the inverter's insulation-resistance measurement sees it and refuses to connect or raises an alarm. On an earthed DC array the first fault is itself the event, and the American experience of fuse-based ground-fault detection on earthed arrays, with its "blind spot" that led to the Bakersfield and Mount Holly fires, is the cautionary tale. Transformerless (non-isolated) inverters are likewise standard; the trade-off is that the DC circuit is referenced to the AC earth through the inverter, and the residual-current monitor is relied upon to detect running faults.

What water does change is the environment the insulation has to survive in. Field experience from the Singapore floating-PV test bed found cables dipping into water, abrasion from cable ties and metal guide plates, conduits admitting rainwater, and insulation resistance falling below inverter thresholds so that inverters started late or not at all. Laboratory work at the University of Évora found rubber-sheathed PV cable submerged in fresh or salt water showed accelerated insulation degradation after freezing temperatures, with copper then detectable in the water. Submersion is rarely designed in; it comes from low clearance, module-cable lengths that don't match the float pitch, and waves from wind or passing boats.

Insulation monitoring thresholds are the design lever. IEC 62548-1:2023 Table 2 sets only a floor (30 kΩ at 20 kW, falling to 1 kΩ above 500 kW) and recommends setting higher. For a 60 kW string inverter on QEII the floor would be 10 kΩ, which is far from conservative on a wet raft, so the set point is a design decision, not a code one.

## 5. Earthing and bonding under IEC 62548-1:2023

The standard contains nothing floating-specific. The word "float" appears only in Annex H for the anti-PID float controller; water appears as "wet locations" and in a note that cables which may be permanently submerged must be rated for it. What it provides is the method:

Clause 7.3.2.1 lists the four reasons to earth or bond parts of an array: functional earthing of conductive non-current-carrying parts so that leakage detection, insulation monitoring and residual-current detection work; earthing for lightning protection; equipotential bonding to avoid uneven potentials across an installation; and functional earthing of one DC pole where a separated inverter and module technology require it.

Clause 7.3.2.4.1 distinguishes main equipotential bonding (to the main earthing terminal) from supplementary equipotential bonding between simultaneously accessible exposed and extraneous conductive parts, whose purpose is to keep the voltage between them low enough to prevent shock. Frame bonding is to follow the decision tree in Figure 13: if the IEC 62305-2 risk assessment calls for lightning earthing, bond frames with a conductor sized to IEC 60364-5-54 and at least 16 mm²; if not, but the array maximum voltage exceeds DVC-A, bond with at least 6 mm²; only below DVC-A is there no requirement.

Clause 7.3.2.2 requires at least 4 mm² copper (or equivalent) for earthing the exposed metallic support structure, including cable trays, on separated systems. Clause 7.3.2.4.2 requires bonding conductors to be run as close as possible to the positive and negative conductors to reduce loop area and lightning-induced voltage. Clause 7.3.2.3 requires any separate electrode to be connected to the main earthing terminal by main equipotential bonding, with IEC 62305-3 for electrode design.

Clause 5.1.13 covers corrosion: corrosion-resistant mounting materials, anodised aluminium in marine or highly corrosive environments, and stand-off materials between galvanically dissimilar metals. Clause 5.1.14.2 requires that a connection between mechanically linked spans be designed to tolerate movement, especially when it is also part of the bonding path. On a raft, read wave movement for thermal movement.

Clause 6.4.1 classes arrays as functionally earthed, non-earth-referenced or non-separated, explicitly independently of frame earthing. Clause 6.4.3.2 requires insulation-resistance measurement by equipment compliant with IEC 63112 before start-up, continuously for non-earth-referenced arrays, with the Table 2 floors above. Clause 6.4.3.3 requires sudden-change residual-current detection for shock protection. Clause 6.4.3.4 sets the continuous fire-hazard residual-current limit at 300 mA up to 30 kW and the lesser of 5 A or 10 mA per kW above that, with a response within 0.3 s. Annex F (new in this edition) covers anti-PID equipment and arc flash; Annex H covers temporary functional earthing for PID mitigation. Amendment 1 was issued in December 2025.

Clause 6.3.2 is the gap that matters for floating plants: it recommends arc-fault protection equipment compliant with IEC 63027, or non-combustible materials near DC parts, for building-integrated PV, and leaves national committees to decide whether that becomes a requirement. Nothing in the standard asks for either measure on a combustible floating structure.

## 6. What happens when two frames sit at different potentials

In a healthy IT array every frame floats to an intermediate potential through leakage measured in megohms, and touching two frames does nothing. If all frames are bonded together and to the shore earth, they are by definition at one potential, the same potential as the water, and a single insulation fault pulls the whole bonded network to the faulted point in the string. Nobody feels anything because everything touchable moved together; the insulation monitor sees the array is no longer floating relative to earth and trips or alarms. One fault, detected, harmless.

Remove the bond, which is what a plastic structure does unless it is deliberately restored, and the picture inverts. A faulted frame sits at string potential and nothing notices, because the inverter measures insulation to earth and an isolated frame is not earth. The hazard is the second contact: a technician bridging that frame to a bonded one, a second fault elsewhere in the string, or the water. On a 1,000 V class string two frames can then sit several hundred volts apart with a low-impedance source behind them and full string current available, which is lethal through a body and sustains a DC arc through a tool or tray. That is the sense in which frames at different potentials are dangerous: an unbonded raft turns every first fault into an invisible, armed one.

The design answer is to make the whole raft and the water one equipotential zone, the same logic as supplementary bonding around a swimming pool. The floating-specific risk is that the bond is a chain of conductors across thousands of joints that flex every day; a single broken jumper silently recreates the unbonded case for one row. Periodic earth-continuity testing therefore matters more on water than on anything on land.

## 7. Floating-specific hazards

Bonding continuity. The World Bank/SERIS handbook notes that constant motion can loosen or snap bonding conductors and that many float designs need separate equipotential bonding wires. IEA PVPS O&M guidance for floating plants lists regular checking of earthing resistance alongside cable-slack checks and inspection of cables in or near the water.

Cable and connector insulation. See section 4. This is the dominant real-world electrical failure on floating plants and the most likely initiator of the fires described below. TÜV Rheinland's 2PfG 2750 standard for water-resistant PV DC cable was created in response.

Stray DC and corrosion. The water, moorings and anchors form an uncontrolled parallel earth path. A grounding specialist quoted in Brazilian trade coverage describes in-water earthing as effectively formed by the anchoring, with natural potential differences between the interconnected metals adding to those from earthing in media of different resistivity. Research from the University of Cyprus argues that leakage-current thresholds in PV earth-fault detection were set for fire and personnel safety and leave stray-current corrosion blind spots on bonded metalwork and nearby infrastructure. On QEII that is galvanised chain, shackles and aluminium spreader bars.

Lightning. Bonding conductors from the far corner of a 57,000 m² raft to the shore electrode are hundreds of metres long; IEC 62548-1 pushes the designer to IEC 62305 and surge protective devices at both ends.

Structure, fatigue and wave loading. The float supplier's own O&M guidance puts floats and their fastenings first, because they must withstand fatigue and dynamic loading from water motion. An Istanbul Technical University field study found wave-induced warpage of floating elements the most serious failure mode and rigid fittings unsuitable; its design principle is that the system as a whole must be flexible while individual units stay stable.

HDPE and arc faults. The floats are plain UV-stabilised HDPE qualified for wind (210 km/h), UV (up to 30 years), snow, water-level variation and drinking-water contact; no reaction-to-fire rating or flame-retardant grade could be found in the supplier's published material. HDPE is combustible and melts and drips; flame-retarded grades exist but none is offered for floating PV as far as can be found, and any additive package would need re-approval for potable-water contact. The research literature notes that floating PV modules and structures contribute to fire development through their own combustibility. The practical consequence is that the structure is simultaneously the fuel and the buoyancy, sitting under live DC, with no standard requiring arc-fault detection above it.

## 8. The QEII fire, 26 May 2020

According to trade press reports published in September 2020 and the operator's own statement, an electrical fault occurred on the array on 26 May 2020 and a small fire followed, damaging components. The fire occurred where two floating platforms met and some modules apparently sank. The water company confirmed the reservoir holds pre-treatment water and that quality tests were carried out. Repairs were due to start in late September 2020, about four months after the event, following the operator's internal HSSE investigation and the water company's approvals. The operator did not comment on the cause, and no root-cause finding has been published since. It was the second fire at a major floating solar plant within a year.

Reading the incident against the sections above: a platform junction is precisely where string cables cross between independently moving rafts and where connectors, jumpers and cable slack take the movement; the fault became a fire rather than a shock, consistent with the hazard ranking in this report; and the consequence chain on water was worse than it would have been on land, because the burning floats took the buoyancy with them and put modules and copper on the bed of a drinking-water store. The absence of any published cause means the industry learned nothing from it in public.

## 9. Other floating PV incidents

Kawashima, Japan, 2016: typhoon damage to modules and racking on a floating plant; cited in incident reviews as a lesson for edge zones and rack connections.

Yamakura Dam, Chiba, Japan, 9 September 2019: Typhoon Faxai struck the 13.7 MW, 50,904-module floating plant commissioned in March 2018. The outermost row tore away, the wind-facing edge lost its ballast against uplift, modules and floats curled up and stacked, and the resulting contact and heat started an electrical fire involving around 50 modules; thick black smoke was reported and the fire was extinguished the same afternoon with no injuries. METI opened a formal investigation into the failure mode, and the plant was later rebuilt with smaller floating islands to reduce structural stress.

Shintaku Tameike, Kyushu, Japan, late September 2019: a second typhoon two weeks after Faxai destroyed a 2.4 MW floating installation.

Queen Elizabeth II Reservoir, UK, 26 May 2020: see section 8.

O'MEGA 1, Piolenc, France, 30 January 2022: a fire broke out on the 17 MW floating plant (inaugurated October 2019) during a storm. The operator presented its first internal conclusions a month later; the recovery effort centred on re-supplying and resizing the plant's cabling rather than changing the floating technology.

Banja reservoir, Albania: a 0.5 MWp membrane-type floating unit, the first stage of a 2 MWp project, was damaged and partly submerged; the supplier's root-cause analysis attributed it to wind above the design criteria. Not a fire, but a structural failure with the same recovery problems.

Lunwei East District, Changhua, Taiwan, 6 November 2025: a cable fire broke out in a section of the 192 MW floating park, confined to the floating platform area; the operator attributed it to a short circuit in a cable.

Otake, Narita, Japan, September 2026: not floating, but directly relevant to PV and water. A ground-mounted plant caught fire after typhoon floodwater submerged its combiner boxes; firefighters held back because of electrocution risk, and METI repeated its warnings that submerged PV equipment remains energised and can cause electrocution or fire after water recedes.

Incident reviews of these events converge on the same themes: storm damage, platform movement, floating debris, partial submersion, fire exposure and difficult post-event recovery; and the observation that being surrounded by water does not remove fire load.

## 10. Land-based PV fires that shaped today's protection rules

Bürstadt, Germany, 2009: a large rooftop plant fire; independent experts attributed it to faulty connections inside modules causing hot spots, while the module supplier blamed roof clamps pressing on module insulation. The dispute is an early example of how rarely PV fire causes are settled publicly.

Bakersfield, California, 5 April 2009 and Mount Holly, North Carolina, 16 April 2011: fires on earthed rooftop arrays of 383 kW and about 1.2 MW. In Bakersfield an initial small ground fault on a string conductor, invisible to the fuse-based ground-fault detector, became the return path for a second large fault when an output-cable joint separated, melting the conductor insulation and igniting the array. The Solar America Board for Codes and Standards work that followed identified the ground-fault detection "blind spot", and Sandia and DNV GL studies evaluated insulation-resistance monitoring and residual-current detection as alternatives. These events drove the shift to IT arrays with Riso and RCD monitoring and the arc-fault detection requirements in the US code.

United Kingdom: the BRE National Solar Centre investigation "Fire and Solar PV Systems – Investigations & Evidence" (2017) for the UK government catalogued PV fire incidents, components implicated and root causes, and found that previously there had been no detailed follow-up investigation of most PV fires.

Wellington North, New South Wales, December 2025: a grass fire at a 400 MW ground-mounted plant during lightning and extreme heat took the site partly offline; included here as a reminder that on land the fire risk is vegetation and surroundings, whereas on water it is the structure itself.

## 11. Standards and guidance

IEC 62548-1:2023 (with Amendment 1, December 2025): the base design standard for PV arrays, summarised in section 5. Nothing floating-specific.

IEC 63112:2021: earth-fault protection equipment for PV arrays, the referenced product standard for insulation-resistance and residual-current monitoring.

IEC 63027:2023: DC arc detection and interruption in PV systems, the referenced product standard for arc-fault protection equipment.

IEC 62305 series: lightning risk assessment and protection, referenced for the frame-earthing decision tree.

IEC TS 62738:2018: design guidelines for ground-mounted PV power plants, including equipotential bonding over large areas; being replaced by IEC TS 62548-2, which reached committee draft in May 2025 with publication forecast for February 2026 and still shown as in development.

IEC TS 63496 ED1, Floating photovoltaic power plants – Design guidelines and recommendations: the project that grew out of new work item 82/2106/NP, in TC 82 Working Group 3. The proposal explicitly listed earthing over water, insulation-resistance measurement, cable and connector selection, cable routing, location of inverters and transformers, mooring and anchoring, and equipotential bonding over large areas as reported field problems, and named Singapore's TR 100:2022 as the starting text. Committee draft registered June 2023; publication was forecast for November 2025 and had not occurred by the end of October 2026.

IEC TS 63618 ED1: HDPE floating bodies for floating PV systems, committee draft December 2024. PNW TS 82-2326 ED1: guidelines for qualifying PV modules for operation on floating platforms (humidity, wave motion, thermal shock, fouling, corrosion, wind on open water), at new-work-proposal stage. UK input to all TC 82 work goes through BSI committee GEL/82.

Singapore TR 100:2022: Floating photovoltaic power plants – design guidelines and recommendations; currently the most complete published design text for floating plants.

DNV-RP-0584, Design, development and operation of floating solar photovoltaic systems: first issued March 2021 from a 24-member joint industry project, updated edition dated September 2026, scoped to sheltered inland and near-shore waters with significant wave heights up to 2 to 3 m. DNV-ST-C108 (structural design of floats, including safety classification, material qualification, testing, corrosion and UV degradation of non-metallic materials) and DNV-ST-E309 (station keeping and mooring) were published in May 2026 and reposition the RP as system-level guidance.

NEC 2023 section 690.4(F): US requirement that floating PV equipment be identified as suitable for the purpose.

World Bank / ESMAP / SERIS, Where Sun Meets Water: Floating Solar Handbook for Practitioners (2019): sections on cable management on water, electrical safety, surge and lightning protection and DC system commissioning, drawing on the 1 MWp Tengeh reservoir test bed.

IEA PVPS Task 13 report T13-31:2025, Floating Photovoltaic Power Plants: A Review of Energy Yield, Reliability, and Maintenance (April 2025), with a summary fact sheet in January 2026: concludes existing guidelines lack quantitative guidance for yield and reliability, that there is no complete model for wave-induced losses, and presents a failure-mode and effects analysis for floating-plant O&M.

IFC Environmental, Health and Safety Guidelines for Solar Power, draft for consultation July 2026: now covers floating PV explicitly, including siting against water-level variation, debris and extreme weather, ingress-protected enclosures in wet environments, and the connection from the floating array to shore.

TÜV Rheinland 2PfG 2750 (2021): test standard for water-resistant PV DC cable for floating applications.

## 12. What the working groups and policymakers did in 2026

IEC TC 82 WG 3: IEC TS 63496 remained unpublished a year past forecast; IEC TS 62548-2 likewise; IEC TS 63618 and PNW TS 82-2326 progressed at proposal and committee-draft stages.

DNV: published DNV-ST-C108 and DNV-ST-E309 in May 2026 and the 2026-09 edition of DNV-RP-0584, making it the freshest published floating-specific reference.

IEA PVPS Task 13: disseminated its 2025 floating-PV report through a January 2026 fact sheet and a February 2026 Chinese translation.

IFC: opened consultation in July 2026 on solar EHS guidelines that include floating PV for the first time.

United Kingdom: the June 2025 Solar Roadmap committed to exploring floating solar and reviewing its treatment in the Contracts for Difference scheme and planning, with further permitted-development reform; a Solar Council succeeded the Solar Taskforce. A Commons Library briefing of 1 April 2026 noted a February 2026 government-commissioned report recommending early public and private investment and policy support. On 30 April 2026 the Energy Secretary announced a public consultation to fast-track floating solar on reservoirs and lakes, alongside CBI Economics modelling for an investor that put inland potential at up to 58.6 GW by 2050; national parks are expected to be treated as inappropriate locations. The consultation document itself could not be located at the time of writing. Pipeline examples include market engagement in February and March 2026 for a roughly 32 MW floating array at Cavendish Dock, Barrow-in-Furness, with works pencilled for August 2026 to July 2027, and floating solar within the proposals for a new Thames Valley reservoir.

Research: a 2026 review in Nature Reviews Clean Technology from the Singapore floating-PV research group put global floating capacity above 10 GWp in 2025 and still has to cite the IEC new work item rather than a published floating-PV standard.

## 13. Operations: birds, cleaning, people

Soiling on QEII is dominated by gulls. Bird droppings are among the most aggressive forms of soiling, sit in hard lumps over a few cells rather than spreading thinly, and promote lichen growth because they are rich in nitrogen; IEA PVPS O&M guidance recommends aerial infrared and visual imaging to find and mitigate hot spots caused by droppings, which makes guano a thermal and degradation issue as well as a yield one. Cleaning on a drinking-water source is restricted to water and soft brushes from the walkable secondary floats or a boat; the float supplier has since developed cleaning robots using soft brushes or demineralised water without chemicals. The 12° tilt gives poor rain self-cleaning. The deterrent-first approach (the laser system) is the cheaper lever.

Health and safety is the dominant personnel risk and the literature says so plainly: work takes place over deep cold water on a moving, guano-slick surface, cleaning crews stand on unbalanced floats, live DC cannot be switched off at source, connectors are wet, access is by boat, the 177 anchors required a dive operation, and the launch was from a 1960s gravel embankment. Drinking-water hygiene rules add constraints on fuels, materials and access. The O&M literature notes the absence of global safety standards for floating-plant maintenance.

## 14. Assessment and recommendations

Floating DC (IT) and non-isolated inverters: keep. They are the safer choices and are what the standards expect; set insulation thresholds well above the IEC floors and use distributed residual-current monitoring to keep detection sensitive on a 6 MW array.

Earthing and bonding: solved on paper by IEC 62548-1 Clause 7.3.2 and Figure 13; on water it becomes a maintenance discipline. Specify bonding to the 6 mm² (or 16 mm² lightning) branch, flexible jumpers at every articulation, corrosion-resistant lugs and fixings, and an earth-continuity test regime with intervals and acceptance values written into the O&M contract. Decide explicitly whether mooring hardware is bonded, and monitor it for stray-current corrosion either way.

Cables and connectors: specify cable to a water-resistant standard, enforce clearance from the water line, design slack for the full range of raft movement, ban metal-edged fasteners, and inspect junctions on a fixed schedule.

Fire: treat arc-fault protection to IEC 63027 on every string as mandatory regardless of what IEC 62548-1 says, require fire-rated cable management at raft-to-raft interfaces, and write a reaction-to-fire requirement into the float specification. Where potable-water approval and flame retardancy conflict, that conflict should be resolved by the float supplier and the water regulator, not left silent.

Disclosure: incidents on water-utility assets should carry a public root-cause reporting obligation. The 2020 QEII fire shows what happens otherwise.

Standards: until IEC TS 63496 is published, use DNV-RP-0584 (2026-09) and TR 100:2022 as the floating-specific references over IEC 62548-1 alone.

## 15. Open questions specific to QEII

Whether inverters were on shore or on technical floats, and whether they were galvanically isolated with a functionally earthed negative for PID mitigation on 2016 p-type modules. The actual insulation-resistance set points and any history of nuisance tripping or late starts after wet winters. Whether frames are bonded through aluminium rails or individually lugged, and when continuity was last tested across the raft. Whether any arc-fault detection has been retrofitted since 2020. The root cause of the 26 May 2020 fire, the extent of module loss to the reservoir bed, and what was recovered. Whether mooring hardware is bonded and what its corrosion condition is after a decade.

## 16. Sources

Project and operating record

Lightsource bp project page: https://lightsourcebp.com/uk/project/queen-elizabeth-ii-reservoir-solar/

Lightsource 2016 construction announcement: https://lightsourcebp.com/uk/news/lightsource-begins-work-on-europes-largest-floating-solar-project

PV Tech, February 2016, construction begins: https://www.pv-tech.org/lightsource-building-largest-floating-pv-project-in-europe/

pv magazine, February 2016: https://www.pv-magazine.com/lightsource-begins-work-on-europes-largest-floating-pv-array-in-london

Ennoviga Solar project reference (private wire, ROC eligibility): https://www.ennovigasolar.com/projects-1/

Ciel & Terre project listing (Hydrelio Classic, 6,338 kWp, scope): https://ciel-et-terre.net/fr/project/page/7

Pager Power project note (depth, anchors, launch): https://www.pagerpower.com/news/europes-largest-floating-solar-farm-sets-sail/

Reservoir history and gull roost: https://en.wikipedia.org/wiki/Queen_Elizabeth_II_Reservoir

Hansard, Floating Solar Panels debate, 26 June 2025: https://hansard.parliament.uk/commons/2025-06-26/debates/5EC14FEA-B51C-4867-9766-56747BFEF0D5/FloatingSolarPanels

Laser bird deterrent at QEII: https://www.solarplaza.com/resource/11730/solving-problem-bird-soiling-pv-plants/

Hydrelio system and electrical architecture overview: https://energyresearch.ucf.edu/floating-pv-overview-fsec

Hydrelio component materials and anchoring: https://repository.officiele-overheidspublicaties.nl/externebijlagen/exb-2019-13191/currentItem

Hydrelio qualification claims (wind, UV, waves): https://ciel-et-terre.net/?p=32188

Hydrelio BS 6920 drinking-water certification: https://taiyangnews.info/technology/ciel-et-terre-global-expansion-in-floating-pv-technology

Hydrelio drinking-water test briefing (materials in water contact): https://www.monroevilleohio.com/pics/Monroeville_FPV_Briefing_Combined.pdf

Hydrelio anchoring hardware: https://www.energy-xprt.com/products/floating-solar-pv-anchoring-system-229953

Floating PV fires and failures

Recharge, September 2020, fire at the QEII array: https://www.rechargenews.com/transition/fire-hits-bp-ventures-flagship-floating-solar-plant-in-uk/2-1-877293

ISSSource, fire hits UK floating solar plant: https://www.isssource.com/fire-hits-uk-floating-solar-plant/

Gramwzielone (Polish trade press) on the QEII fire and undisclosed cause: https://www.gramwzielone.pl/?p=103925

Xinhua, 9 September 2019, Yamakura Dam fire: http://www.xinhuanet.com/english/2019-09/09/c_138378230.htm

Energy Incident Register, Yamakura Dam (EIR-0986): https://energyincidentregister.com/incident/eir-0986/

pv magazine, February 2020, Yamakura failure mode and METI investigation: https://www.pv-magazine.com/2020/02/10/dont-throw-caution-to-the-wind/

Green Building Africa, Yamakura fire after Typhoon Faxai: https://www.greenbuildingafrica.co.za/japan-floating-pv-plant-catches-fire-after-typhoon-faxai-impact/

VOA, floating solar overview including Yamakura: https://www.voanews.com/a/something-new-under-the-sun-floating-solar-panels-/6794529.html

Arizona Solar Center note on Yamakura and Shintaku Tameike: https://azsolarcenter.org/japan-s-largest-floating-pv-plant-catches-fire

pv magazine, 1 March 2022, O'MEGA 1 Piolenc fire: https://www.pv-magazine.com/2022/03/01/akuo-speaks-out-on-recent-fire-accident-at-its-17mw-floating-pv-plant-in-france/

Offshore Energy, Banja reservoir unit failure root cause: https://offshore-energy.biz/?p=477236

Exit News, Albania floating plant sinks: https://exit.al/en/?p=149408

pv magazine, 6 November 2025, Lunwei East cable fire: https://www.pv-magazine.com/2025/11/06/short-circuit-in-cable-causes-fire-at-taiwanese-floating-pv-plant

PVTime, Lunwei East cable fire: https://www.pvtime.org/?p=24343

pv magazine, 5 October 2026, flooded plant fire at Narita and METI warnings: https://www.pv-magazine.com/2026/10/05/flooded-solar-plant-in-japan-catches-fire-after-typhoon/

TheNavalArch, When Floating PV Fails (incident review incl. Kawashima 2016): https://thenavalarch.com/when-floating-pv-fails/

Land-based PV fires and protection history

Sandia / Solar ABCs ground-fault blind spot study (SAND report): https://www.osti.gov/servlets/purl/1313068

Sandia and DNV GL, Riso and RCD alternatives to ground-fault fuses: https://www.osti.gov/servlets/purl/1313071

pv magazine, 2013, cables as culprits at Bakersfield and Mount Holly: https://www.pv-magazine.com/2013/05/03/cable-care_100011160/

Fluke, DC ground faults and the Bakersfield case study: https://www.fluke.com/en-id/learn/blog/grounding/dc-ground-faults-pv-systems

Review of catastrophic faults in PV arrays (Bakersfield and Mount Holly dates): https://sindex.sdl.edu.sa/esploro/outputs/journalArticle/A-Comprehensive-Review-of-Catastrophic-Faults/9922422108331

EE Times, 2009, Bürstadt fire dispute: https://www.eetimes.com/?p=1254420

BRE National Solar Centre, Fire and Solar PV Systems – Investigations & Evidence (UK government): https://assets.publishing.service.gov.uk/media/5a81d3c340f0b62302699602/fire-solar-pv-systems-investigations-evidence.pdf

Wellington North grass fire, December 2025: https://ground.news/article/wellington-north-solar-farm-offline-in-st-pasa-data-from-saturday-6th-december-2025-following-grassfire

PV Tech, root-cause analysis of PV plant fires: https://www.pv-tech.org/mitigating-fire-risks-in-solar-power-plants-a-comprehensive-root-cause-analysis

Standards and guidance

IEC 62548-1:2023: https://webstore.iec.ch/publication/64171

IEC 62548-1:2023+AMD1:2025 consolidated: https://webstore.iec.ch/en/publication/110893

IEC 63112:2021 earth-fault protection equipment: https://webstore.iec.ch/publication/59647

IEC 63027:2023 DC arc detection and interruption: https://webstore.iec.ch/en/publication/27362

IEC new work item 82/2106/NP floating PV power plants (BSI page): https://standardsdevelopment.bsigroup.com/projects/9023-08033

IEC TS 63496 ED1 project status: https://genorma.com/en/standards/iec-ts-63496-ed1

IEC TS 62548-2 ED1 project status: https://genorma.com/en/standards/iec-ts-62548-2-ed1

IEC TS 62738:2018 scope: https://standards.globalspec.com/std/13055804/iec-ts-62738

IEC TS 63618 ED1 HDPE floating body: https://iss.rs/en/project/show/iec:proj:128819

PNW TS 82-2326 ED1 modules for floating platforms (BSI page): https://standardsdevelopment.bsigroup.com/projects/9024-11282

BSI GEL/82 committee: https://standardsdevelopment.bsigroup.com/committees/50001566

JRC, Standards for Photovoltaic Energy Systems (TC 82 project tracker): https://www.researchgate.net/publication/387995236_Standards_for_Photovoltaic_Energy_Systems

DNV-RP-0584 (edition 2026-09): https://www.dnv.com/energy/standards-guidelines/dnv-rp-0584-design-development-and-operation-of-floating-solar-photovoltaic-systems/

DNV 2021 launch of the recommended practice: https://www.dnv.com/news/2021/dnv-publishes-world-s-first-recommended-practice-for-floating-solar-power-plants-199138/

DNV May 2026 launch of DNV-ST-C108 and DNV-ST-E309: https://www.dnv.com/news/2026/dnv-launches-coordinated-standards-to-improve-safety-and-reliability-of-floating-solar/

pv Europe on the DNV standards: https://www.pveurope.eu/mounting/dnv-sets-technical-baseline-floating-solar-sector-matures

Singapore TR 100:2022: https://www.singaporestandardseshop.sg/Product/SSPdtDetail/a2b5734e-1f94-4bfd-91db-fb3e59fec053

NEC 2023 690.4 including 690.4(F) floating PV: https://www.solarpermitsolutions.com/blog/nec-690-4-solar-pv-general-requirements

World Bank, Where Sun Meets Water handbook: https://openknowledge.worldbank.org/handle/10986/32804

Handbook PDF (SERIS mirror): https://www.seris.nus.edu.sg/wp-content/uploads/2023/09/ESMAP_FloatingSolar_Gde_A4-WEBL-REV2.pdf

IEA PVPS Task 13 report T13-31:2025: https://iea-pvps.org/key-topics/t13-floating-pv-plants-review-2025/

IEA PVPS Task 13 report PDF: https://iea-pvps.org/wp-content/uploads/2025/04/IEA-PVPS-T13-31-2025-REPORT-Floating-PV-Plants.pdf

IEA PVPS Task 13 floating PV fact sheet, January 2026: https://iea-pvps.org/fact-sheets/fact-sheet-floating-photovoltaic-power-plants/

PV Tech on the IEA PVPS report: https://pv-tech.org/technical-knowledge-gaps-slowing-floating-pv-adoption-iea-pvps

IFC Solar Power EHS Guidelines, draft for consultation July 2026: https://www.ifc.org/content/dam/ifc/doc/2026/2026-consultation-draft-solar-power-ehs-guidelines-en.pdf

SERIS webinar slides, five years of the Tengeh test bed: https://www.pv-magazine.com/wp-content/uploads/2021/04/02_pv-magazine-Webinar_Presentation-by-SERIS.pdf

pv magazine webinar page, TÜV 2PfG 2750 floating PV cable standard: https://www.pv-magazine.com/webinars/waterproofed-new-cable-testing-standard-for-fpv/

TÜV Rheinland floating PV certification: https://www.tuv.com/world/en/floating-pv-certification.html

PV Tech Power, floating PV design considerations (2019): https://www.pv-tech.org/technical-papers/floating-pv-systems-an-overview-of-design-considerations/

PV Tech Power, floating PV BOS component challenges (2022): https://www.pv-tech.org/technical-papers/challenges-and-experiences-of-floating-pv-and-bos-components/

Research

Cable submersion testing, Open Research Europe 2024 (record): https://zenodo.org/records/10149038

Cable submersion testing, University of Évora repository: https://rdpc.uevora.pt/handle/10174/38821

DC leakage and faults in floating (IT) PV systems, IEEE PowerTech 2017 (University of Cyprus): https://gnosis.library.ucy.ac.cy/handle/7/43294

Stray-current DC corrosion blind spots, IEEE Transactions on Power Delivery 2018: https://gnosis.library.ucy.ac.cy/handle/7/63428

PVrosion project overview, IET 2021: https://digital-library.theiet.org/content/conferences/10.1049/icp.2021.1230

Problems encountered with floating PV under real conditions (Istanbul Technical University, 2021): https://research.itu.edu.tr/en/publications/problems-encountered-with-floating-photovoltaic-systems-under-rea/

Earthing of floating solar systems formed by anchoring (Canal Solar): https://canalsolar.com.br/en/saiba-como-funciona-o-terramento-de-sistemas-solares-flutuantes

Fire hazards of floating PV in the literature (Frontiers in Marine Science, 2024): https://www.frontiersin.org/journals/marine-science/articles/10.3389/fmars.2024.1413678/full

HDPE thermal degradation and PV module flammability (cone calorimetry): https://www.researchgate.net/publication/281736927_Experimental_Studies_on_the_Flammability_and_Fire_Hazards_of_Photovoltaic_Modules

Design and implementation of floating photovoltaics, Nature Reviews Clean Technology 2026 (reprint): https://now.solar/2026/05/30/design-and-implementation-of-floating-photovoltaics-nature/

Ciel & Terre on floating-plant O&M: https://ciel-et-terre.net/how-approach-maintenance-and-operation-floating-solar-plants

Ciel & Terre on cleaning floating panels: https://ciel-et-terre.net/ciel-terre-emea-develops-solutions-for-efficient-cleaning-of-floating-solar-panels

Renewable Watch, O&M safety challenges in floating PV: https://renewablewatch.in/2023/03/28/safety-first-om-challenges-in-floating-pv-systems/

Bird droppings and floating PV performance (Korea, 2025): https://www.koreascience.kr/article/JAKO202505054137627.page?&lang=en

UK policy 2025–2026

DESNZ Solar Roadmap, June 2025: https://assets.publishing.service.gov.uk/media/685d6e483e6b7941f4e00afb/35.87_DESNZ_UK_Solar_Roadmap_final.pdf

Commentary on the Roadmap's floating-solar permitted-development commitment: https://www.turley.co.uk/comment/solar-roadmap-lighting-way-clean-energy-2030

House of Commons Library briefing CBP-10610, Alternatives to ground mounted solar, 1 April 2026: https://researchbriefings.files.parliament.uk/documents/CBP-10610/CBP-10610.pdf

CBI Economics report on floating solar for an investor, April 2026: https://thebluefieldgroup.com/wp-content/uploads/2026/04/280426-CBI-Economics-Report-on-Floating-Solar.pdf

Coverage of the 30 April 2026 consultation announcement: https://www.yahoo.com/news/articles/labour-plans-blanket-lakes-floating-070000673.html

Further coverage with US comparison: https://www.autonocion.com/us/britain-solar-panels-lakes-us/

Solar Power Portal, UK solar outlook for 2026 (Solar Council): https://www.solarpowerportal.co.uk/energy-policy/uk-solar-progress-and-outlook-for-2026

Find a Tender, Barrow EnergyDock floating solar market engagement: https://www.find-tender.service.gov.uk/Notice/010686-2026/PDF
