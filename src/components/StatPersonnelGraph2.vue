<template>
    <div>
        <!-- style="width: 900px; height: 300px;"" -->
            <div id="piechart" style="width:100%;"></div>
            <div id="chart_div4" style="width:100%;"></div>
        <div id="chart_div3" style="width:100%;"></div>
        <div id="chart_div" style="width:100%;"></div>
    </div>
</template>
<script>
import { GoogleCharts } from 'google-charts';
export default {

    data(){

        return {
            stat_sami: [
                [
                    "lettre",
                    "nb"
                ],
                [
                    "S",
                    240
                ],
                [
                    "A",
                    15
                ],
                [
                    "M",
                    10
                ],
                [
                    "I",
                    0
                ]
            ],
        
            stat_sami_collecte: [
                [
                    "Item",
                    "S",
                    "A",
                    "M",
                    "I"
                ],
                [
                    "2022-02-10 KN AGENT PRESTATAIRE LAM",
                    18,
                    2,
                    1,
                    0
                ],
                [
                    "2022-02-10 KN AGENT PRESTATAIRE LAM",
                    18,
                    2,
                    1,
                    0
                ],
                [
                    "2022-02-14 KN ANNONCEUR SENTINELLE",
                    35,
                    0,
                    0,
                    0
                ],
                [
                    "2022-02-14 KN ANNONCEUR SENTINELLE",
                    35,
                    0,
                    0,
                    0
                ],
                [
                    "2022-04-14 KN ANNONCEUR SENTINELLE",
                    28,
                    0,
                    0,
                    0
                ],
                [
                    "2022-05-05 KN AGENT DE SECURITE DU PERSONNEL EN EQUIPE",
                    42,
                    1,
                    7,
                    0
                ],
                [
                    "2022-08-31 KN ANNONCEUR SENTINELLE",
                    27,
                    3,
                    1,
                    0
                ],
                [
                    "2022-09-16 KN AGENT DE SECURITE DU PERSONNEL EN EQUIPE",
                    37,
                    7,
                    0,
                    0
                ]
            ],
            stat_sami_formulaire: [
                [
                    "Item",
                    "S",
                    "A",
                    "M",
                    "I"
                ],
                [
                    " KN AGENT PRESTATAIRE LAM",
                    36,
                    4,
                    2,
                    0
                ],
                [
                    " KN ANNONCEUR SENTINELLE",
                    125,
                    3,
                    1,
                    0
                ],
                [
                    " KN AGENT DE SECURITE DU PERSONNEL EN EQUIPE",
                    79,
                    8,
                    7,
                    0
                ]
            ],
        
            stat_sami_question: [
            [
                "Item",
                "S",
                "A",
                "M",
                "I"
            ],
            [
                " Connaissance de l'environnement (particularit??s locales)",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des textes r??glementaires (ISF, PPSPS)",
                2,
                0,
                0,
                0
            ],
            [
                " Application briefing",
                2,
                0,
                0,
                0
            ],
            [
                " Risques li??s ?? la circulation",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition de la zone dangereuse",
                2,
                0,
                0,
                0
            ],
            [
                " Risques li??s ?? la traction ??lectrique",
                2,
                0,
                0,
                0
            ],
            [
                " Hauteur minimum et maximum de la cat??naire ? Hauteur sur LGV ?",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition des zones ??lectriques",
                2,
                0,
                0,
                0
            ],
            [
                " Signification des diff??rents passants (gris, jaune, vert, bleu, violet)",
                2,
                0,
                0,
                0
            ],
            [
                " Comportement de l'agent",
                2,
                0,
                0,
                0
            ],
            [
                " Concentration de l'agent",
                2,
                0,
                0,
                0
            ],
            [
                " V??rification de(s) engin(s) (agr??s, agr??ments, limiteurs)",
                2,
                0,
                0,
                0
            ],
            [
                " Conditions mont??e descente",
                2,
                0,
                0,
                0
            ],
            [
                " Immobilisation Gestion des al??as",
                0,
                2,
                0,
                0
            ],
            [
                " Mesures en cas de d??faillance conducteur",
                2,
                0,
                0,
                0
            ],
            [
                " Conditions pour plusieurs LAM",
                2,
                0,
                0,
                0
            ],
            [
                " Stationnement du LAM (conditions ?? respecter)",
                0,
                0,
                2,
                0
            ],
            [
                " Hauteur du limiteur de la pelle",
                2,
                0,
                0,
                0
            ],
            [
                " Sp??cificit??s enraillement ?? un PN",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des textes r??glementaires (ISF, PPSPS)",
                0,
                2,
                0,
                0
            ],
            [
                " Utilisation de Pebble",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des lieux (vitesses, sens de circulation, particularit??s ???)",
                4,
                0,
                0,
                0
            ],
            [
                " Connaissance de la voie de travail",
                4,
                0,
                0,
                0
            ],
            [
                " Connaissance de l'emplacement de garage",
                4,
                0,
                0,
                0
            ],
            [
                " Connaissance du PRS sur le chantier et l?? t??l??phone d'alarme le plus proche",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des documents de pr??vention sur la tablette (PGC, PDP, CSF, ISF, NSF,  PPSPS,???)",
                2,
                0,
                0,
                0
            ],
            [
                " Possession, validit??e de la carte d'habilitation et l'acc??s aux emprises",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition de la zone dangereuse + valeurs ",
                2,
                0,
                0,
                0
            ],
            [
                " Signification des diff??rents passants (gris, jaune, vert, bleu, violet)",
                2,
                0,
                0,
                0
            ],
            [
                " Comportement de l'agent",
                4,
                0,
                0,
                0
            ],
            [
                " Concentration de l'agent",
                4,
                0,
                0,
                0
            ],
            [
                " R??activit?? de l'agent",
                4,
                0,
                0,
                0
            ],
            [
                " Quels sont les 4 conditions l??gales ?? remplir pour ??tre annonceur sentinelle ?",
                4,
                0,
                0,
                0
            ],
            [
                " Port des EPI et bon ??tat pour la mission",
                2,
                0,
                0,
                0
            ],
            [
                " Quels sont les agr??s d'un annonceur ?",
                4,
                0,
                0,
                0
            ],
            [
                " Validit?? des p??tards",
                4,
                0,
                0,
                0
            ],
            [
                " Validit?? de la torche et dur??e de combustion",
                4,
                0,
                0,
                0
            ],
            [
                " Comment craquer une torche ?? flamme rouge ( en mode secours et le positionnement)",
                4,
                0,
                0,
                0
            ],
            [
                " Etat des diff??rents agr??s",
                4,
                0,
                0,
                0
            ],
            [
                " Etat du carquois",
                2,
                0,
                0,
                0
            ],
            [
                " Quels sont les agr??s d'un annonceur de nuit ?",
                4,
                0,
                0,
                0
            ],
            [
                " Positionnement de l'annonceur",
                4,
                0,
                0,
                0
            ],
            [
                " Connaissance de la DCO ( Proposer diff??rents cas)",
                3,
                1,
                0,
                0
            ],
            [
                " Point d'annonce (avec rep??re physique)",
                2,
                0,
                0,
                0
            ],
            [
                " Identification des voies",
                2,
                0,
                0,
                0
            ],
            [
                " Sens de circulation surveill??",
                2,
                0,
                0,
                0
            ],
            [
                " Possession de la CADA et signification",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des emplacements de garage",
                4,
                0,
                0,
                0
            ],
            [
                " Utilisation de la trompe ?? grande puissance (pression, purge en fin de journ??e, ???)",
                4,
                0,
                0,
                0
            ],
            [
                " Audibilit?? de l'annonce sur le chantier",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des diff??rentes voies ?? annoncer",
                4,
                0,
                0,
                0
            ],
            [
                " Connaissance de la distance moyenne entre 2 t??l??phones d'alarme",
                4,
                0,
                0,
                0
            ],
            [
                " R??le RPAC",
                2,
                0,
                0,
                0
            ],
            [
                " R??le ASP et ASP rempla??ant",
                2,
                0,
                0,
                0
            ],
            [
                " R??le annonceur",
                4,
                0,
                0,
                0
            ],
            [
                " Les diff??rents emplacements de garage et d??finition d'un garage r??duit",
                2,
                0,
                0,
                0
            ],
            [
                " Possession des EPI obligatoire",
                2,
                0,
                0,
                0
            ],
            [
                " Risques li??s ?? la circulation",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition de la zone dangereuse",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition des zones ??lectriques",
                2,
                0,
                0,
                0
            ],
            [
                " Citer les r??gles qui sauvent",
                2,
                0,
                0,
                0
            ],
            [
                " Port des EPI pour la mission ?",
                2,
                0,
                0,
                0
            ],
            [
                " R??percussion de l'alerte donn??e par une sentinelle",
                2,
                0,
                0,
                0
            ],
            [
                " Quelles informations peut-on trouver sur un support cat??naire ?",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance des lieux (vitesse, sens de circulation, particularit??s, ???)",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance de la voie de travail",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance du t??l??phone d'alarme le plus proche du chantier",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance organisation du chantier  phasage",
                2,
                0,
                0,
                0
            ],
            [
                " Quelles sont les conditions pour cumuler le r??le d'ASP Annonceur",
                0,
                1,
                1,
                0
            ],
            [
                " Que doit faire un ASP lors d'une CO",
                2,
                0,
                0,
                0
            ],
            [
                " Quelles informations peut-on trouver sur un support cat??naire ?",
                2,
                0,
                0,
                0
            ],
            [
                " O?? trouve-t-on les pistes et itin??raires ?",
                2,
                0,
                0,
                0
            ],
            [
                " Respect des zones de voisinage des parties sous tension",
                2,
                0,
                0,
                0
            ],
            [
                " Travers??e de mat??riaux",
                1,
                0,
                0,
                0
            ],
            [
                " Connaissance et respect du gabarit des d??p??ts provisoires (sch??ma)",
                2,
                0,
                0,
                0
            ],
            [
                " S??ret?? du chantier",
                1,
                0,
                0,
                0
            ],
            [
                " Les diff??rents emplacements de garage",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition d'un garage r??duit",
                1,
                0,
                0,
                0
            ],
            [
                " Manutention de pi??ces lourdes et encombrantes",
                2,
                0,
                0,
                0
            ],
            [
                " Risques li??s ?? la circulation",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition de la zone dangereuse et ses valeurs",
                1,
                1,
                0,
                0
            ],
            [
                " Risques li??s ?? la traction ??lectrique",
                2,
                0,
                0,
                0
            ],
            [
                " Hauteur minimum et maximum de la cat??naire ? Hauteur sur LGV ?",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition des zones ??lectriques",
                2,
                0,
                0,
                0
            ],
            [
                " R??gles de rep??rage dans les emprises ferrovaires",
                2,
                0,
                0,
                0
            ],
            [
                " Signification des diff??rents passants (gris, jaune, vert, bleu, violet)",
                2,
                0,
                0,
                0
            ],
            [
                " Comportement de l'agent",
                2,
                0,
                0,
                0
            ],
            [
                " Concentration de l'agent",
                2,
                0,
                0,
                0
            ],
            [
                " R??activit?? de l'agent",
                2,
                0,
                0,
                0
            ],
            [
                " Citer les r??gles qui sauvent",
                1,
                1,
                0,
                0
            ],
            [
                " Identification du RPAC et ou agent s??curit??",
                2,
                0,
                0,
                0
            ],
            [
                " Cat??gorie d'outillage utilis?? pour la mission",
                2,
                0,
                0,
                0
            ],
            [
                " Exception d'utilisation de la 1??re et 2??me cat??gorie",
                0,
                1,
                1,
                0
            ],
            [
                " Port des EPI adapt??s au travail entrepris",
                2,
                0,
                0,
                0
            ],
            [
                " Quels sont les agr??s d'un ASP Agent seul ?",
                1,
                0,
                0,
                0
            ],
            [
                " Validit?? des p??tards",
                2,
                0,
                0,
                0
            ],
            [
                " Validit?? de la torche et dur??e de combustion et connaissance de son fonctionnement",
                2,
                0,
                0,
                0
            ],
            [
                " Port des diff??rents passants (gris, jaune, vert, bleu, mauve)",
                1,
                0,
                0,
                0
            ],
            [
                " Que doit poss??der un ASP pour cumuler avec le r??le d'annonceur",
                0,
                0,
                1,
                0
            ],
            [
                " D??termination de la zone de travail",
                2,
                0,
                0,
                0
            ],
            [
                " Prise en compte de la cat??gorie d'outillage",
                2,
                0,
                0,
                0
            ],
            [
                " D??termination de l'emplacement de garage et des zones de garage r??duit",
                2,
                0,
                0,
                0
            ],
            [
                " Comment d??termine t'on une marge de s??curit??",
                1,
                0,
                1,
                0
            ],
            [
                " Quelles sont les questions ?? se poser sur voie circul??e?",
                0,
                1,
                1,
                0
            ],
            [
                " Quels sont les questions ?? se poser sur voie intercept??e ou proche d'une ZD",
                1,
                0,
                1,
                0
            ],
            [
                " V??rification du chantier",
                2,
                0,
                0,
                0
            ],
            [
                " R??le ASP et ASP rempla??ant",
                1,
                0,
                0,
                0
            ],
            [
                " VU - VUT - IPCS - ITCS - voie banalis??e - double voie - TCT",
                2,
                0,
                0,
                0
            ],
            [
                " Signification et principe de la CADA",
                2,
                0,
                0,
                0
            ],
            [
                " Connaissance de la distance moyenne entre 2 t??l??phones d'alarme",
                2,
                0,
                0,
                0
            ],
            [
                " Valeurs d'un quai bas, haut et mi haut",
                2,
                0,
                0,
                0
            ],
            [
                " D??finition du RCT",
                1,
                0,
                0,
                0
            ],
            [
                " Ensemble des documents li??s ?? la mission ayant la bonne version ",
                1,
                0,
                0,
                0
            ],
            [
                " Appr??ciation g??n??rale : (noter S, A, M ou I dans la case)",
                0,
                1,
                1,
                0
            ],
            [
                " Connaissance des gabarits de d??p??t provisoire (sch??ma)",
                0,
                0,
                1,
                0
            ],
            [
                " VU - VUT - IPCS - ITCS - TCT - voie banalis??e - double voie",
                0,
                1,
                0,
                0
            ],
            [
                " Appr??ciation g??n??rale : (noter S, A, M ou I dans la case)",
                0,
                1,
                0,
                0
            ],
            [
                " Possession, validit??e de la carte d'habililitation et acc??s aux emprises",
                1,
                0,
                0,
                0
            ],
            [
                " Briefing avant le d??part sur le chantier avec r??alisateur",
                0,
                1,
                0,
                0
            ],
            [
                " Connaissance textes de prescription",
                0,
                1,
                0,
                0
            ]
            ]
        }
    },
    methods: {
        drawChart() {
            let div = document.getElementById('piechart');
            let datatable = this.stat_sami;

            let data = GoogleCharts.api.visualization.arrayToDataTable(datatable);

            var options = {
            title: 'R??partition des r??ponses sur l\'ensemble des KN',
            // width: '100%',
            is3D: true,
            pieSliceText: 'label',
            colors: ['#198754', '#0d6efd', '#ffc107', '#dc3545']
            };

            let chart = new GoogleCharts.api.visualization.PieChart(div);

            chart.draw(data, options);
        },

        drawStacked() {
            let div = document.getElementById('chart_div');
            let datatable = this.stat_sami_question;

            var data2 = GoogleCharts.api.visualization.arrayToDataTable(datatable);

            var options2 = {
            title: 'r??partitions des r??ponses par questions',
            // width: 400,

            chartArea: {width: '40%'},
            isStacked: 'percent',
            colors: ['#198754', '#0d6efd', '#ffc107', '#dc3545'],
            legend: { position: 'top', maxLines: 4 },
            height: 2000
            };
            let chart = new GoogleCharts.api.visualization.BarChart(div);
            chart.draw(data2, options2);
        },

        drawStacked3() {
            let div = document.getElementById('chart_div3');
            let datatable = this.stat_sami_formulaire;

            var data3 = GoogleCharts.api.visualization.arrayToDataTable(datatable);

            var options3 = {
                title: 'r??partition des r??ponses par habilitation',
                chartArea: {width: '40%'},
                isStacked: 'percent',
                colors: ['#198754', '#0d6efd', '#ffc107', '#dc3545'],
                legend: { position: 'top', maxLines: 4 }
            };
            let chart = new GoogleCharts.api.visualization.BarChart(div);
            chart.draw(data3, options3);
            },
            drawStacked4() {
            let div = document.getElementById('chart_div4');
            let datatable = this.stat_sami_collecte;

            var data4 = GoogleCharts.api.visualization.arrayToDataTable(datatable);

            var options4 = {
                title: 'r??partition des r??ponses  par KN r??alis??s',
                chartArea: {width: '50%'},
                isStacked: 'percent',
                colors: ['#198754', '#0d6efd', '#ffc107', '#dc3545'],
                legend: { position: 'top', maxLines: 4 }
            };
            let chart = new GoogleCharts.api.visualization.BarChart(div);
            chart.draw(data4, options4);
            }
    },

    beforeUnmount() {
        window.removeEventListener("resize", this.drawChart);
        window.removeEventListener("resize", this.drawStacked);
        window.removeEventListener("resize", this.drawStacked3);
        window.removeEventListener("resize", this.drawStacked4);
        
    },

    mounted(){
        GoogleCharts.load(this.drawChart);
        GoogleCharts.load(this.drawStacked);
        GoogleCharts.load(this.drawStacked3);
        GoogleCharts.load(this.drawStacked4);
        window.addEventListener("resize", this.drawChart);
        window.addEventListener("resize", this.drawStacked);
        window.addEventListener("resize", this.drawStacked3);
        window.addEventListener("resize", this.drawStacked4);




    }


}
</script>