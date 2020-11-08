---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250073"
---
# <span data-ttu-id="9df21-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="9df21-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="9df21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9df21-102">SYNOPSIS</span></span>
<span data-ttu-id="9df21-103">Получает состояние задания миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="9df21-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="9df21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9df21-104">SYNTAX</span></span>

### <span data-ttu-id="9df21-105">ListByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9df21-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9df21-106">GetById</span><span class="sxs-lookup"><span data-stu-id="9df21-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9df21-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9df21-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9df21-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="9df21-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9df21-109">ListById</span><span class="sxs-lookup"><span data-stu-id="9df21-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9df21-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9df21-110">DESCRIPTION</span></span>
<span data-ttu-id="9df21-111">Командлет Get-AzMigrateJob retrives состояние задания миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="9df21-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="9df21-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9df21-112">EXAMPLES</span></span>

### <span data-ttu-id="9df21-113">Пример 1: получение по идентификатору задания</span><span class="sxs-lookup"><span data-stu-id="9df21-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="9df21-114">Это извлекает задание по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="9df21-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="9df21-115">Пример 2: список по группе ресурсов и проекту</span><span class="sxs-lookup"><span data-stu-id="9df21-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="9df21-116">Это получает все задания в проекте.</span><span class="sxs-lookup"><span data-stu-id="9df21-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="9df21-117">Пример 3: "получить по группе ресурсов", названию проекта и должности</span><span class="sxs-lookup"><span data-stu-id="9df21-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="9df21-118">Это возвращает определенное задание.</span><span class="sxs-lookup"><span data-stu-id="9df21-118">This gets a specific job.</span></span>

## <span data-ttu-id="9df21-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9df21-119">PARAMETERS</span></span>

### <span data-ttu-id="9df21-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df21-120">-DefaultProfile</span></span>
<span data-ttu-id="9df21-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9df21-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9df21-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="9df21-122">-Filter</span></span>
<span data-ttu-id="9df21-123">Параметры фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="9df21-123">OData filter options.</span></span>

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

### <span data-ttu-id="9df21-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9df21-124">-InputObject</span></span>
<span data-ttu-id="9df21-125">Указывает объект Job сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="9df21-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="9df21-126">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9df21-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9df21-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="9df21-127">-JobID</span></span>
<span data-ttu-id="9df21-128">Указывает код задания, для которого требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="9df21-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="9df21-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="9df21-129">-JobName</span></span>
<span data-ttu-id="9df21-130">Идентификатор задания</span><span class="sxs-lookup"><span data-stu-id="9df21-130">Job identifier</span></span>

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

### <span data-ttu-id="9df21-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="9df21-131">-ProjectID</span></span>
<span data-ttu-id="9df21-132">Задает проект миграции Azure, в котором реплицируются серверы.</span><span class="sxs-lookup"><span data-stu-id="9df21-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="9df21-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9df21-133">-ProjectName</span></span>
<span data-ttu-id="9df21-134">Имя переносимого проекта.</span><span class="sxs-lookup"><span data-stu-id="9df21-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="9df21-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="9df21-135">-ResourceGroupID</span></span>
<span data-ttu-id="9df21-136">Указывает группу ресурсов для проекта миграции Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="9df21-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="9df21-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df21-137">-ResourceGroupName</span></span>
<span data-ttu-id="9df21-138">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9df21-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9df21-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9df21-139">-SubscriptionId</span></span>
<span data-ttu-id="9df21-140">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="9df21-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9df21-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df21-141">CommonParameters</span></span>
<span data-ttu-id="9df21-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9df21-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df21-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9df21-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df21-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9df21-144">INPUTS</span></span>

## <span data-ttu-id="9df21-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9df21-145">OUTPUTS</span></span>

### <span data-ttu-id="9df21-146">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="9df21-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="9df21-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="9df21-147">NOTES</span></span>

<span data-ttu-id="9df21-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9df21-148">ALIASES</span></span>

