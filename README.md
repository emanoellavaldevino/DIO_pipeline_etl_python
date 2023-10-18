# DIO: Pipeline ETL Python
_Explorando IA Generativa em um Pipeline de ETL com Python_

### ▶ Proposta
O objetivo é usar o poder da IA Generativa para criar mensagens de marketing personalizadas que serão entregues a cada cliente.

### ▶ Metodologia

* Coleta e Aquisição dos Dados - Extract

Criamos um arquivo em formato CSV., colocamos uma lista de _UserIDs_ de usuário do banco, de acordo com o Briefing enviado.
No link: [API da Santander Dev Week 2023](https://sdw-2023-prd.up.railway.app/swagger-ui/index.html#/) Foram criadas IDs no **GET**: _4970, 4971 e 4972_.

![User_4970](https://lh3.googleusercontent.com/pw/ADCreHcSYriXHcwkPkqIJU7RXHLTdDoW1fJoN22FIcV6uc-M6Xwj9vbVosZG70O5egay0AfZBf3LKjIOFRW-puE1QrecE8vKSagflO9bL5mH2Y6Bajh3Vcmv8ATJ34EW0frG1XOoHnSNZuruySCIDEoCJnjwg7-d9We-IVHAFc0IfZHyHbWgQv1x0kTNz0T_FGihg_lHSCTmLCYOGVQDnmr2BpI5vgiXl4PsuhkyGJRRftmJiSPBGHZyvbjCYAMTogJBI5zF2smzjQevM1pha4ATPwnHu4SyMSbsIcJtrpj7kJw_729cpByZwHAXwwdsbSeTutZQUSPtxxrxv5CRYyCHYxHNicv89Bwg05KvPf98DaRqBMV6VWELChW_wOjiyUryqWjOvtEvGeC8bgp5svbhaCRyy20pZcGXCJ2vT_D6zgalHn7BHQTKGA8-4digGstQ8k0bsOE2VeGWfcB-h9BEEdrDSpcSXS9apnrGLC3j1-Wuo8JPgByRH29db-VwhasyM60aoJ1L1BKPDCXROAvG8NoBarGp-wdTLfoMJcFtdCp2KneRV9E-CE8n6pdzTloTeH6kuLVMTaIhCFae3ySAcQfHeSiNsV69TjqfUgyC3kMiy3UBc6jei1IyY3Xgz5ZEDoGGGGW_QDddht3GcqrmvEnRDV5-iWrawZr6eY7OLaYEOikvT7w09uax9KdqMECVuSyinIaKi7L92WQA9R44UJcj-bHAouGeWYIHOWCqIIwQzq8eHywWznUiTj8rAHkmrY3CoXnQci2lSz9iX_-4eSrCZgdJ5fVdRY-EQkDQrlhMkmUf-2GHfNs7yd2LBj9bSOQAKPiZVUII_ZdfvGQq_Zj2AZgYe76OU9tM6Ia1va4DUCYIOVtzIoPan0P-c12VJojX7IYJYvP2lgmoExPSAhI=w763-h379-s-no-gm?authuser=0) 

**Conexão gerada via [Santander Dev Week 2023](https://colab.research.google.com/drive/1SF_Q3AybFPozCcoFBptDSFbMk-6IVGF-?usp=sharing) com o update do arquivo _SDW2023.csv_**

* Utilizando o IA via ChatGPT - Transform

Foi utilizado a API do OpenAI gpt-3.5-turbo para gerar uma mensagem de marketing personalizada para cada usuário. Substituir pela sua API key, criada no OpenIA [OpenIA](https://platform.openai.com/account/api-keys).

![ API do OpenAI - gpt-3.5-turbo](https://lh3.googleusercontent.com/pw/ADCreHccjvPF_ZsQRBt8aS_vTYcp9CbJBUl5i4GvBs25-Fa4EyFPwbvcg0L8la63IZELW9o28E7WBIzIs-RdXqsSwMvzsDwtk28PcWYK_ChQb5csnRVL3O14Yy_8e9-Iul0gVeikG_e4uiiTllLAaB5TdAC0QRpsAHBudcfPU-WVhuRketv3l838rBXCUJLEFEKKFjz6gmc3lVnJqoteyraWpa0nlUERJlRgaB3gKvlC7A16lwmJHlnGLGTB7OTHdEHpOTUmLWE4_8pSsmuBsV93fWikO3mXnwy6inGzAUdvUo6XDcvKaGwGl2zArCXiRRCTheaBA-ZIE576WxauRink3kf0qSK3yLZmUi95dEQBuhT6nCa_1JPKQIx9AZTTxzURHVEfDItnIJGqxXbb0Jwfr53ZTeoMy8GGyWTUXr81B2P-ckq3PqQGEf1WInKtqayJRSCdJGW5LHbTv5GyACmCEe9gLGaaUEiGTLUYSazL8lBzIU1h99yt12RawpXklO8vxG_TDIu2LMCQ755514QK7eOhrVBsWJpYTIySH3E_QuTrqOYvB0bvMYPY8z3UYRGaV5gcI5ik7MtSyJ6IdUuMVW6lox19WgxizSvH0fhHK69y6ns7e1h-9bnjwwt9gfklnxNrMLkbUp2ejcR1Skn18-suS-dm2XyRCaxERoqzOLW52E-kQHvcKF7E1RGCJSTNwO4kg--aK0Ij9YcYaq-2pntDtO4hkBY4uLgd_NEf0U2wNyL4oL4aOBr8G1ZeU2MhDHgnPtP9U3H_XBXfxakbY52ZQYdMWJ5hBtgn6qBaAHS_3AEU5fDVkmz-4ED8HV3oc6b81XoPCfwjS48qLcz8QQ7-Te3u42IIYUSrDOiGoQYGkh7XFu9Pr3SJtyVd8Sa8D29DWpJge1Y278d1xV40SjQ=w984-h349-s-no-gm?authuser=0)

* Load

Atualize a lista de "news" de cada usuário na API com a nova mensagem gerada.

![Células](https://lh3.googleusercontent.com/pw/ADCreHckk1etc8qwKJksBUiqdLZbxrueMCBStboXyFS1EgBsBa75AzJXKIwJ8T2vjDgqZKmPAOxE_Vo63larJ8n2kpGQlIRRhHfF-XIKYQjw3bdRzle459gLp34bd9t_0xIQ5XgJMbEAvRUgu2_xQ_nspG9aiH7R6rjHPC6vxTaSgI8BFDJ4DQ9yPQSQHn5ElDjanHtQ0bfn0i_d29MPR9WNE34xlAq5COTXkICf47GPL4xrD3n_oOKDhKWqXwcMVfDXkKoZyespDda3b0LgCrQnWP_-SrOubyXbX4TB3uEfF2kWkQscmCypwIIlfLyWS0J0a6eK-2kHOD6jgifLa6leMDetnYYMnG_oil7tKaJGPeh5BDmGTH4XFPSRBi9_C4KqVVJKHtudFz52jtGnlOuJj20zsjfmHeOMoOrJZyjf2reSVQY3SZJ9krbUrHVPHsaxnDa0dhdh1BN0fR8Qmxkkddnzc1HaZcSZiTObrpT75uChv9FilTLSDW0dutYaw8yo2tF33PmbvV4qZZXaIJIucJR9Xj9guILlErhRkJ6MnFpg9oLdKxG7Q0wB6CStOcZ5ouBva9i1U0t-pMZbWIS2K5lU9WqVkpFyHkEUOks4kiwoDw25BHzY2ExbqEQ-qm6xL3tV-XaeioyLB7pHXSusP9Yv9TcYgFHmH1yc5X9oiWBtda8XyCgl-6zY4FvTrmf_Nypknni7mhfjHFkU6zDqlVNiBnZosNnE_OtQslWsRs65WlUusIeGqI3N_EU9Qc_lgUgcqeEJ5aNAnadDsR1CItks47mXniKK2-7mnVEN0xSsanfLhYAV1CU-PcwuphDtl_pL2me_PiqfTnvD0_oAn7MlBGsGBjLA7lDIVNEQ4sOzXIdjsyB78fCdOsGaJHwlhXbVBJoPGg7h7oijUbJK6XA=w843-h174-s-no-gm?authuser=0).

### ▶ Linguagem Utilizada


![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=white&color=black)

### ▶ Bibliotecas Utilizadas

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white&color=black) 	![OpenAI](https://img.shields.io/badge/OpenAI-%233F4F75.svg?style=for-the-badge&logoColor=white&color=black)












