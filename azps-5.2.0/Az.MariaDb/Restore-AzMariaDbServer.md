---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411028"
---
# <span data-ttu-id="4c762-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="4c762-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="4c762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c762-102">SYNOPSIS</span></span>
<span data-ttu-id="4c762-103">Восстановление MariaDB из существующей системы MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4c762-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="4c762-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c762-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c762-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c762-105">DESCRIPTION</span></span>
<span data-ttu-id="4c762-106">Восстановление MariaDB из существующей системы MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4c762-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="4c762-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c762-107">EXAMPLES</span></span>

### <span data-ttu-id="4c762-108">Пример 1. Восстановление имени сервера PointInTime MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4c762-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4c762-109">Эта команда восстанавливает имя сервера PointInTime MariaDB.</span><span class="sxs-lookup"><span data-stu-id="4c762-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="4c762-110">Пример 2. Восстановление объекта PointInTime MariaDB с помощью объекта сервера</span><span class="sxs-lookup"><span data-stu-id="4c762-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4c762-111">Эта команда восстанавливает точку PointInTime MariaDB с помощью объекта-сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="4c762-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c762-112">PARAMETERS</span></span>

### <span data-ttu-id="4c762-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c762-113">-AsJob</span></span>
<span data-ttu-id="4c762-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4c762-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4c762-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c762-115">-DefaultProfile</span></span>
<span data-ttu-id="4c762-116">Region DefaultParameters— учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c762-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c762-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c762-117">-InputObject</span></span>
<span data-ttu-id="4c762-118">Исходный сервер, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="4c762-118">The source server object to restore from.</span></span>
<span data-ttu-id="4c762-119">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="4c762-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c762-120">-Location</span><span class="sxs-lookup"><span data-stu-id="4c762-120">-Location</span></span>
<span data-ttu-id="4c762-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c762-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="4c762-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4c762-122">-Name</span></span>
<span data-ttu-id="4c762-123">Имя сервера, из которого нужно восстановить имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="4c762-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4c762-124">-NoWait</span></span>
<span data-ttu-id="4c762-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4c762-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4c762-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c762-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c762-127">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="4c762-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4c762-128">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4c762-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4c762-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="4c762-129">-RestorePointInTime</span></span>
<span data-ttu-id="4c762-130">region PointInTimeRestore Расположение, где находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="4c762-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c762-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c762-131">-ServerName</span></span>
<span data-ttu-id="4c762-132">Имя сервера-источника, из которого нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="4c762-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="4c762-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c762-133">-SubscriptionId</span></span>
<span data-ttu-id="4c762-134">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c762-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4c762-135">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4c762-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4c762-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c762-136">-Tag</span></span>
<span data-ttu-id="4c762-137">Метаданные приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="4c762-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="4c762-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c762-138">-Confirm</span></span>
<span data-ttu-id="4c762-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4c762-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c762-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c762-140">-WhatIf</span></span>
<span data-ttu-id="4c762-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c762-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c762-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4c762-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c762-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c762-143">CommonParameters</span></span>
<span data-ttu-id="4c762-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c762-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c762-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c762-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c762-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c762-146">INPUTS</span></span>

### <span data-ttu-id="4c762-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="4c762-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4c762-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c762-148">OUTPUTS</span></span>

### <span data-ttu-id="4c762-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="4c762-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4c762-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c762-150">NOTES</span></span>

<span data-ttu-id="4c762-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4c762-151">ALIASES</span></span>

<span data-ttu-id="4c762-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4c762-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c762-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4c762-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c762-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c762-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c762-155">INPUTOBJECT: <IServer> исходный объект сервера, из который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="4c762-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="4c762-156">`Location <String>`. Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c762-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="4c762-157">`[Tag <ITrackedResourceTags>]`: метаданные конкретного приложения в виде пар ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="4c762-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="4c762-158">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="4c762-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4c762-159">`[AdministratorLogin <String>]`: имя администратора для входа на сервер.</span><span class="sxs-lookup"><span data-stu-id="4c762-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="4c762-160">Может быть указано только при создании сервера (и требуется для создания).</span><span class="sxs-lookup"><span data-stu-id="4c762-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="4c762-161">`[EarliestRestoreDate <DateTime?>]`: самое раннее время создания точки восстановления (формат ISO8601)</span><span class="sxs-lookup"><span data-stu-id="4c762-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="4c762-162">`[FullyQualifiedDomainName <String>]`: полное доменное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="4c762-163">`[IdentityType <IdentityType?>]`: Тип удостоверения.</span><span class="sxs-lookup"><span data-stu-id="4c762-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="4c762-164">Задайте для этого назначения "SystemAssigned", чтобы автоматически создать и назначить ресурсу главную сумму Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4c762-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="4c762-165">`[MasterServerId <String>]`. Он является для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="4c762-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="4c762-166">`[ReplicaCapacity <Int32?>]`: Максимальное количество реплик, которые может иметь этаго сервер.</span><span class="sxs-lookup"><span data-stu-id="4c762-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="4c762-167">`[ReplicationRole <String>]`: роль репликации сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="4c762-168">`[SkuCapacity <Int32?>]`: пропускная способность, представляющая вычислительные единицы сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="4c762-169">`[SkuFamily <String>]`: семейство оборудования.</span><span class="sxs-lookup"><span data-stu-id="4c762-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="4c762-170">`[SkuName <String>]`: название SKU, как правило, уровень + семья + ядер, например, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="4c762-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="4c762-171">`[SkuSize <String>]`: код размера, который должен быть интерпретируется ресурсом при необходимости.</span><span class="sxs-lookup"><span data-stu-id="4c762-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="4c762-172">`[SkuTier <SkuTier?>]`. Уровень конкретного SKU, например "Простой".</span><span class="sxs-lookup"><span data-stu-id="4c762-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="4c762-173">`[SslEnforcement <SslEnforcementEnum?>]`: включить или не включить ssl-при подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="4c762-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="4c762-174">`[StorageProfileBackupRetentionDay <Int32?>]`: дней резервного копирования для хранения на сервере.</span><span class="sxs-lookup"><span data-stu-id="4c762-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="4c762-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: включить гео избыточные или не архивные копии на сервере.</span><span class="sxs-lookup"><span data-stu-id="4c762-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="4c762-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: включить автоматическое рост хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c762-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="4c762-177">`[StorageProfileStorageMb <Int32?>]`: Максимальное хранилище, разрешенное для сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="4c762-178">`[UserVisibleState <ServerState?>]`Состояние сервера, которое видно пользователю.</span><span class="sxs-lookup"><span data-stu-id="4c762-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="4c762-179">`[Version <ServerVersion?>]`: Версия сервера.</span><span class="sxs-lookup"><span data-stu-id="4c762-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="4c762-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c762-180">RELATED LINKS</span></span>

