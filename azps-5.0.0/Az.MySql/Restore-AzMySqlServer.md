---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246577"
---
# <span data-ttu-id="ccc9f-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="ccc9f-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="ccc9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc9f-103">Восстановление сервера из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="ccc9f-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="ccc9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccc9f-104">SYNTAX</span></span>

### <span data-ttu-id="ccc9f-105">Геовосстановление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccc9f-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ccc9f-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="ccc9f-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ccc9f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-107">DESCRIPTION</span></span>
<span data-ttu-id="ccc9f-108">Восстановление сервера из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="ccc9f-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="ccc9f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-109">EXAMPLES</span></span>

### <span data-ttu-id="ccc9f-110">Пример 1. Восстановление сервера MySql с помощью геореплики</span><span class="sxs-lookup"><span data-stu-id="ccc9f-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ccc9f-111">Этот командлет восстанавливает сервер MySql с помощью георепликового восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="ccc9f-112">Пример 2: восстановление сервера MySql с помощью PointInTime Restore</span><span class="sxs-lookup"><span data-stu-id="ccc9f-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="ccc9f-113">Эти командлеты восстанавливают сервер MySql с помощью PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="ccc9f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-114">PARAMETERS</span></span>

### <span data-ttu-id="ccc9f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccc9f-115">-AsJob</span></span>
<span data-ttu-id="ccc9f-116">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="ccc9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc9f-117">-DefaultProfile</span></span>
<span data-ttu-id="ccc9f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc9f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccc9f-119">-InputObject</span></span>
<span data-ttu-id="ccc9f-120">Исходный объект сервера, из которого нужно выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-120">The source server object to restore from.</span></span>
<span data-ttu-id="ccc9f-121">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc9f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="ccc9f-122">-Location</span></span>
<span data-ttu-id="ccc9f-123">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ccc9f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccc9f-124">-Name</span></span>
<span data-ttu-id="ccc9f-125">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-125">The name of the server.</span></span>

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

### <span data-ttu-id="ccc9f-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="ccc9f-126">-NoWait</span></span>
<span data-ttu-id="ccc9f-127">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ccc9f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc9f-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccc9f-129">Имя группы ресурсов, содержащей ресурс, это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ccc9f-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="ccc9f-130">-RestorePointInTime</span></span>
<span data-ttu-id="ccc9f-131">Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ccc9f-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="ccc9f-132">-Sku</span></span>
<span data-ttu-id="ccc9f-133">Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ccc9f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccc9f-134">-SubscriptionId</span></span>
<span data-ttu-id="ccc9f-135">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ccc9f-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="ccc9f-136">-Tag</span></span>
<span data-ttu-id="ccc9f-137">Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ccc9f-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ccc9f-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="ccc9f-138">-UseGeoRestore</span></span>
<span data-ttu-id="ccc9f-139">Восстановление с помощью географического режима</span><span class="sxs-lookup"><span data-stu-id="ccc9f-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="ccc9f-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="ccc9f-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="ccc9f-141">Восстановление с помощью режима PointInTime</span><span class="sxs-lookup"><span data-stu-id="ccc9f-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="ccc9f-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccc9f-142">-Confirm</span></span>
<span data-ttu-id="ccc9f-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccc9f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccc9f-144">-WhatIf</span></span>
<span data-ttu-id="ccc9f-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccc9f-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccc9f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc9f-147">CommonParameters</span></span>
<span data-ttu-id="ccc9f-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc9f-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccc9f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc9f-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccc9f-150">INPUTS</span></span>

### <span data-ttu-id="ccc9f-151">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ccc9f-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ccc9f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-152">OUTPUTS</span></span>

### <span data-ttu-id="ccc9f-153">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="ccc9f-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ccc9f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccc9f-154">NOTES</span></span>

<span data-ttu-id="ccc9f-155">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-155">ALIASES</span></span>

<span data-ttu-id="ccc9f-156">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ccc9f-157">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ccc9f-158">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ccc9f-159">INPUTOBJECT <IServer> : исходный серверный объект для восстановления.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="ccc9f-160">`Location <String>`: Расположение, в котором находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="ccc9f-161">`[Tag <ITrackedResourceTags>]`: Метаданные, зависящие от приложения, в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="ccc9f-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="ccc9f-162">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ccc9f-163">`[AdministratorLogin <String>]`: Имя для входа на сервер, на котором находится администратор.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ccc9f-164">Может быть указан только в том случае, если сервер создается (и является обязательным для создания).</span><span class="sxs-lookup"><span data-stu-id="ccc9f-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ccc9f-165">`[EarliestRestoreDate <DateTime?>]`: Самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="ccc9f-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ccc9f-166">`[FullyQualifiedDomainName <String>]`: Полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ccc9f-167">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ccc9f-168">Задайте для этого свойства значение "SystemAssigned", чтобы автоматически создать и назначить участника Azure Active Directory для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ccc9f-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Состояние, показывающее, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="ccc9f-170">`[MasterServerId <String>]`: Идентификатор главного сервера для сервера-реплики.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ccc9f-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Принудительная минимальная версия TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="ccc9f-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Разрешены ли доступ к общедоступной сети для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="ccc9f-173">Значение не является обязательным, но если оно передано, должно быть включено или отключено</span><span class="sxs-lookup"><span data-stu-id="ccc9f-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="ccc9f-174">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь главный сервер.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ccc9f-175">`[ReplicationRole <String>]`: Роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ccc9f-176">`[SkuCapacity <Int32?>]`: Масштабирование и уменьшение производительности, представляющие вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ccc9f-177">`[SkuFamily <String>]`: Семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ccc9f-178">`[SkuName <String>]`: Название SKU, обычно — «уровни + семейство + ядра», например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ccc9f-179">`[SkuSize <String>]`: Код размера, который должен обрабатываться ресурсом соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ccc9f-180">`[SkuTier <SkuTier?>]`: Уровень определенного SKU, например Basic.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ccc9f-181">`[SslEnforcement <SslEnforcementEnum?>]`: Включение принудительного применения SSL или не при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ccc9f-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Срок хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ccc9f-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Включение геоизбыточного резервирования или не для резервного копирования сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ccc9f-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Включите автоматическое расширение хранилища.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ccc9f-185">`[StorageProfileStorageMb <Int32?>]`: Максимальный объем хранилища, разрешенный для сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ccc9f-186">`[UserVisibleState <ServerState?>]`: Состояние сервера, доступного для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ccc9f-187">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ccc9f-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccc9f-188">RELATED LINKS</span></span>