<span data-ttu-id="9df21-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9df21-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9df21-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9df21-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9df21-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9df21-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9df21-152">INPUTOBJECT <IJob> : определяет объект задания на сервере репликации.</span><span class="sxs-lookup"><span data-stu-id="9df21-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="9df21-153">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="9df21-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="9df21-154">`[ActivityId <String>]`: Идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="9df21-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="9df21-155">`[AllowedAction <String[]>]`: Разрешенное действие для задания.</span><span class="sxs-lookup"><span data-stu-id="9df21-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="9df21-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Такие свойства объекта, как исходный сервер, исходное облако, целевой сервер, целевое облако и т. п. основываются на данных объекта рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="9df21-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="9df21-157">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="9df21-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9df21-158">`[EndTime <DateTime?>]`: Время окончания.</span><span class="sxs-lookup"><span data-stu-id="9df21-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="9df21-159">`[Error <IJobErrorDetails[]>]`: Ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="9df21-160">`[CreationTime <DateTime?>]`: Время создания ошибки задания.</span><span class="sxs-lookup"><span data-stu-id="9df21-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="9df21-161">`[ErrorLevel <String>]`: Ошибка уровня ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="9df21-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="9df21-163">`[ProviderErrorDetailErrorId <String>]`: Идентификатор ошибки поставщика.</span><span class="sxs-lookup"><span data-stu-id="9df21-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="9df21-164">`[ProviderErrorDetailErrorMessage <String>]`: Сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9df21-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="9df21-165">`[ProviderErrorDetailPossibleCaus <String>]`: Возможные причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="9df21-166">`[ProviderErrorDetailRecommendedAction <String>]`: Рекомендуемое действие для устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="9df21-167">`[ServiceErrorDetailActivityId <String>]`: Идентификатор действия.</span><span class="sxs-lookup"><span data-stu-id="9df21-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="9df21-168">`[ServiceErrorDetailCode <String>]`: Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="9df21-169">`[ServiceErrorDetailMessage <String>]`: Сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9df21-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="9df21-170">`[ServiceErrorDetailPossibleCaus <String>]`: Возможные причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="9df21-171">`[ServiceErrorDetailRecommendedAction <String>]`: Рекомендуемое действие для устранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9df21-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="9df21-172">`[TaskId <String>]`: Идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="9df21-173">`[FriendlyName <String>]`: DisplayName.</span><span class="sxs-lookup"><span data-stu-id="9df21-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="9df21-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="9df21-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="9df21-175">`[StartTime <DateTime?>]`: Время начала.</span><span class="sxs-lookup"><span data-stu-id="9df21-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="9df21-176">`[State <String>]`: Состояние задания.</span><span class="sxs-lookup"><span data-stu-id="9df21-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="9df21-177">Это одно из следующих значений: "NotStarted", "выполняется", "успешно", "сбой", "отменено", "приостановлено", "</span><span class="sxs-lookup"><span data-stu-id="9df21-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="9df21-178">`[StateDescription <String>]`: Описание состояния задания.</span><span class="sxs-lookup"><span data-stu-id="9df21-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="9df21-179">Например, для состояния "успешно завершено" Описание может быть заполнено, PartiallySucceeded, CompletedWithInformation или пропущено.</span><span class="sxs-lookup"><span data-stu-id="9df21-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="9df21-180">`[TargetInstanceType <String>]`: Тип объекта, затрагиваемого классом {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="9df21-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="9df21-181">`[TargetObjectId <String>]`: Затронутый идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="9df21-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="9df21-182">`[TargetObjectName <String>]`: Имя затрагиваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="9df21-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="9df21-183">`[Task <IAsrTask[]>]`: Задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="9df21-184">`[AllowedAction <String[]>]`: Область или действия, применимые к этой задаче.</span><span class="sxs-lookup"><span data-stu-id="9df21-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="9df21-185">`[CustomDetailInstanceType <String>]`: Тип сведений о задаче.</span><span class="sxs-lookup"><span data-stu-id="9df21-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="9df21-186">`[EndTime <DateTime?>]`: Время окончания.</span><span class="sxs-lookup"><span data-stu-id="9df21-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="9df21-187">`[Error <IJobErrorDetails[]>]`: Подробные сведения об ошибке задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="9df21-188">`[FriendlyName <String>]`: Имя.</span><span class="sxs-lookup"><span data-stu-id="9df21-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="9df21-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Дочерние задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="9df21-190">`[GroupTaskCustomDetailInstanceType <String>]`: Тип сведений о задаче.</span><span class="sxs-lookup"><span data-stu-id="9df21-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="9df21-191">`[Name <String>]`: Уникальное название задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="9df21-192">`[StartTime <DateTime?>]`: Время начала.</span><span class="sxs-lookup"><span data-stu-id="9df21-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="9df21-193">`[State <String>]`: Состояние.</span><span class="sxs-lookup"><span data-stu-id="9df21-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="9df21-194">Это одно из следующих значений: "NotStarted", "выполняется", "успешно", "сбой", "отменено", "приостановлено", "</span><span class="sxs-lookup"><span data-stu-id="9df21-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="9df21-195">`[StateDescription <String>]`: Описание состояния задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="9df21-196">Например, для состояния "успешно завершено" Описание может быть заполнено, PartiallySucceeded, CompletedWithInformation или пропущено.</span><span class="sxs-lookup"><span data-stu-id="9df21-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="9df21-197">`[TaskId <String>]`: Идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9df21-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="9df21-198">`[TaskType <String>]`: Тип задачи.</span><span class="sxs-lookup"><span data-stu-id="9df21-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="9df21-199">Сведения в свойстве CustomDetails зависят от этого типа.</span><span class="sxs-lookup"><span data-stu-id="9df21-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="9df21-200">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9df21-200">RELATED LINKS</span></span>

