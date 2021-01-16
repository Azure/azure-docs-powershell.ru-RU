---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421343"
---
# <span data-ttu-id="fe348-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="fe348-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="fe348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe348-102">SYNOPSIS</span></span>
<span data-ttu-id="fe348-103">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="fe348-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="fe348-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe348-104">SYNTAX</span></span>

### <span data-ttu-id="fe348-105">Получить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe348-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fe348-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fe348-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe348-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe348-107">DESCRIPTION</span></span>
<span data-ttu-id="fe348-108">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="fe348-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="fe348-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe348-109">EXAMPLES</span></span>

### <span data-ttu-id="fe348-110">Пример 1. Получить строку подключения PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="fe348-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="fe348-111">Этот cmdlet получает строку подключения PostgreSql server по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="fe348-112">Пример 2. Получить строку подключения сервера PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="fe348-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="fe348-113">Этот cmdlet получает строку подключения PostgreSql server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="fe348-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="fe348-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe348-114">PARAMETERS</span></span>

### <span data-ttu-id="fe348-115">-Client</span><span class="sxs-lookup"><span data-stu-id="fe348-115">-Client</span></span>
<span data-ttu-id="fe348-116">Поставщик клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="fe348-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe348-117">-DefaultProfile</span></span>
<span data-ttu-id="fe348-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe348-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe348-119">-InputObject</span></span>
<span data-ttu-id="fe348-120">Исходный серверный объект для создания репликации.</span><span class="sxs-lookup"><span data-stu-id="fe348-120">The source server object to create replica from.</span></span>
<span data-ttu-id="fe348-121">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="fe348-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fe348-122">-Name</span></span>
<span data-ttu-id="fe348-123">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe348-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe348-125">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fe348-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe348-126">-SubscriptionId</span></span>
<span data-ttu-id="fe348-127">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="fe348-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe348-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe348-128">CommonParameters</span></span>
<span data-ttu-id="fe348-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe348-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe348-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe348-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe348-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe348-131">INPUTS</span></span>

### <span data-ttu-id="fe348-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="fe348-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="fe348-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe348-133">OUTPUTS</span></span>

### <span data-ttu-id="fe348-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fe348-134">System.String</span></span>

## <span data-ttu-id="fe348-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe348-135">NOTES</span></span>

<span data-ttu-id="fe348-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe348-136">ALIASES</span></span>

<span data-ttu-id="fe348-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fe348-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe348-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fe348-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe348-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe348-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe348-140">INPUTOBJECT: <IServer> исходный объект сервера, из который создается реплика.</span><span class="sxs-lookup"><span data-stu-id="fe348-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="fe348-141">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe348-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="fe348-142">`[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="fe348-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="fe348-143">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="fe348-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fe348-144">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="fe348-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="fe348-145">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="fe348-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="fe348-146">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="fe348-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="fe348-147">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="fe348-148">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="fe348-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="fe348-149">Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe348-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="fe348-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="fe348-151">`[MasterServerId <String>]`: он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="fe348-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="fe348-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="fe348-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: разрешен ли доступ к общедоступным сетям для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="fe348-154">Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".</span><span class="sxs-lookup"><span data-stu-id="fe348-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="fe348-155">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.</span><span class="sxs-lookup"><span data-stu-id="fe348-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="fe348-156">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="fe348-157">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="fe348-158">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="fe348-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="fe348-159">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="fe348-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="fe348-160">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="fe348-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="fe348-161">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="fe348-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="fe348-162">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="fe348-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="fe348-163">`[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.</span><span class="sxs-lookup"><span data-stu-id="fe348-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="fe348-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="fe348-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="fe348-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe348-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="fe348-166">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="fe348-167">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="fe348-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="fe348-168">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="fe348-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="fe348-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe348-169">RELATED LINKS</span></span>

