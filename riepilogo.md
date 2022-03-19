## File Generati
- azienda_refactor.py
- bilancia_refactor.py
- chiamate_refactor.py
- datimanuali_refactor.py
- previsionale_refactor.py
- quesito_refactor.py
- rating_refactor.py
- report_refactor.py
- studio_refactor.py
- util_refactor.py
- query.py >>> __NUOVO__ file che contiene alcune query complesse, precedentemente scritte direttamente nelle classi dei Model


## Endpoint sottoposti a refactor

### GESTIONE STUDIO
- endpoint _creazionestudio.php_
	- `studio.py:creazionestudio()`
	- `util.py:get_formdata()`
- endpoint _getdatistudio.php_
	- `studio.py:getdatistudio()`
- endpoint _deldatistudio.php_
	- `studio.py:deldatistudio()`
- endpoint _updatedatistudio.php_
	- `studio.py:updatedatistudio()`
- endpoint _getpiutilizzate.php_ 
	- `studio.py:getpiutilizzate()`
- endpoint _getaziendestudio.php_
	- `studio.py:getaziendestudio()`
	- `bilancia.py:lastbilancioaziecod()`
	- `bilancia.py:valorebilancioazie()`
	- `studio.py:RATING_TYPES`
	- `rating.py:ratingbilanciodash()`


### GESTIONE AZIENDA
- endpoint _creazioneazienda.php_
	- `azienda.py:creazioneazienda()`
- endpoint _deldatiazienda.php_
	- `azienda.py:deldatiazienda()`
- endpoint _getdatiazienda.php_
	- `azienda.py:getdatiazienda()`
- endpoint _updateazienda.php_
	- `azienda.py:updateazienda()`
- endpoint _caricadaxbrl.php_
	- `azienda.py:caricadaxbrl()`
- endpoint _getelencoindici.php_
	- `azienda.py:getelencoindici()`
	- `azienda.py:INDEXES`


### DATI MANUALI
- endpoint _manualicaricati.php_
	- `datimanuali.py:manualicaricati()`)
- endpoint _listadatimanuali.php_
	- `datimanuali.py:listadatimanuali()`
- endpoint _getdatimanuali.php_ 
	- `datimanuali.py:getdatimanuali()`
- endpoint _deldatimanuali.php_
	- `datimanuali.py:deldatimanuali()`
- endpoint _creazionedatimanuali.php_
	- `datimanuali.py:creazionedatimanuali()`
- endpoint _updatedatimanuali.php_
	- `datimanuali.py:updatedatimanuali()`


### DATI MANUALI (previsionale)
- endpoint _manualicaricatipr.php_
	- `datimanuali.py:manualicaricatipr()`


### BILANCIO ORDINARIO:
- endpoint _getclassicrisi.php_
	- `chiamate.py:getclassicrisi()`
- endpoint _getclassiefmcc.php_
	- `chiamate.py:getclassiefmcc()`
- endpoint _generaapp.php_
	- `azienda.py:generaapp()`
- endpoint _bilanciazie.php_
	- `bilancia.py:bilanciazie()`
- endpoint _ratingbilancio.php_
	- `rating.py:ratingbilancio()`
- endpoint _leggivaloribilancio.php_
	- `bilancia.py:leggivaloribilancio()`


### QUEST:
- TODO segnare endpoint questdomande*, questrisposte*, questresult*  (TODO test)

- creazionequest*, delquest*, questionaricaricati


### BILANCIO PREVISIONALE
- endpoint _getparametripr.php_
	- `chiamate.py:getparametripr()`
- endpoint _listadatimanualiprevisionale.php_
	- `previsionale.py:listadatimanualiprevisionali()`
- endpoint _getparametriprevisionale.php_
	- `previsionale.py:getparametriprevisionale()`
- endpoint _getdatimanualiprevisionale.php_
	- `previsionale.py:getdatimanualiprevisionali()`
- endpoint _getdatidscrprevisionale.php_
	- `previsionale.py:getdatidscrprevisionale()`
- endpoint _leggiprevisionaleCE.php_
	- `previsionale.py:leggiprevisionaleCE()`
- endpoint _leggiprevisionaleIVA.php_
	- `previsionale.py:leggiprevisionaleIVA()`
- endpoint _leggiprevisionaleSP.php_
	- `previsionale.py:leggiprevisionaleSP()`
- endpoint _leggiprevisionaleDSCR.php_
	- `previsionale.py:leggiprevisionaleDSCR()`
- endpoint _leggiprevisionaleINCPAG.php_
	- `previsionale.py:leggiprevisionaleINCPAG()`
- endpoint _getincidenzeprevisionale.php_
	- `chiamate.py:getincidenzeprevisionale()`


### XBRL:
- endpoint _importaxbrl.php_
	- `xbrl.py:parse_xbrl()`
	- `query.py:xf01_get_formule_fase()`
	- `xbrl.py:parse_formula()` NOTA: solo fase 1
	- `xbrl.py:importaxbrl()`

- endpoint _importaxbrlfase2.php_
	- `xbrl.py:parse_formula()` NOTA: fase 2
	- `query.py:report_query()`
	- `report.py:dashazieeco()`
	- `report.py:dashazieliq()`
	- `report.py:IPF()`
	- `report.py:IPF2()`
	- `report.py:IROT()`
	- `xbrl.py:gat_rating_indici()`
	- `xbrl.py:CASHFLOW_REFS`
	- `xbrl.py:CASHFLOW_RATINGS`
	- `xbrl.py:get_rating_cashflow()`
	- `query.py:xf03_leggi_sp()`
	- `xbrl.py:SP_FASCE`
	- `xbrl.py:get_rating_spoor()`
	- `query.py:xf03_leggi_al()`
	- `xbrl.py:get_rating_alt()`
	- `query.py:xa02_leggi_info_mcc()`
	- `query.py:xb03_leggi_valore_mcc()`
	- `query.py:xf03_leggi_valore_mcc()`
	- `xbrl.py:get_rating_mcc_ef()`
	- `query.py:xf03_leggi_andamento_mcc()`
	- `xbrl.py:get_rating_mcc_and()`
	- `xbrl.py:get_rating_mcc_comb()`
	- `xbrl.py:ISA_REFS`
	- `xbrl.py:ISA_RATINGS`
	- `xbrl.py:get_rating_isa()`
	- `query.py:xf03_get_indici()`
	- `xbrl.py:importaxbrl_fase2()`
