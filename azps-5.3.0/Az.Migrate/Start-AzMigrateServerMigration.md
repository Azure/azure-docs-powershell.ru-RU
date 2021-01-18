---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505074"
---
# <span data-ttu-id="c6c20-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="c6c20-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="c6c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c20-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c20-103">Запускает миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c6c20-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="c6c20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6c20-104">SYNTAX</span></span>

### <span data-ttu-id="c6c20-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6c20-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6c20-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c6c20-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c6c20-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6c20-107">DESCRIPTION</span></span>
<span data-ttu-id="c6c20-108">Запускает миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c6c20-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="c6c20-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6c20-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c20-110">Пример 1. По id</span><span class="sxs-lookup"><span data-stu-id="c6c20-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c6c20-111">По id</span><span class="sxs-lookup"><span data-stu-id="c6c20-111">By id</span></span>

## <span data-ttu-id="c6c20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6c20-112">PARAMETERS</span></span>

### <span data-ttu-id="c6c20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c20-113">-DefaultProfile</span></span>
<span data-ttu-id="c6c20-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c20-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6c20-115">-InputObject</span></span>
<span data-ttu-id="c6c20-116">Указывает сервер репликации, для которого нужно инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="c6c20-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="c6c20-117">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="c6c20-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c6c20-118">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="c6c20-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c20-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6c20-119">-SubscriptionId</span></span>
<span data-ttu-id="c6c20-120">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c20-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c6c20-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c6c20-121">-TargetObjectID</span></span>
<span data-ttu-id="c6c20-122">Указывает реплицирующий сервер, для которого нужно инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="c6c20-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="c6c20-123">Код должен быть извлечен с помощью Get-AzMigrateServerReplication-управления.</span><span class="sxs-lookup"><span data-stu-id="c6c20-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c20-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="c6c20-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="c6c20-125">Определяет, следует ли отключить исходный сервер после миграции.</span><span class="sxs-lookup"><span data-stu-id="c6c20-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="c6c20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c20-126">CommonParameters</span></span>
<span data-ttu-id="c6c20-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c20-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6c20-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c20-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c20-129">INPUTS</span></span>

## <span data-ttu-id="c6c20-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6c20-130">OUTPUTS</span></span>

### <span data-ttu-id="c6c20-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c6c20-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c6c20-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6c20-132">NOTES</span></span>

<span data-ttu-id="c6c20-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c6c20-133">ALIASES</span></span>

<span data-ttu-id="c6c20-134">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c6c20-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6c20-135">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c6c20-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6c20-136">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6c20-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6c20-137">INPUTOBJECT: определяет сервер репликации, для которого <IMigrationItem> нужно инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="c6c20-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="c6c20-138">Объект сервера можно извлечь с помощью Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="c6c20-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c6c20-139">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="c6c20-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c6c20-140">`[CurrentJobId <String>]`: ARM ид задания.</span><span class="sxs-lookup"><span data-stu-id="c6c20-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c6c20-141">`[CurrentJobName <String>]`: имя задания.</span><span class="sxs-lookup"><span data-stu-id="c6c20-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c6c20-142">`[CurrentJobStartTime <DateTime?>]`. Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="c6c20-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c6c20-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`. Настраиваемые параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="c6c20-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="c6c20-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6c20-144">RELATED LINKS</span></span>

