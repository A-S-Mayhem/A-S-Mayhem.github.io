---
title: "REHAB-AVQ"
fullname: "REHABilitation des Activités de la Vie Quotidienne"
collection: projects
link: rehabavq
excerpt: "Le projet Rehab-AVQ vise à développer un système basé sur la réalité virtuelle pour réentraîner des personnes atteintes de la maladie d'Azheimer à réaliser des activités en cuisine."
begin: 2011-01-01
end: 2013-01-01
context: "Afin de retarder le plus longtemps possible la perte d’autonomie associée à la maladie d’Alzheimer et pour en réduire l’impact socioéconomique (dépendance aux proches, voisins ou services médicosociaux), les recommandations s’accordent toutes sur l’urgence de développer des techniques spécifiquement adaptées à la maladie. Généralement, elles préconisent que les personnes restent actives et pratiquent des activités de leur choix. Dans le cas d'apprentissages complexes, les méthodes de réductions d’erreurs semblent particulièrement prometteuses. Malheureusement, les observations restent anecdotiques. De plus, les risques que présentent certaines activités pour ces patients vulnérables (p. ex., coupures, brulures), l’utilisation répétée de périssables, ou le manque de portabilité du matériel sont d’autres obstacles, non seulement à l’adhésion des thérapeutes à la prise en charge fonctionnelle, mais également à l’avancée de la recherche dans ce domaine. Le projet Rehab-QVA a permis d’évaluer l’intérêt des techniques de réalité virtuelle pour améliorer l’autonomie de patients Alzheimer pour des AVQs en cuisine via l’apprentissage sans erreurs."
done: "Dans ce contexte, nous avons créé une cuisine virtuelle permettant de réaliser dix activités, et implémenté une méthode d’entraînement ainsi qu’une procédure d’évaluation. La méthode d’entraînement se fonde sur l’apprentissage sans erreurs et des assistances rétroactives délivrées après une certaine durée d’action libre. Le développement a suivi un processus itératif comprenant différents cycles. Chaque cycle était déterminé par un objectif, associé à une phase d’analyse-conception, puis une phase d’évaluation-analyse suivie de rectifications éventuelles. Les premiers tests ont porté sur les scripts verbaux et les retours visuels et sonores qui permettent de suivre le déroulement des tâches. Ensuite, nous avons évalué l’utilisabilité du logiciel auprès de personnes âgées en bonne santé. Une fois le système utilisable dans le cadre de la prise en charge, nous avons voulu savoir si un entraînement au moyen de notre système permet d’accroître ou non l’autonomie réelle des patients, comparé à un entraînement analogue en contexte réel. Ainsi, nous avons pris en charge 10 patients pendant 4 semaines, en virtuel et en réel, et évaluer leur autonomie en réel avant et après l’entraînement, puis 1 mois et 6 mois après la fin de la phrase d’entraînement."
results: "La plupart des résultats sont en cours de publication."
---

{% for post in site.projects reversed %}
  {% if post.title == title %}
    {% include projectdetailled.html %}
    {% endif %}
{% endfor %}
