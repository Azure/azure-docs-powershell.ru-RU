---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234823"
---
# <span data-ttu-id="cd38a-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="cd38a-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="cd38a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd38a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd38a-103">Создание новой реплики из существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="cd38a-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="cd38a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd38a-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd38a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd38a-105">DESCRIPTION</span></span>
<span data-ttu-id="cd38a-106">Создание новой реплики из существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="cd38a-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="cd38a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd38a-107">EXAMPLES</span></span>

### <span data-ttu-id="cd38a-108">Пример 1: создание новой реплики сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="cd38a-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cd38a-109">Этот командлет создает новую реплику сервера PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="cd38a-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="cd38a-110">Пример 2: создание новой реплики сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="cd38a-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cd38a-111">Этот командлет создает новую реплику сервера PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="cd38a-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="cd38a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd38a-112">PARAMETERS</span></span>

### <span data-ttu-id="cd38a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd38a-113">-AsJob</span></span>
<span data-ttu-id="cd38a-114">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="cd38a-114">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd38a-115">-DefaultProfile</span></span>
<span data-ttu-id="cd38a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd38a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd38a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cd38a-117">-Location</span></span>
<span data-ttu-id="cd38a-118">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd38a-118">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-119">-Master</span><span class="sxs-lookup"><span data-stu-id="cd38a-119">-Master</span></span>
<span data-ttu-id="cd38a-120">Исходный объект сервера, из которого создается реплика.</span><span class="sxs-lookup"><span data-stu-id="cd38a-120">The source server object to create replica from.</span></span>
<span data-ttu-id="cd38a-121">Для конструирования ознакомьтесь с разделом "Заметки" ЭТАЛОНных свойств и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="cd38a-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-122">-Wait</span><span class="sxs-lookup"><span data-stu-id="cd38a-122">-NoWait</span></span>
<span data-ttu-id="cd38a-123">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="cd38a-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="cd38a-124">-ReplicaName</span></span>
<span data-ttu-id="cd38a-125">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd38a-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd38a-127">Имя группы ресурсов, содержащей ресурс, это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="cd38a-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cd38a-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd38a-128">-Sku</span></span>
<span data-ttu-id="cd38a-129">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cd38a-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd38a-130">-SubscriptionId</span></span>
<span data-ttu-id="cd38a-131">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="cd38a-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd38a-132">-Confirm</span></span>
<span data-ttu-id="cd38a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd38a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd38a-134">-WhatIf</span></span>
<span data-ttu-id="cd38a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd38a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd38a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd38a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd38a-137">CommonParameters</span></span>
<span data-ttu-id="cd38a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd38a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd38a-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd38a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd38a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd38a-140">INPUTS</span></span>

### <span data-ttu-id="cd38a-141">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="cd38a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cd38a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd38a-142">OUTPUTS</span></span>

### <span data-ttu-id="cd38a-143">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="cd38a-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="cd38a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd38a-144">NOTES</span></span>

<span data-ttu-id="cd38a-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="cd38a-145">ALIASES</span></span>

<span data-ttu-id="cd38a-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cd38a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd38a-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd38a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd38a-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd38a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd38a-149">ОБРАЗЕЦ <IServer> : исходный объект сервера, из которого создается реплика.</span><span class="sxs-lookup"><span data-stu-id="cd38a-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="cd38a-150">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd38a-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cd38a-151">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="cd38a-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cd38a-152">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="cd38a-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cd38a-153">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="cd38a-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cd38a-154">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="cd38a-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cd38a-155">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="cd38a-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cd38a-156">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cd38a-157">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="cd38a-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cd38a-158">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd38a-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cd38a-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Состояние, показывающее, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="cd38a-160">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="cd38a-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cd38a-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Принудительная минимальная версия TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="cd38a-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Разрешены ли доступ к общедоступной сети для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="cd38a-163">Значение не является обязательным, но если оно передано, должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="cd38a-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="cd38a-164">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="cd38a-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cd38a-165">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cd38a-166">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cd38a-167">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="cd38a-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cd38a-168">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cd38a-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cd38a-169">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="cd38a-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cd38a-170">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="cd38a-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cd38a-171">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="cd38a-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cd38a-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cd38a-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cd38a-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="cd38a-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cd38a-175">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cd38a-176">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd38a-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cd38a-177">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="cd38a-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cd38a-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd38a-178">RELATED LINKS</span></span>
