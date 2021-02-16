---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 58158888b99a5f4662de7530576eca084f849966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241200"
---
# <span data-ttu-id="2ae56-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="2ae56-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="2ae56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ae56-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae56-103">Создает новую реплику из существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="2ae56-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="2ae56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ae56-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2ae56-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ae56-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae56-106">Создает новую реплику из существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="2ae56-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="2ae56-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ae56-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae56-108">Пример 1. Создание репликации сервера MySql</span><span class="sxs-lookup"><span data-stu-id="2ae56-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="2ae56-109">Этот cmdlet создает новую реплику сервера MySql Server.</span><span class="sxs-lookup"><span data-stu-id="2ae56-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="2ae56-110">Пример 2. Создание репликации сервера MySql</span><span class="sxs-lookup"><span data-stu-id="2ae56-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="2ae56-111">Этот cmdlet with parameter master(inputobject) создает новую реплику сервера MySql.</span><span class="sxs-lookup"><span data-stu-id="2ae56-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="2ae56-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ae56-112">PARAMETERS</span></span>

### <span data-ttu-id="2ae56-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ae56-113">-AsJob</span></span>
<span data-ttu-id="2ae56-114">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="2ae56-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="2ae56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae56-115">-DefaultProfile</span></span>
<span data-ttu-id="2ae56-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ae56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae56-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2ae56-117">-Location</span></span>
<span data-ttu-id="2ae56-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2ae56-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2ae56-119">-Master</span><span class="sxs-lookup"><span data-stu-id="2ae56-119">-Master</span></span>
<span data-ttu-id="2ae56-120">Исходный серверный объект для создания репликации.</span><span class="sxs-lookup"><span data-stu-id="2ae56-120">The source server object to create replica from.</span></span>
<span data-ttu-id="2ae56-121">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств MASTER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2ae56-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae56-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ae56-122">-NoWait</span></span>
<span data-ttu-id="2ae56-123">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="2ae56-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2ae56-124">-Репликация</span><span class="sxs-lookup"><span data-stu-id="2ae56-124">-Replica</span></span>
<span data-ttu-id="2ae56-125">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-125">The name of the server.</span></span>

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

### <span data-ttu-id="2ae56-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae56-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ae56-127">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="2ae56-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2ae56-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ae56-128">-Sku</span></span>
<span data-ttu-id="2ae56-129">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2ae56-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="2ae56-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ae56-130">-SubscriptionId</span></span>
<span data-ttu-id="2ae56-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2ae56-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2ae56-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ae56-132">-Confirm</span></span>
<span data-ttu-id="2ae56-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2ae56-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae56-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae56-134">-WhatIf</span></span>
<span data-ttu-id="2ae56-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ae56-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae56-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2ae56-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae56-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae56-137">CommonParameters</span></span>
<span data-ttu-id="2ae56-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ae56-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae56-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ae56-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae56-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ae56-140">INPUTS</span></span>

### <span data-ttu-id="2ae56-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="2ae56-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2ae56-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ae56-142">OUTPUTS</span></span>

### <span data-ttu-id="2ae56-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="2ae56-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2ae56-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ae56-144">NOTES</span></span>

<span data-ttu-id="2ae56-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2ae56-145">ALIASES</span></span>

<span data-ttu-id="2ae56-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2ae56-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ae56-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae56-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ae56-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ae56-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ae56-149">MASTER: <IServer> исходный объект сервера для создания репликации.</span><span class="sxs-lookup"><span data-stu-id="2ae56-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="2ae56-150">`Location <String>`: географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="2ae56-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="2ae56-151">`[Tag <ITrackedResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ae56-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2ae56-152">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="2ae56-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2ae56-153">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="2ae56-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="2ae56-154">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="2ae56-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="2ae56-155">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="2ae56-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="2ae56-156">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="2ae56-157">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="2ae56-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="2ae56-158">Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ae56-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="2ae56-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`Состояние, показывающая, включено ли шифрование инфраструктуры сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="2ae56-160">`[MasterServerId <String>]`. Он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="2ae56-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="2ae56-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: привязйте минимальную версию TLS для сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="2ae56-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: разрешен ли доступ к общедоступным сетям для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="2ae56-163">Значение является необязательным, но если он передан, необходимо использовать значения "Включено" или "Отключено".</span><span class="sxs-lookup"><span data-stu-id="2ae56-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="2ae56-164">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.</span><span class="sxs-lookup"><span data-stu-id="2ae56-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="2ae56-165">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="2ae56-166">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="2ae56-167">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="2ae56-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="2ae56-168">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2ae56-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="2ae56-169">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="2ae56-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="2ae56-170">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="2ae56-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="2ae56-171">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="2ae56-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="2ae56-172">`[StorageProfileBackupRetentionDay <Int32?>]`: дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="2ae56-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.</span><span class="sxs-lookup"><span data-stu-id="2ae56-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="2ae56-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="2ae56-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="2ae56-175">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="2ae56-176">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="2ae56-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="2ae56-177">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="2ae56-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="2ae56-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ae56-178">RELATED LINKS</span></span>

