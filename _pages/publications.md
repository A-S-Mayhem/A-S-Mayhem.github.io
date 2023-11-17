---
layout: archive
title: "Research"
permalink: /publications/
author_profile: true
---

## :mag: Research Interests
My research interests lie within NLP and Information Retrieval. I like to study and work on building easy, scalable and efficient systems in the neural search paradigm. My long-term research ambition lies in building robust and generalizable retrieval models to help serve information better for everyone. Few of my notable works include developing the BEIR Benchmark [(Thakur et al., 2021)](https://openreview.net/forum?id=wCu6T5xFjeJ) and Augmented SBERT [(Thakur et al., 2021)](https://aclanthology.org/2021.naacl-main.28/). 

### :bar_chart: Data Efficiency: Transfer Learning, Data Augmentation and Zero-shot Learning 
In order to train neural retriever systems, large amounts of human-labeled training data is required which is often cumbersome and expensive to generate for real-world tasks. Data efficiency plays a crucial role to address this challenge. Transfer learning is motivated by distilling knowledge from pretrained models or LLMs to train data-efficient models. Data Augmentation techniques involve generating high-quality synthetic data for training purposes. Zero-shot learning enables models to generalize to unseen classes or queries without any training examples.

### :speaking_head: Languages: Multilingual Retrieval
Multilingual Retrieval aims to provide relevant search results for user searching across multiple languages. Multilingual retrieval involves various challenges, including language mismatch, translation ambiguity, and language-specific resource limitations. To overcome these challenges, machine translation, cross-lingual IR and mulitilingual embeddings have been employed. However, training data for such tasks is even more scarce than English making it a important challenge.

## :scroll: Publications
For an updated list of publications please refer either to my [Google Scholar profile](https://scholar.google.com/citations?user=CE9GJoMAAAAJ&hl=en) or [Semantic Scholar profile](https://www.semanticscholar.org/author/Nandan-Thakur/47583894). 

\* denotes equal contribution

<table style="width:100%;border:0px;border-spacing:0px;border-collapse:separate;margin-right:auto;margin-left:auto;">

  {% for post in site.publications reversed%}
  <tr>
    <td style="border: none; padding:2.5%;width:25%;vertical-align:middle;max-width:100px;max-height:100px">
      <img src="/{{post.image}}" alt="project image" style="width:auto; height:auto; max-width:100%;" />
    </td>
    <td style="border: none; padding:2.5%;width:75%;vertical-align:middle">
      <h3>{{post.title}}</h3>
      {{post.authors}}
      <em>{{post.venue}}</em>, {{ post.date | date: "%Y" }}.
      <br>
      {{post.affiliation}}
      <br>
        {% if post.paperurl %}
          <a href="{{post.paperurl}}">[paper]</a> /
        {% endif %}
        {% if post.page %}
          <a href="{{post.page}}">[website]</a> /
        {% endif %}
        {% if post.code %}
          <a href="{{post.code}}">[code]</a> /
        {% endif %}
        {% if post.video %}
          <a href="{{post.video}}">[video]</a> /
        {% endif %}
        {% if post.poster %}
          <a href="{{post.poster}}">[poster]</a> /
        {% endif %}
        {% if post.slides %}
          <a href="{{post.slides}}">[slides]</a> /
        {% endif %}
        {% if post.dataset %}
          <a href="{{post.dataset}}">[dataset]</a> /
        {% endif %}
      <p></p>
      {{ post.excerpt }}
    </td>
  </tr>
  {% endfor %}
</table>
