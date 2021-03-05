---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982952"
---
# <span data-ttu-id="c2136-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="c2136-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="c2136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2136-102">SYNOPSIS</span></span>
<span data-ttu-id="c2136-103">Извлекает состояние задания миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="c2136-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="c2136-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2136-104">SYNTAX</span></span>

### <span data-ttu-id="c2136-105">ListByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2136-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2136-106">GetById</span><span class="sxs-lookup"><span data-stu-id="c2136-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2136-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2136-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2136-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="c2136-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c2136-109">ListById</span><span class="sxs-lookup"><span data-stu-id="c2136-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c2136-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2136-110">DESCRIPTION</span></span>
<span data-ttu-id="c2136-111">При Get-AzMigrateJob будет снова отознано состояние задания миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="c2136-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="c2136-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2136-112">EXAMPLES</span></span>

### <span data-ttu-id="c2136-113">Пример 1. "Получить по заданиям"</span><span class="sxs-lookup"><span data-stu-id="c2136-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c2136-114">Задание будет извлечено по его ИД.</span><span class="sxs-lookup"><span data-stu-id="c2136-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="c2136-115">Пример 2. Список по группе ресурсов и проекту</span><span class="sxs-lookup"><span data-stu-id="c2136-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c2136-116">Это все задания в проекте.</span><span class="sxs-lookup"><span data-stu-id="c2136-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="c2136-117">Пример 3. Группа ресурсов, проект и имя задания</span><span class="sxs-lookup"><span data-stu-id="c2136-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c2136-118">Это задание будет конкретным.</span><span class="sxs-lookup"><span data-stu-id="c2136-118">This gets a specific job.</span></span>

## <span data-ttu-id="c2136-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2136-119">PARAMETERS</span></span>

### <span data-ttu-id="c2136-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2136-120">-DefaultProfile</span></span>
<span data-ttu-id="c2136-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2136-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2136-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="c2136-122">-Filter</span></span>
<span data-ttu-id="c2136-123">Параметры фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c2136-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2136-124">-InputObject</span></span>
<span data-ttu-id="c2136-125">Определяет объект задания для сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c2136-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="c2136-126">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="c2136-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="c2136-127">-JobID</span></span>
<span data-ttu-id="c2136-128">Определяет ид задания, для которого требуется получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="c2136-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2136-129">-JobName</span></span>
<span data-ttu-id="c2136-130">Идентификатор задания</span><span class="sxs-lookup"><span data-stu-id="c2136-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="c2136-131">-ProjectID</span></span>
<span data-ttu-id="c2136-132">Определяет проект миграции Azure, в котором репликация серверов.</span><span class="sxs-lookup"><span data-stu-id="c2136-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c2136-133">-ProjectName</span></span>
<span data-ttu-id="c2136-134">Имя проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="c2136-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="c2136-135">-ResourceGroupID</span></span>
<span data-ttu-id="c2136-136">Группа ресурсов в azure Migrate Project в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c2136-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2136-137">-ResourceGroupName</span></span>
<span data-ttu-id="c2136-138">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="c2136-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2136-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2136-139">-SubscriptionId</span></span>
<span data-ttu-id="c2136-140">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c2136-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c2136-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2136-141">CommonParameters</span></span>
<span data-ttu-id="c2136-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2136-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2136-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2136-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2136-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2136-144">INPUTS</span></span>

## <span data-ttu-id="c2136-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2136-145">OUTPUTS</span></span>

### <span data-ttu-id="c2136-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c2136-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c2136-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2136-147">NOTES</span></span>

<span data-ttu-id="c2136-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c2136-148">ALIASES</span></span>

