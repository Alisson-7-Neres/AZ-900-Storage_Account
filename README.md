### Storage Account

- Criando uma Storage Account (**AZ-900_Lab_DIO**)
- *Portal Azure*

<img src='img/01-storage_account.png'/>
<img src='img/02-storage_account-create.png'/>

**Storage account name** é único, único no mundo todo.

<img src='img/03-storage_account-basics.png'/>

Em **redundancy** teremos quatro opções:
**Locally-redundant storage (LRS):**
Datacenter individual na região primária. 
**Geo-redundant storage (GRS):**
Datacenter único no primário e região secundária.
**Zone-redundant storage (ZRS):**
Três zonas de disponibilidade na região primária.
**Geo-zone-redundant storage (GZRS):**
Três zonas de disponibilidade na região primária e um único datacenter na região secundária.

<img src='img/04-storage_account-basics.png'/>

Em **advanced**, temos três opções de **acess tier**:
**Hot**
Otimizada para armazenamento de dados acessados com frequência.
**Cool**
Otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 30 dias.
**Cold**
Otimizado para o armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias.

<img src='img/05-storage_account-advanced.png'/>

No caso onde o Storage Account ficar muito tempo 'inativo' é essas opções estiverem marcada, será excluído: 'blobs,containers e file shares' em determinado período, nesse caso será em 7 dias.

<img src='img/06-storage_account-data-protetion.png'/>

<img src='img/07-storage_account-create.png'/>

Em **Data Storage**, terá três opções:
**Containers**
Serviço que orgazina conjuntos de dados não estruturados.
**File Shares**
Configura um compartilhamento de arquivos de rede altamente disponível que pode ser utilizado usando o protocolo Bloco de Mensagens do Servidor.
**Queues**
Serviço de armazenamento de mensagens que fornece armazenamento e recuperação para grandes quantidades de mensagens, cada uma com até 64 KB.
**Tables**
Fornece uma opção de chave/atributo para o armazenamento de dados estruturados não relacionais com um design sem esquema.
<img src='img/08-storage_account-data-storage.png'/>

### Migrate
Plataforma de migração unificada.

<img src='img/09-migrate.png'/>

<img src='img/10-migrate.png'/>

<img src='img/11-migrate-create.png'/>

<img src='img/12-migrate_created.png'/>

<img src='img/13-migrate.png'/>

### Container
Em **Storage Account**

<img src='img/14-storage_account-containers.png'/>

<img src='img/15-storage_account-containers.png'/>

Dentro do container criando, em **Shared access tokens**

<img src='img/16-storage_account-containers-tokens.png'/>

Clicando em **Generate SAS token and URL** teromos o link dos tokens
Obs.: Esses tokens são importantes na hora do gerenciamentode arquivos (AzCopy)

<img src='img/17-storage_account-containers-tokens.png'/>



### Opções de gerenciamento de arquivios 
**AzCopy**
Utilitario de linha de comando.
'https://learn.microsoft.com/pt-br/azure/storage/common/storage-use-azcopy-v10'

Como eu utilizo o OS Big Linux a instalação será essa:
sudo pamac update
sudo pamac install azcopy
sudo dnf install azcopy

No terminal
azcopy copy "C:\local\path" "token" --recursive=true

- C:\local\path -> Pasta de compartilhamento
- token -> token gerado do Container

No terminal

<img src='img/18-storage_account-azcopy.png'/>

Arquivos enviados

<img src='img/19-storage_account-azcopy-sent.png'/>

<img src='img/20-storage_account-azcopy-completed.png/'>

## Storage Explorer

Diferente do **AzCopy** e que é sincronização em uma direção, O **Storage Explorer** sincroniza os arquivos do Azure e locais de forma bidirecional, é também tem uma interface ao invés de utilizar o terminal.

<img src='img/21-storage_account-storage-explorer.png/'>

Criando conexão com o **Container**

<img src='img/22-storage_account-storage-explorer-app.png/'>

<img src='img/23-storage_account-storage-explorer-app.png/'/>

<img src='img/24-storage_account-storage-explorer-app.png/'/>

<img src='img/25-storage_account-storage-explorer-app.png/'/>

<img src='img/26-storage_account-storage-explorer-app.png/'/>

<img src='img/27-storage_account-storage-explorer-app.png/'/>

<img src='img/28-storage_account-storage-explorer-app.png/'/>

<img src='img/29-storage_account-storage-explorer-app.png/'/>








