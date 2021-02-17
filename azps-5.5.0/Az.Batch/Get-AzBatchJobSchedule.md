---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239373"
---
# <span data-ttu-id="86a1e-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="86a1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="86a1e-103">Получает расписание пакетных рабочих мест.</span><span class="sxs-lookup"><span data-stu-id="86a1e-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="86a1e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86a1e-104">SYNTAX</span></span>

### <span data-ttu-id="86a1e-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86a1e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a1e-106">ИД</span><span class="sxs-lookup"><span data-stu-id="86a1e-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a1e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86a1e-107">DESCRIPTION</span></span>
<span data-ttu-id="86a1e-108">С **помощью cmdlet Get-AzBatchJobSchedule** можно получить расписание пакетных рабочих мест Azure для учетной записи batch, заданной *параметром BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="86a1e-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="86a1e-109">Укажите ИД для получения единого расписания работы.</span><span class="sxs-lookup"><span data-stu-id="86a1e-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="86a1e-110">Укажите *параметр Filter,* чтобы получить расписания задания, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="86a1e-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="86a1e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86a1e-111">EXAMPLES</span></span>

### <span data-ttu-id="86a1e-112">Пример 1. Поиск расписания работы с помощью задания</span><span class="sxs-lookup"><span data-stu-id="86a1e-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="86a1e-113">Эта команда возвращает расписание задания с расписанием задания ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="86a1e-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="86a1e-114">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="86a1e-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="86a1e-115">Пример 2. Поиск расписания работы с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="86a1e-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 :
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 :
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    :
PreviousState               : Invalid
PreviousStateTransitionTime :
Schedule                    :
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="86a1e-116">Эта команда получает все расписания работы с ИД, начинающиеся с задания, путем указания *параметра Filter.*</span><span class="sxs-lookup"><span data-stu-id="86a1e-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="86a1e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86a1e-117">PARAMETERS</span></span>

### <span data-ttu-id="86a1e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="86a1e-118">-BatchContext</span></span>
<span data-ttu-id="86a1e-119">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="86a1e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="86a1e-120">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="86a1e-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="86a1e-121">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="86a1e-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="86a1e-122">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86a1e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="86a1e-123">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="86a1e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86a1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a1e-124">-DefaultProfile</span></span>
<span data-ttu-id="86a1e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86a1e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a1e-126">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="86a1e-126">-Expand</span></span>
<span data-ttu-id="86a1e-127">Указывает предложение развернуть протокол Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="86a1e-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="86a1e-128">Укажите значение этого параметра, чтобы получить связанные объекты основной сущности, которую вы получаете.</span><span class="sxs-lookup"><span data-stu-id="86a1e-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="86a1e-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="86a1e-129">-Filter</span></span>
<span data-ttu-id="86a1e-130">Указывает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="86a1e-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="86a1e-131">Этот командлет возвращает расписания задания, которые соответствуют фильтру, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="86a1e-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="86a1e-132">Если не указать фильтр, этот cmdlet возвращает все расписания для контекста пакета.</span><span class="sxs-lookup"><span data-stu-id="86a1e-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a1e-133">-Id</span><span class="sxs-lookup"><span data-stu-id="86a1e-133">-Id</span></span>
<span data-ttu-id="86a1e-134">Определяет код расписания задания, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a1e-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="86a1e-135">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="86a1e-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86a1e-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="86a1e-136">-MaxCount</span></span>
<span data-ttu-id="86a1e-137">Определяет максимальное количество возвращаемых рабочих графиков.</span><span class="sxs-lookup"><span data-stu-id="86a1e-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="86a1e-138">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="86a1e-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="86a1e-139">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="86a1e-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a1e-140">-Select</span><span class="sxs-lookup"><span data-stu-id="86a1e-140">-Select</span></span>
<span data-ttu-id="86a1e-141">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="86a1e-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="86a1e-142">Укажите значение для этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="86a1e-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="86a1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a1e-143">CommonParameters</span></span>
<span data-ttu-id="86a1e-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a1e-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86a1e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a1e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86a1e-146">INPUTS</span></span>

### <span data-ttu-id="86a1e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="86a1e-147">System.String</span></span>

### <span data-ttu-id="86a1e-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="86a1e-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="86a1e-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86a1e-149">OUTPUTS</span></span>

### <span data-ttu-id="86a1e-150">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="86a1e-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86a1e-151">NOTES</span></span>

## <span data-ttu-id="86a1e-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86a1e-152">RELATED LINKS</span></span>

[<span data-ttu-id="86a1e-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="86a1e-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="86a1e-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="86a1e-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="86a1e-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="86a1e-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="86a1e-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="86a1e-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="86a1e-159">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="86a1e-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
