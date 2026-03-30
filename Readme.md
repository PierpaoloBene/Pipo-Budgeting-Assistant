# Pipo Automatic Budgeting Assistant

Pipo aims to become an intelligent, automated personal finance assistant designed to help users seamlessly track, categorize, and optimize their daily expenses. By leveraging Open Banking APIs and Machine Learning, Pipo transforms raw transactional data into actionable financial insights.

## Work Phases
- [ ] Research on Open Banking APIs for personal use   
- [ ] Meeting to schedule how to organize the work, the framework, and the agenda  
- [ ] TBD ...

`Commento: l'idea è quella di documentare non solo il codice ma anche le scelte prese. Il progetto sarà lungo e andrà per le lunghe. In questo modo potremmo ricordare perchè abbiamo scelto un'opzione rispetto ad un'altra e riconsultare il processo decisionale in futuro se le cose cambiano o se ci serve un refresh.`  
## 1. OpenBanking APIs
To build Pipo for personal use while remaining fully compliant with **PSD2** regulations, direct connection to bank APIs is not possible without a specific license. 

It is not possible to directly leverage openbaking APISs, so Pipo must rely on an authorized *Account Information Service Provider (AISP)* acting as a secure bridge.


**Findings:**
* **GoCardless (formerly Nordigen):** Option that i'm investigating rn. 
* **Plaid:** Next to be studied
* `Aggiungere qui altre alternative`

Link utili:
 - [What is an api in open banklng](https://gocardless.com/guides/posts/what-is-an-api-in-open-banking/)
 - [I just found this awesome EU Banking API for personal use](https://dev.to/jerzakm/i-just-found-this-awesome-eu-banking-api-for-personal-use-113a)