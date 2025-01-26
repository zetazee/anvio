# read recruitment glossary
read here means short pieces of dna, and recruitment here means matching similar short pieces together. it’s like you have a job (a genome), and people (reads) get recruited for it. so, if we have a genome and want to see if it, as a whole or in parts, exists in our sample, we use this technique.  

please visit [this video](https://www.youtube.com/watch?v=MqD4aN1p1qA) to fully grasp the idea.

before doing the [read recruitment exercise](https://zetazee.github.io/anvio/read_recruitment.html), here is a glossary that you might find useful:

<details>
  <summary>sequencing</summary>
  <p>Determining the precise order of nucleotides in a DNA or RNA.</p>
  <ul>
    <li>Sanger sequencing (first generation)</li>
    <li>Next generation sequencing (NGS)</li>
    <li>Third gen (Oxford Nanopore, PacBio SMRT)</li>
  </ul>
</details>

<details>
  <summary>reference sequence</summary>
  <ul>
    <li>A sequence that serves as the base for comparing and aligning other sequences.</li>
    <li>Anything that is longer than your shorts may serve as a reference.</li>
  </ul>
</details>

<details>
  <summary>metagenomes</summary>
  <ul>
    <li>Metagenomes are complete or partial genomes that have been gathered from an environment (for example, soil or water).</li>
    <li>They are then sequenced by a sequencing machine to be transferred into a computer.</li>
    <li>The so-called shift from <em>in vitro</em> to <em>in silico</em>.</li>
  </ul>
</details>


<details>
  <summary>short reads</summary>
  <ul>
    <li>DNA sequences generated during sequencing, ranging from 50 to 300 base pairs.</li>
    <li>They are produced by technologies like Illumina.</li>
    <li>Shorts can be long: you can recruit long reads with your reference sequence, too.</li>
  </ul>
</details>

<details>
  <summary>short reads generation</summary>
  <ol>
    <li>
      <strong>Fragmentation:</strong> Using physical, enzymatic, or chemical methods. 
      These produce fragments of varying size but within a specific range (200–500 base pairs).
    </li>
    <li>
      <strong>Size selection:</strong> Using electrophoresis and purification. 
      Fragments within the desired size range are enriched, while others are discarded.
    </li>
    <li>
      <strong>Adapter ligation:</strong> Short DNA sequences (adapters) are added to the ends of the fragments 
      to attach them to the sequencing platform.
    </li>
    <li>
      <strong>Sequencing by synthesis:</strong> Illumina sequences the fragments. 
      The length is defined by the number of cycles during sequencing.
    </li>
  </ol>
</details>

<details>
  <summary>contig</summary>
  <ul>
    <li>
      When sequencing generates <strong>many reads that overlap</strong>, it means that the sequencing machine produces multiple short fragments of DNA that represent the <strong>same regions of the original DNA sequence</strong>, often with overlapping sections. 
      <br><strong>What does this mean?</strong>
      <ul>
        <li>It means that one part of the DNA is being read several times by the machine.</li>
        <li>The parts that are repeated with high likelihood are accepted as correct bases (shorts).</li>
      </ul>
    </li>
    <li>
      These shorts are then put together to form a contig, which is longer. You can build a contig with or without a reference sequence.
    </li>
    <li>
      Software analyzes the reads to determine where the end of one read matches the start of another. This is how the shorts are assembled in order.
    </li>
  </ul>
</details>

<details>
  <summary>amplicon</summary>
  <ul>
    <li><strong>Amplify:</strong> To make large; <strong>-on:</strong> A suffix used in genetics to denote a unit or region.</li>
    <li>A piece of DNA that has been amplified (copied).</li>
    <li>Amplification is often done using PCR to copy those pieces.</li>
    <li>Amplicons are usually small, ranging from 100 to 500 base pairs.</li>
  </ul>
</details>

<details>
  <summary>metagenomic</summary>
  <p>Metagenomics is the study of genetic material recovered directly from environmental samples, bypassing the need to isolate and culture individual organisms.</p>
</details>

<details>
  <summary>single copy core genes</summary>
  <ul>
    <li>Genes that are typically found as a single copy in the genomes of organisms (bacteria, archaea, or eukaryotes).</li>
  </ul>
</details>

<details>
  <summary>MAG</summary>
  <ul>
    <li>
      Remember how we sliced the DNA into short reads to get it out of the cell? After extracting it, we try to rebuild it. A MAG is what we have rebuilt. 
      <br>(No, we are not crazy—the technological restrictions dictate this process for now.)
    </li>
    <li>
      Sometimes we can build the entire genome from the pieces, and other times it is incomplete. Both are called MAGs.
    </li>
    <li>
      MAG stands for <strong>Metagenome-Assembled Genome</strong>.
    </li>
  </ul>
</details>

<details>
  <summary>What is the purpose of read recruitment?</summary>
  <ul>
    <li>
      To investigate one or more reference sequences in the context of one or more samples, which we access through short reads.
    </li>
    <li>
      Your reference and short reads can represent any DNA or RNA sequences.
    </li>
  </ul>
</details>

<details>
  <summary>What can serve as a reference?</summary>
  <ul>
    <li><strong>Complete genomes</strong> (e.g., bacterial, viral, eukaryotic).</li>
    <li><strong>Draft genomes</strong> or <strong>contigs</strong> (incomplete assemblies from sequencing projects).</li>
    <li><strong>Individual genes</strong> or <strong>regions of interest</strong> (e.g., marker genes like 16S rRNA, functional genes).</li>
    <li><strong>Metagenome-assembled genomes (MAGs)</strong> from previous analyses.</li>
    <li>Even artificially constructed sequences or hypothetical references.</li>
  </ul>
</details>

<details>
  <summary>What can serve as short reads?</summary>
  <p><strong>Short reads are raw sequencing reads from your dataset.</strong> These are obtained by extracting and fragmenting DNA in vitro, sequencing them with a machine, and then analyzing the sequences in silico.</p>
  <ul>
    <li><strong>Metagenomic datasets:</strong> Sequences come from a mixed microbial community.</li>
    <li><strong>Transcriptomic datasets:</strong> Focus on RNA sequences (e.g., for gene expression studies).</li>
    <li><strong>Amplicon sequencing:</strong> Includes sequences like 16S or ITS reads for community profiling.</li>
    <li><strong>Whole-genome sequencing (WGS):</strong> Data for a specific organism.</li>
    <li>Even synthetic or simulated reads, depending on the purpose of the study.</li>
  </ul>
</details>

<details>
  <summary>Are amplicons connected or separated?</summary>
  <p>Amplicons can be connected or separated, depending on the context of the analysis:</p>
  <ul>
    <li><strong>Connected:</strong> In metagenomics, amplicons can overlap if they are multiple fragments.</li>
    <li><strong>Separated:</strong> In PCR or during sequencing and analysis. In Anvio, they are typically treated as separated unless you assemble them into contigs.</li>
  </ul>
</details>

<details>
  <summary>What is the difference: amplicons - reads?</summary>
  <p>
    The difference between amplicons and reads can be visualized in the following image:
  </p>
  <img src="read_recruitment/amplicon-read.png" alt="Amplicon vs Read">
</details>


<details>
  <summary> can you get amplicons from a read?</summary>

  We don’t usually produce amplicons from reads because reads are random fragments of DNA generated during sequencing. Amplicons, on the other hand, are specific DNA regions amplified during a PCR-based process, targeting a particular part of the genome (e.g., the 16S rRNA gene). Reads can, however, be used to reconstruct amplicons when they originate from sequencing targeted amplicons.
 </details>














