## Divisão 2

- **1. Introdução**
  - ***1.1 Saudação.***
    
- **2. Reconhecimento do cidadão:**

  - ***2.1 Identificação_usuario***
  - ***2.2 Aviso_CPF_inválido***
  - ***2.3 Verificação_cadastro_cidadão:***
    - Buscar Cidadão
      - Definir tipo do usuário
  - ***2.4 Info_Cidadao_pelo_Botpress:***
    - Buscar Cidadão
      -  Definir tipo do usuário 
  - ***2.5 Confirmacao_dados_cidadao:***
    - Mostrar resumo cad. manif.
  - ***2.6 Aviso_anônimo***
  - ***2.7 return_to_identificação***
  - ***2.8 Saudação_cadastro_cidadão***
 
- **3. Cadastro do usuário:**
  
  - ***3.1 Cadastro_cidadao:***
    - Processar Doc. de Identificação
    - WF - Cadastro do Manifestante
      - Enviar WAFlow
      - Mostrar resumo cad. manif.
    - Inserir Cidadão
      - Definir Tipo de Usuário 
  - ***3.2 aviso_falha_processamento***
  - ***3.3 CPF_divergente***
  - ***3.4 Aviso_CPF_divergente***

- **4. Escolhas de serviço do Cidadão**
  - ***4.1 Escolha_servico_bot***
  - ***4.3 Teimoso:***
    - Iterações Reusáveis/Usuário teimoso
  - ***4.2 Obter_protocolos:***
    - Listagem de Protocolos:
      - Listar Protocolos
      - Iterações Reusáveis/Usuário Teimoso
      - Iterações Reusáveis/Mostrar info do protocolo
      - Registrar consulta
        - Criacao Protocolo
        - Finalização genérica  
	- ***4.3 Registrar_nova_demanda:***
		- Iterações Reusáveis/Nova Demanda
      - Iterações Reusáveis/Usuário teimoso
        
- **5. Serviço: Registrar nova demanda:**
  - ***5.1 Pega_endereço_se_nescessario:***
    - Endereço por FLAG
      - WF_Cadastro_Endereco_Ocor
      - WF - Endereço via Location
  - ***5.2 Transferência_atn_humano***
  - ***5.3 Teimoso:***
    - Iterações Reusáveis/Usuário teimoso
      
  - **6.0 Registro: Transição de fluxo**
    - ***transição_de_fluxo:***
      - Iterações Reusáveis/Consulta protocolo manual
        - Busca Protocolo
        - Registrar consulta
          - Criacao Protocolo
          - Finalização genérica
    - ***Elogio_Sugestao:***
      - Elogio / Sugestão
        - Resumo e correção
        -  Iterações Reusáveis/Usuário teimoso
        -  Criacao Protocolo Completa
          -  Anexar Arquivos Protocolo
          -  Criacao Protocolo
        -  Finalização genérica
    - ***Denuncia_Reclamacao***
      - Reclamação / Denúncia
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Fluxo_uma_lâmpada***
      -  Fluxo iluminação - uma lâmpada
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Fluxo_multipas_lampadas***
      - Fluxo Iluminação - duas ou mais lâmpadas
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Fluxo_solicitação_fiscalize***
      - WF - Solicitação do Fiscalize:
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Fluxo_Protocolo_nao_Atendido***
      - Fluxo Reclamação não atendida:
        - Buscar Protocolo
        - Listagem de Protocolos:
          - Listar Protocolos
          - Iterações Reusáveis/Usuário Teimoso
          - Iterações Reusáveis/Mostrar info do protocolo
          - Registrar consulta
            - Criacao Protocolo
            - Finalização genérica
        - Mostrar info do protocolo
        - Endereço por FLAG
          - WF_Cadastro_Endereco_Ocor
            - Enviar WAflow
          - WF - Endereço via Location
            - Usuário teimoso  
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Sindionibus:***
      - WF- Sindiônibus:
        - Enviar WAFlow
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
        - Finalização genérica
    - ***Solicitação_bloqueio_bilhete_unico:***
      - Solicitação de Bloqueio do Bilhete Único
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
    - ***Rec_Consulta_Medica***
      - Reclamação Consulta Medica
        - Enviar WAFlow
        - Resumo e correção
        - Iterações Reusáveis/Usuário teimoso
        - Criacao Protocolo Completa:
          - Anexar Arquivos Protocolo
          - Criacao Protocolo
        - Finalização genérica
     - ***Vale_gas***
       - Central 156 - Consulta Vale Gás
          - Resumo e correção
          - Iterações Reusáveis/Usuário teimoso
          - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
          - Finalização genérica
      - ***Agend_Castracao_Animal***
        - Agend Castração Animal:
          - Enviar WAFlow
          - Resumo e correção
          - Iterações Reusáveis/Usuário teimoso
          - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
          - Finalização genérica
      - ***Reforço_Agendamento***
        - Reforço Agend Castração:
        - Resumo e correção
          - Iterações Reusáveis/Usuário teimoso
          - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
          - Finalização genérica
    - ***COESD_CPDrogas***
      -  WF - COESD CPDrogas:
        - Enviar WAFlow
        - Resumo e correção
        - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
        - Finalização genérica
    - ***Agendamento_AMC***
      - WF - Agendamento AMC:
        - Enviar WAFlow
        - Resumo e correção
        - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
        - Finalização genérica
    - ***Info_carteirinha_estudante***
      - WF - Info carteirinha ETUFOR:
      - Enviar WAFlow
        - Resumo e correção
        - Criacao Protocolo Completa:
            - Anexar Arquivos Protocolo
            - Criacao Protocolo
        - Finalização genérica
    Obs:Todos deste bloco no final vão para o mesmo card.
    - ***Back_to_menu*** 
        

   




      
- **7. Serviço: Consultar Demanda registrada:**
  - ***7.1 consulta_protocolo***
    - Iterações Reusáveis/Consulta protocolo manual
      - Buscar Protocolo
      - Registrar consulta
      



- **Cards sem utilização**
  - Aviso_cadastro_inalterado 


  
	
	
 
		
		
		

	

	
