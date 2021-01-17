---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405204"
---
# <span data-ttu-id="3da41-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="3da41-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="3da41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3da41-102">SYNOPSIS</span></span>
<span data-ttu-id="3da41-103">Создает реплику сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="3da41-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3da41-104">SYNTAX</span></span>

### <span data-ttu-id="3da41-105">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3da41-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3da41-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="3da41-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3da41-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3da41-107">DESCRIPTION</span></span>
<span data-ttu-id="3da41-108">Создает реплику сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="3da41-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3da41-109">EXAMPLES</span></span>

### <span data-ttu-id="3da41-110">Пример 1. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="3da41-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3da41-111">Эта команда создает копию DB для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="3da41-112">Пример 2. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="3da41-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3da41-113">Эта команда создает копию DB для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="3da41-114">Пример 3. Создание копии DB для MariaDB</span><span class="sxs-lookup"><span data-stu-id="3da41-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3da41-115">Эта команда с параметром inputobject создает копию db с параметром inputobject для MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="3da41-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3da41-116">PARAMETERS</span></span>

### <span data-ttu-id="3da41-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3da41-117">-AsJob</span></span>
<span data-ttu-id="3da41-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3da41-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3da41-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da41-119">-DefaultProfile</span></span>
<span data-ttu-id="3da41-120">Region DefaultParameters— учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3da41-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3da41-121">-Location</span><span class="sxs-lookup"><span data-stu-id="3da41-121">-Location</span></span>
<span data-ttu-id="3da41-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3da41-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3da41-123">-Master</span><span class="sxs-lookup"><span data-stu-id="3da41-123">-Master</span></span>
<span data-ttu-id="3da41-124">Исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="3da41-124">The source server object to restore from.</span></span>
<span data-ttu-id="3da41-125">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств MASTER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3da41-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3da41-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="3da41-126">-MasterName</span></span>
<span data-ttu-id="3da41-127">Имя сервера MariaDB.</span><span class="sxs-lookup"><span data-stu-id="3da41-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="3da41-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3da41-128">-NoWait</span></span>
<span data-ttu-id="3da41-129">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3da41-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3da41-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="3da41-130">-ReplicaName</span></span>
<span data-ttu-id="3da41-131">Имя реплики.</span><span class="sxs-lookup"><span data-stu-id="3da41-131">Replica name.</span></span>

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

### <span data-ttu-id="3da41-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da41-132">-ResourceGroupName</span></span>
<span data-ttu-id="3da41-133">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="3da41-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3da41-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="3da41-134">-Sku</span></span>
<span data-ttu-id="3da41-135">Как правило, это название SKU уровня +family + cores, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="3da41-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="3da41-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3da41-136">-SubscriptionId</span></span>
<span data-ttu-id="3da41-137">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3da41-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3da41-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="3da41-138">-Tag</span></span>
<span data-ttu-id="3da41-139">Метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="3da41-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3da41-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3da41-140">-Confirm</span></span>
<span data-ttu-id="3da41-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da41-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da41-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da41-142">-WhatIf</span></span>
<span data-ttu-id="3da41-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da41-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da41-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3da41-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da41-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da41-145">CommonParameters</span></span>
<span data-ttu-id="3da41-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da41-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da41-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3da41-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da41-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3da41-148">INPUTS</span></span>

### <span data-ttu-id="3da41-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="3da41-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="3da41-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3da41-150">OUTPUTS</span></span>

### <span data-ttu-id="3da41-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="3da41-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="3da41-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3da41-152">NOTES</span></span>

<span data-ttu-id="3da41-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3da41-153">ALIASES</span></span>

<span data-ttu-id="3da41-154">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3da41-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3da41-155">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3da41-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3da41-156">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3da41-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3da41-157">MASTER: <IServer> исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="3da41-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="3da41-158">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3da41-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="3da41-159">`[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="3da41-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="3da41-160">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="3da41-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3da41-161">`[AdministratorLogin <String>]`. Имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="3da41-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="3da41-162">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="3da41-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="3da41-163">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="3da41-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="3da41-164">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="3da41-165">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="3da41-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="3da41-166">Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3da41-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="3da41-167">`[MasterServerId <String>]`. Он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="3da41-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="3da41-168">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этот сервер.</span><span class="sxs-lookup"><span data-stu-id="3da41-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="3da41-169">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="3da41-170">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="3da41-171">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="3da41-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="3da41-172">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="3da41-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="3da41-173">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3da41-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="3da41-174">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="3da41-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="3da41-175">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="3da41-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="3da41-176">`[StorageProfileBackupRetentionDay <Int32?>]`: дней хранения резервных копий для сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="3da41-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточное или не для резервного копирования на сервере.</span><span class="sxs-lookup"><span data-stu-id="3da41-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="3da41-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="3da41-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="3da41-179">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="3da41-180">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="3da41-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="3da41-181">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="3da41-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="3da41-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3da41-182">RELATED LINKS</span></span>

