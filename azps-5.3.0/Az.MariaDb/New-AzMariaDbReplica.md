---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507138"
---
# <span data-ttu-id="25897-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="25897-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="25897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25897-102">SYNOPSIS</span></span>
<span data-ttu-id="25897-103">Создает реплику сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="25897-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25897-104">SYNTAX</span></span>

### <span data-ttu-id="25897-105">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25897-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25897-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="25897-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="25897-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25897-107">DESCRIPTION</span></span>
<span data-ttu-id="25897-108">Создает реплику сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="25897-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25897-109">EXAMPLES</span></span>

### <span data-ttu-id="25897-110">Пример 1. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="25897-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="25897-111">Эта команда создает копию DB для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="25897-112">Пример 2. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="25897-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="25897-113">Эта команда создает копию DB для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="25897-114">Пример 3. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="25897-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="25897-115">Эта команда с параметром inputobject создает копию db с параметром inputobject для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="25897-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25897-116">PARAMETERS</span></span>

### <span data-ttu-id="25897-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25897-117">-AsJob</span></span>
<span data-ttu-id="25897-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="25897-118">Run the command as a job</span></span>

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

### <span data-ttu-id="25897-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25897-119">-DefaultProfile</span></span>
<span data-ttu-id="25897-120">Region DefaultParameters The credentials, account, tenant и subscription, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25897-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25897-121">-Location</span><span class="sxs-lookup"><span data-stu-id="25897-121">-Location</span></span>
<span data-ttu-id="25897-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="25897-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="25897-123">-Master</span><span class="sxs-lookup"><span data-stu-id="25897-123">-Master</span></span>
<span data-ttu-id="25897-124">Исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="25897-124">The source server object to restore from.</span></span>
<span data-ttu-id="25897-125">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств MASTER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="25897-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25897-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="25897-126">-MasterName</span></span>
<span data-ttu-id="25897-127">Имя сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="25897-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25897-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25897-128">-NoWait</span></span>
<span data-ttu-id="25897-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="25897-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25897-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="25897-130">-ReplicaName</span></span>
<span data-ttu-id="25897-131">Имя реплики.</span><span class="sxs-lookup"><span data-stu-id="25897-131">Replica name.</span></span>

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

### <span data-ttu-id="25897-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25897-132">-ResourceGroupName</span></span>
<span data-ttu-id="25897-133">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="25897-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25897-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="25897-134">-Sku</span></span>
<span data-ttu-id="25897-135">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="25897-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="25897-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25897-136">-SubscriptionId</span></span>
<span data-ttu-id="25897-137">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="25897-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25897-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="25897-138">-Tag</span></span>
<span data-ttu-id="25897-139">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="25897-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="25897-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25897-140">-Confirm</span></span>
<span data-ttu-id="25897-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25897-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25897-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25897-142">-WhatIf</span></span>
<span data-ttu-id="25897-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25897-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25897-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="25897-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25897-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25897-145">CommonParameters</span></span>
<span data-ttu-id="25897-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25897-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25897-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25897-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25897-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25897-148">INPUTS</span></span>

### <span data-ttu-id="25897-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="25897-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="25897-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25897-150">OUTPUTS</span></span>

### <span data-ttu-id="25897-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="25897-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="25897-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25897-152">NOTES</span></span>

<span data-ttu-id="25897-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="25897-153">ALIASES</span></span>

<span data-ttu-id="25897-154">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="25897-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25897-155">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="25897-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25897-156">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25897-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25897-157">MASTER: <IServer> исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="25897-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="25897-158">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="25897-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="25897-159">`[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="25897-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="25897-160">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="25897-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="25897-161">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="25897-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="25897-162">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="25897-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="25897-163">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="25897-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="25897-164">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="25897-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="25897-165">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="25897-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="25897-166">Задайте для этого назначения ресурсу systemAssigned, чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25897-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="25897-167">`[MasterServerId <String>]`: он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="25897-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="25897-168">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.</span><span class="sxs-lookup"><span data-stu-id="25897-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="25897-169">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="25897-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="25897-170">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="25897-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="25897-171">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="25897-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="25897-172">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="25897-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="25897-173">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="25897-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="25897-174">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="25897-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="25897-175">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="25897-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="25897-176">`[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.</span><span class="sxs-lookup"><span data-stu-id="25897-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="25897-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.</span><span class="sxs-lookup"><span data-stu-id="25897-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="25897-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="25897-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="25897-179">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="25897-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="25897-180">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="25897-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="25897-181">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="25897-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="25897-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25897-182">RELATED LINKS</span></span>