<span data-ttu-id="c2136-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c2136-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2136-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2136-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2136-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2136-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2136-152">INPUTOBJECT: <IJob> определяет объект задания сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="c2136-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="c2136-153">`[Location <String>]`: расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="c2136-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c2136-154">`[ActivityId <String>]`: ИД действия.</span><span class="sxs-lookup"><span data-stu-id="c2136-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="c2136-155">`[AllowedAction <String[]>]`Действие "Разрешено".</span><span class="sxs-lookup"><span data-stu-id="c2136-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="c2136-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: затронутые свойства объекта, такие как исходный сервер, источник облака, целевой сервер, целевое облако и т. д., на основе сведений о объекте рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="c2136-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="c2136-157">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="c2136-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c2136-158">`[EndTime <DateTime?>]`: время окончания.</span><span class="sxs-lookup"><span data-stu-id="c2136-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="c2136-159">`[Error <IJobErrorDetails[]>]`: Ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="c2136-160">`[CreationTime <DateTime?>]`: Время создания ошибки задания.</span><span class="sxs-lookup"><span data-stu-id="c2136-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="c2136-161">`[ErrorLevel <String>]`: Уровень ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="c2136-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="c2136-163">`[ProviderErrorDetailErrorId <String>]`: ИД ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="c2136-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="c2136-164">`[ProviderErrorDetailErrorMessage <String>]`: Сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c2136-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="c2136-165">`[ProviderErrorDetailPossibleCaus <String>]`: возможные причины возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="c2136-166">`[ProviderErrorDetailRecommendedAction <String>]`Рекомендуемое действие для устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="c2136-167">`[ServiceErrorDetailActivityId <String>]`: ИД действия.</span><span class="sxs-lookup"><span data-stu-id="c2136-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="c2136-168">`[ServiceErrorDetailCode <String>]`: Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="c2136-169">`[ServiceErrorDetailMessage <String>]`: сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c2136-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="c2136-170">`[ServiceErrorDetailPossibleCaus <String>]`: Возможные причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="c2136-171">`[ServiceErrorDetailRecommendedAction <String>]`: Рекомендуемое действие для устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="c2136-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="c2136-172">`[TaskId <String>]`: ИД задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="c2136-173">`[FriendlyName <String>]`: DisplayName.</span><span class="sxs-lookup"><span data-stu-id="c2136-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="c2136-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="c2136-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="c2136-175">`[StartTime <DateTime?>]`: время начала.</span><span class="sxs-lookup"><span data-stu-id="c2136-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="c2136-176">`[State <String>]`: Состояние задания.</span><span class="sxs-lookup"><span data-stu-id="c2136-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="c2136-177">Это одно из этих значений: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended или Other.</span><span class="sxs-lookup"><span data-stu-id="c2136-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="c2136-178">`[StateDescription <String>]`: Описание состояния задания.</span><span class="sxs-lookup"><span data-stu-id="c2136-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="c2136-179">Например: для состояния "Успешное состояние" описание может быть завершено, частично Сужение, CompletedWithInformation или Skipped.</span><span class="sxs-lookup"><span data-stu-id="c2136-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="c2136-180">`[TargetInstanceType <String>]`: Тип затронутого объекта— класс {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="c2136-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="c2136-181">`[TargetObjectId <String>]`: Затронутый ИД объекта.</span><span class="sxs-lookup"><span data-stu-id="c2136-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="c2136-182">`[TargetObjectName <String>]`: имя затронутого объекта.</span><span class="sxs-lookup"><span data-stu-id="c2136-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="c2136-183">`[Task <IAsrTask[]>]`Задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="c2136-184">`[AllowedAction <String[]>]`. Состояние или действия, применимые к данной задаче.</span><span class="sxs-lookup"><span data-stu-id="c2136-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="c2136-185">`[CustomDetailInstanceType <String>]`: Тип сведений о задаче.</span><span class="sxs-lookup"><span data-stu-id="c2136-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="c2136-186">`[EndTime <DateTime?>]`: время окончания.</span><span class="sxs-lookup"><span data-stu-id="c2136-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="c2136-187">`[Error <IJobErrorDetails[]>]`: Сведения об ошибке задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="c2136-188">`[FriendlyName <String>]`: Имя.</span><span class="sxs-lookup"><span data-stu-id="c2136-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="c2136-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Задачи ребенка.</span><span class="sxs-lookup"><span data-stu-id="c2136-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="c2136-190">`[GroupTaskCustomDetailInstanceType <String>]`: Тип сведений о задаче.</span><span class="sxs-lookup"><span data-stu-id="c2136-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="c2136-191">`[Name <String>]`: Уникальное имя задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="c2136-192">`[StartTime <DateTime?>]`: время начала.</span><span class="sxs-lookup"><span data-stu-id="c2136-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="c2136-193">`[State <String>]`: Штат.</span><span class="sxs-lookup"><span data-stu-id="c2136-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="c2136-194">Это одно из этих значений: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended или Other.</span><span class="sxs-lookup"><span data-stu-id="c2136-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="c2136-195">`[StateDescription <String>]`: Описание состояния задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="c2136-196">Например: для состояния "Успешное состояние" описание может быть завершено, частично Сужение, CompletedWithInformation или Skipped.</span><span class="sxs-lookup"><span data-stu-id="c2136-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="c2136-197">`[TaskId <String>]`: ИД.</span><span class="sxs-lookup"><span data-stu-id="c2136-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="c2136-198">`[TaskType <String>]`Тип задачи.</span><span class="sxs-lookup"><span data-stu-id="c2136-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="c2136-199">Сведения в свойстве CustomDetails зависят от этого типа.</span><span class="sxs-lookup"><span data-stu-id="c2136-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="c2136-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2136-200">RELATED LINKS</span></span>

