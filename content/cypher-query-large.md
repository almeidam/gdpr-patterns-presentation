---
title        : Cypher Query Large
type         : neo4j
height       : 630
relationships:
gravity      : -500
menu         : main
weight       : 5
labels       :
    Vulnerability:
        caption: key
    Summary:
        caption: key
    Risk_Owner:
        caption: key
    #Brands:
    #    caption: key
    Risk:
        caption: key
---

{{< cypher-query height="55">}}
MATCH (a)-[to]-(b:Risk_Owner) where a.status = "Fixed" return *
//MATCH (a)-[to]-(b:Risk_Owner) where a.status = "Risk Approved" return *
{{</ cypher-query >}}

<style>
    body             { background-color: white    }
    #cypher-query    { padding: 5px ; margin: 0px }
    h2               { display: none  !important  }
</style>

<script>
    $('.app-header').hide()
    //$('h2').hide()
    $('.app-body').css( { margin: "0px"})
    $('.container-fluid').css( { padding: "0px"})
    $('.main').css( { margin : 0 })
    $('.sidebar').hide()
    $(function() {
        $('.app-footer').hide()
        });


</script>
