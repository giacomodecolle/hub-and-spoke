### Domain

The domain is comprised of particulars that stand in the primitive instances of relation to universals at times. BFO’s hierarchy of universals can be represented by defining the relation:

    ∀x,t is_a(A,B)=def instance_of(x,A,t)→instance_of(x,B,t)

For example, material entity is a independent continuant.

By rigid universal Ur, we mean any entity that is instantiated by Ur, instantiates Ur for the whole of its existence. All classes in BFO are rigid other than the three subclasses of material entity: fiat object part, object, and object aggregate. For example, an instance of object aggregate at some time may later instantiate object.

### Mereology
BFO’s theory of parts is modeled after Minimal Extension Mereology (MEM). MEM is described in terms of binary part relations, but is extended to handle the time-indexed relations. The MEM axioms state that a part relation is reflexive, antisymmetric, transitive, weakly supplemented, and exhibits the unique product property. Any time-indexed relation implies that the first two relata exist, and holds at any time the relata exist. For instance, when a timeindexed relation is reflexive we mean that the self-relationship refers to the first two relata and it must hold at any time the relata exist.

<pre class="mermaid language-mermaid">
graph TD
    A(Entity) --> B(Continuant)
    A(Entity) --> C(Occurrent)
</pre>

BFO has two part of relations, one for continuants, called continuant part of and one for occurrents called occurrent part of. Continuant part of is time indexed, whereas occurrent part of is not. Worth noting is the treatment of the anti-symmetry of continuant part of applied to object aggregates. If a continuant part of b at some t and b continuant part of a at the same time t, we do not conclude that a=b.

Using these relations we can define irreflexive, asymmetric, transitive proper occurrent part of and proper continuant part of relations in the usual way.

### Continuants 

<pre class="mermaid language-mermaid">
graph TD
    B(Continuant) --> D(Specifically Dependent<br> Continuant)
    B(Continuant) --> E(Generically Dependent<br> Continuant)
    B(Continuant) --> F(Independent<br> Continuant)
    F(Independent<br> Continuant) --> G(Material Entity)
    F(Independent<br> Continuant) --> H(Immaterial<br> Entity)
</pre>

Starting at the continuant side of the BFO hierarchy, an independent continuant is distinguished from other continuants in that they neither generically nor specifically depend on other entities. In contrast, a specifically dependent continuant specifically depends on an independent continuant8 rigidly. If x specifically depends on y, then as long as x exists, the relation holds. If y ceases to exist, then x does as well.

<pre class="mermaid language-mermaid">
graph TD    
    H(Immaterial<br> Entity) --> O(Site)
    H(Immaterial<br> Entity) --> P(Spatial<br> Region)
    H(Immaterial<br> Entity) --> Q(Continuant Fiat<br> Boundary)
    Q(Continuant Fiat<br> Boundary) --> R(Fiat<br> Point)
    Q(Continuant Fiat<br> Boundary) --> S(Fiat<br> Surface)
    Q(Continuant Fiat<br> Boundary) --> T(Fiat<br> Line)
    P(Spatial<br> Region) --> U(One-Dimensional<br> Spatial Region)
    P(Spatial<br> Region) --> V(Two-Dimensional<br> Spatial Region)
    P(Spatial<br> Region) --> W(Three-Dimensional<br> Spatial Region)
</pre>

A specifically dependent continuant is said to inhere in – a relation defined in terms of specifically depends on – an instance of independent continuant. The inverse of inheres in is bearer of. A generically dependent continuant is concretized by a process or specifically dependent continuant. When the concretization is a specifically dependent continuant the generically dependent continuant generically depends on the specifically dependent continuant’s bearer.

<pre class="mermaid language-mermaid">
graph TD
    D(Specifically Dependent<br> Continuant) --> I(Quality)
    D(Specifically Dependent<br> Continuant) --> J(Realizable<br> Entity)
    I(Quality) --> K(Relational<br> Quality)
    J(Realizable<br> Entity) --> L(Role)
    J(Realizable<br> Entity) --> M(Disposition)
    M(Disposition) --> N(Function)
</pre>

All independent continuants other than spatial regions occupy a spatial region, and so are extended in space and time. Some may be located in others at some time, as the food you ingest is at some point located in the lumen of your stomach after you have eaten. Located in is transitive.

<pre class="mermaid language-mermaid">
graph TD
    G(Material<br> Entity) --> X(Fiat Object Part)
    G(Material<br> Entity) --> Y(Object<br> Aggregate)
    G(Material<br> Entity) --> Z(Object)
</pre>

A material entity can be continuant part of another material entity at some time. Material entities can have material and immaterial parts. An object can be member part of an object aggregate. Member part of is not transitive but implies continuant part of. An object aggregate always has at least one member, and must, at some time, have more than one.

### Occurrents

<pre class="mermaid language-mermaid">
graph TD
    C(Occurrent) --> AA(Process)
    C(Occurrent) --> AB(Process<br> Boundary)
    C(Occurrent) --> AC(Temporal<br> Region)
    C(Occurrent) --> AD(Spatiotemporal<br> Region)
    AA(Process) --> AE(History)
    AC(Temporal<br> Region) --> AF(Zero-Dimensional<br> Temporal Region)
    AC(Temporal<br> Region) --> AI(One-Dimensional<br> Temporal Region)
    AF(Zero-Dimensional<br> Temporal Region) --> AG(Temporal<br> Instant)
    AI(One-Dimensional<br> Temporal Region) --> AH(Temporal<br> Interval)
</pre>

Any independent continuant, specifically dependent continuant, or generically dependent continuant can participate in a process. In the latter two cases, it is implied that their bearer also participates in the process. When a process realizes a realizable entity, the realizable entity’s bearer also participates in the process. When a generically dependent continuant participates in a process p, some concretization of the generically dependent continuant participates in p. If that concretization is a process, it is temporal part of p.

A process occupies temporal region some temporal region. Processes have at least one process boundary as part. The temporal region that a process occupies must have as part a temporal interval. A process boundary can only occupy a temporal instant.
An occurrent can be a temporal part of some other. Occurrent parts can differ from what they are part of both spatially and temporally (e.g. the process which occurs in the left half of a soccer field during the first period of a game). By contrast, temporal part of an occurrent differs in that there is no difference in the spatial extent of the part and the whole.

Temporal regions provide the indices for all the time-indexed ternary relations in BFO. A temporal region has first instant and has last instant a temporal instant marking its extrema. A first or last instant can be temporal part of the region or not. A temporal instant that precedes the last instant of a temporal interval and are preceded by the interval’s first instant are necessarily part of the interval. Using these relations, the familiar and widely used Allen’s interval algebra may be formulated.