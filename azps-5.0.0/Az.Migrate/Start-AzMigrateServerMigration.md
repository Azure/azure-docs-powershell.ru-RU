---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248623"
---
# <span data-ttu-id="f67bb-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="f67bb-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="f67bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f67bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f67bb-103">Запускает миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="f67bb-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="f67bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f67bb-104">SYNTAX</span></span>

### <span data-ttu-id="f67bb-105">ByIDVMwareCbt (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f67bb-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f67bb-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="f67bb-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f67bb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f67bb-107">DESCRIPTION</span></span>
<span data-ttu-id="f67bb-108">Запускает миграцию для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="f67bb-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="f67bb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f67bb-109">EXAMPLES</span></span>

### <span data-ttu-id="f67bb-110">Пример 1: по идентификатору</span><span class="sxs-lookup"><span data-stu-id="f67bb-110">Example 1: By id</span></span>
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

<span data-ttu-id="f67bb-111">По идентификатору</span><span class="sxs-lookup"><span data-stu-id="f67bb-111">By id</span></span>

## <span data-ttu-id="f67bb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f67bb-112">PARAMETERS</span></span>

### <span data-ttu-id="f67bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67bb-113">-DefaultProfile</span></span>
<span data-ttu-id="f67bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f67bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f67bb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f67bb-115">-InputObject</span></span>
<span data-ttu-id="f67bb-116">Задает сервер репликации, для которого необходимо инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="f67bb-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="f67bb-117">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="f67bb-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="f67bb-118">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f67bb-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f67bb-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f67bb-119">-SubscriptionId</span></span>
<span data-ttu-id="f67bb-120">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="f67bb-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f67bb-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="f67bb-121">-TargetObjectID</span></span>
<span data-ttu-id="f67bb-122">Указывает сервер replcating, для которого необходимо инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="f67bb-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="f67bb-123">Идентификатор следует получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="f67bb-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="f67bb-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="f67bb-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="f67bb-125">Указывает, следует ли отключить сервер системы исходного кода после миграции.</span><span class="sxs-lookup"><span data-stu-id="f67bb-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="f67bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67bb-126">CommonParameters</span></span>
<span data-ttu-id="f67bb-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f67bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67bb-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f67bb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67bb-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f67bb-129">INPUTS</span></span>

## <span data-ttu-id="f67bb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f67bb-130">OUTPUTS</span></span>

### <span data-ttu-id="f67bb-131">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="f67bb-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="f67bb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f67bb-132">NOTES</span></span>

<span data-ttu-id="f67bb-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f67bb-133">ALIASES</span></span>

<span data-ttu-id="f67bb-134">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f67bb-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f67bb-135">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f67bb-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f67bb-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f67bb-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f67bb-137">INPUTOBJECT <IMigrationItem> : определяет сервер репликации, для которого необходимо инициировать миграцию.</span><span class="sxs-lookup"><span data-stu-id="f67bb-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="f67bb-138">Объект сервера можно получить с помощью командлета Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="f67bb-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="f67bb-139">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="f67bb-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="f67bb-140">`[CurrentJobId <String>]`: Идентификатор ARM выполняемого задания.</span><span class="sxs-lookup"><span data-stu-id="f67bb-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="f67bb-141">`[CurrentJobName <String>]`: Имя задания.</span><span class="sxs-lookup"><span data-stu-id="f67bb-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="f67bb-142">`[CurrentJobStartTime <DateTime?>]`: Время начала задания.</span><span class="sxs-lookup"><span data-stu-id="f67bb-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="f67bb-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Пользовательские параметры поставщика миграции.</span><span class="sxs-lookup"><span data-stu-id="f67bb-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="f67bb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f67bb-144">RELATED LINKS</span></span>

