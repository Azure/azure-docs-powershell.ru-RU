---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: 76e7cd3f61e4d7708481f6296be24ff12b6de3f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953587"
---
# <span data-ttu-id="bc857-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="bc857-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="bc857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc857-102">SYNOPSIS</span></span>
<span data-ttu-id="bc857-103">Восстановление сервера из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="bc857-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="bc857-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc857-104">SYNTAX</span></span>

### <span data-ttu-id="bc857-105">GeoRestore (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc857-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc857-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="bc857-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bc857-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc857-107">DESCRIPTION</span></span>
<span data-ttu-id="bc857-108">Восстановление сервера из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="bc857-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="bc857-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc857-109">EXAMPLES</span></span>

### <span data-ttu-id="bc857-110">Пример 1. Восстановление сервера PostgreSql с помощью GeoReplica Restore</span><span class="sxs-lookup"><span data-stu-id="bc857-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="bc857-111">Этот cmdlet restores PostgreSql server using GeoReplica Restore.</span><span class="sxs-lookup"><span data-stu-id="bc857-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="bc857-112">Пример 2. Восстановление сервера PostgreSql с помощью восстановления PointInTime</span><span class="sxs-lookup"><span data-stu-id="bc857-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="bc857-113">Эти cmdlets restore PostgreSql server using PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="bc857-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="bc857-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc857-114">PARAMETERS</span></span>

### <span data-ttu-id="bc857-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc857-115">-AsJob</span></span>
<span data-ttu-id="bc857-116">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="bc857-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="bc857-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc857-117">-DefaultProfile</span></span>
<span data-ttu-id="bc857-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc857-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc857-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc857-119">-InputObject</span></span>
<span data-ttu-id="bc857-120">Исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="bc857-120">The source server object to restore from.</span></span>
<span data-ttu-id="bc857-121">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="bc857-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-122">-Location</span><span class="sxs-lookup"><span data-stu-id="bc857-122">-Location</span></span>
<span data-ttu-id="bc857-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc857-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="bc857-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bc857-124">-Name</span></span>
<span data-ttu-id="bc857-125">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bc857-126">-NoWait</span></span>
<span data-ttu-id="bc857-127">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bc857-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="bc857-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc857-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc857-129">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="bc857-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="bc857-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="bc857-130">-RestorePointInTime</span></span>
<span data-ttu-id="bc857-131">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc857-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="bc857-132">-Sku</span></span>
<span data-ttu-id="bc857-133">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bc857-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bc857-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc857-134">-SubscriptionId</span></span>
<span data-ttu-id="bc857-135">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="bc857-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="bc857-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc857-136">-Tag</span></span>
<span data-ttu-id="bc857-137">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="bc857-137">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="bc857-138">-UseGeoRestore</span></span>
<span data-ttu-id="bc857-139">Восстановление с помощью георежима</span><span class="sxs-lookup"><span data-stu-id="bc857-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="bc857-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="bc857-141">Восстановление с помощью режима PointInTime</span><span class="sxs-lookup"><span data-stu-id="bc857-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc857-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc857-142">-Confirm</span></span>
<span data-ttu-id="bc857-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc857-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc857-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc857-144">-WhatIf</span></span>
<span data-ttu-id="bc857-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc857-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc857-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc857-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc857-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc857-147">CommonParameters</span></span>
<span data-ttu-id="bc857-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc857-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc857-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc857-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc857-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc857-150">INPUTS</span></span>

### <span data-ttu-id="bc857-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="bc857-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bc857-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc857-152">OUTPUTS</span></span>

### <span data-ttu-id="bc857-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="bc857-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="bc857-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc857-154">NOTES</span></span>

<span data-ttu-id="bc857-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bc857-155">ALIASES</span></span>

<span data-ttu-id="bc857-156">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bc857-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc857-157">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="bc857-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc857-158">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc857-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc857-159">INPUTOBJECT: <IServer> исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="bc857-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="bc857-160">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="bc857-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="bc857-161">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc857-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bc857-162">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="bc857-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bc857-163">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="bc857-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="bc857-164">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="bc857-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="bc857-165">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="bc857-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="bc857-166">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="bc857-167">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="bc857-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="bc857-168">Задайте для этого назначения ресурсу systemAssigned, чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc857-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="bc857-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="bc857-170">`[MasterServerId <String>]`. Он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="bc857-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="bc857-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="bc857-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`. Разрешен ли доступ к общедоступным сетям для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="bc857-173">Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".</span><span class="sxs-lookup"><span data-stu-id="bc857-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="bc857-174">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.</span><span class="sxs-lookup"><span data-stu-id="bc857-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="bc857-175">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="bc857-176">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="bc857-177">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="bc857-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="bc857-178">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bc857-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="bc857-179">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bc857-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="bc857-180">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="bc857-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="bc857-181">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="bc857-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="bc857-182">`[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.</span><span class="sxs-lookup"><span data-stu-id="bc857-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="bc857-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.</span><span class="sxs-lookup"><span data-stu-id="bc857-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="bc857-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="bc857-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="bc857-185">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="bc857-186">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="bc857-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="bc857-187">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="bc857-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="bc857-188">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc857-188">RELATED LINKS</span></span>

