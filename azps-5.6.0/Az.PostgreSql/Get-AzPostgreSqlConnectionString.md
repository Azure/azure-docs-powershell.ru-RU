---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996092"
---
# <span data-ttu-id="bb256-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="bb256-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="bb256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb256-102">SYNOPSIS</span></span>
<span data-ttu-id="bb256-103">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bb256-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bb256-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb256-104">SYNTAX</span></span>

### <span data-ttu-id="bb256-105">Получить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb256-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb256-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb256-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb256-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb256-107">DESCRIPTION</span></span>
<span data-ttu-id="bb256-108">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bb256-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="bb256-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb256-109">EXAMPLES</span></span>

### <span data-ttu-id="bb256-110">Пример 1. Получить строку подключения PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="bb256-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="bb256-111">Этот cmdlet получает строку подключения PostgreSql server по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="bb256-112">Пример 2. Получить строку подключения Сервера PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="bb256-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="bb256-113">Этот cmdlet получает строку подключения PostgreSql server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="bb256-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="bb256-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb256-114">PARAMETERS</span></span>

### <span data-ttu-id="bb256-115">-Client</span><span class="sxs-lookup"><span data-stu-id="bb256-115">-Client</span></span>
<span data-ttu-id="bb256-116">Поставщик клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="bb256-116">Client connection provider.</span></span>

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

### <span data-ttu-id="bb256-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb256-117">-DefaultProfile</span></span>
<span data-ttu-id="bb256-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb256-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb256-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb256-119">-InputObject</span></span>
<span data-ttu-id="bb256-120">Сервер строки подключения Для сстройки. См. раздел "ЗАМЕТКИ" для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="bb256-120">The server for the connection string To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb256-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bb256-121">-Name</span></span>
<span data-ttu-id="bb256-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-122">The name of the server.</span></span>

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

### <span data-ttu-id="bb256-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb256-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb256-124">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="bb256-124">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bb256-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb256-125">-SubscriptionId</span></span>
<span data-ttu-id="bb256-126">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="bb256-126">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bb256-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb256-127">CommonParameters</span></span>
<span data-ttu-id="bb256-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb256-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb256-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb256-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb256-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb256-130">INPUTS</span></span>

### <span data-ttu-id="bb256-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="bb256-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bb256-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb256-132">OUTPUTS</span></span>

### <span data-ttu-id="bb256-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bb256-133">System.String</span></span>

## <span data-ttu-id="bb256-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb256-134">NOTES</span></span>

<span data-ttu-id="bb256-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bb256-135">ALIASES</span></span>

<span data-ttu-id="bb256-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bb256-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb256-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="bb256-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb256-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb256-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb256-139">INPUTOBJECT <IServer> : сервер для строки подключения</span><span class="sxs-lookup"><span data-stu-id="bb256-139">INPUTOBJECT <IServer>: The server for the connection string</span></span>
  - <span data-ttu-id="bb256-140">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="bb256-140">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="bb256-141">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb256-141">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bb256-142">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="bb256-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bb256-143">`[AdministratorLogin <String>]`. Имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="bb256-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bb256-144">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="bb256-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bb256-145">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="bb256-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bb256-146">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bb256-147">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="bb256-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bb256-148">Задайте для этого назначения ресурсу systemAssigned, чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb256-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bb256-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bb256-150">`[MasterServerId <String>]`: он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="bb256-150">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bb256-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bb256-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: разрешен ли доступ к общедоступным сетям для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bb256-153">Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".</span><span class="sxs-lookup"><span data-stu-id="bb256-153">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bb256-154">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этот сервер.</span><span class="sxs-lookup"><span data-stu-id="bb256-154">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bb256-155">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-155">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bb256-156">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-156">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bb256-157">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="bb256-157">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bb256-158">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bb256-158">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bb256-159">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bb256-159">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bb256-160">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="bb256-160">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bb256-161">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="bb256-161">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bb256-162">`[StorageProfileBackupRetentionDay <Int32?>]`: дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bb256-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="bb256-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bb256-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="bb256-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bb256-165">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-165">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bb256-166">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="bb256-166">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bb256-167">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="bb256-167">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bb256-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb256-168">RELATED LINKS</span></span>

