---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565271"
---
# <span data-ttu-id="6f71d-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6f71d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f71d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f71d-103">Получает расписания пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="6f71d-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f71d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f71d-104">SYNTAX</span></span>

### <span data-ttu-id="6f71d-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f71d-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f71d-106">Номер</span><span class="sxs-lookup"><span data-stu-id="6f71d-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f71d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f71d-107">DESCRIPTION</span></span>
<span data-ttu-id="6f71d-108">Командлет **Get-AzureBatchJobSchedule** получает расписания пакетных заданий Azure для учетной записи пакетной службы, указанной параметром *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="6f71d-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="6f71d-109">Укажите идентификатор для получения одного расписания задания.</span><span class="sxs-lookup"><span data-stu-id="6f71d-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="6f71d-110">Укажите параметр *фильтра* для получения расписаний заданий, соответствующих фильтру протокола OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="6f71d-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6f71d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f71d-111">EXAMPLES</span></span>

### <span data-ttu-id="6f71d-112">Пример 1: получение расписания задания с указанием идентификатора</span><span class="sxs-lookup"><span data-stu-id="6f71d-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="6f71d-113">Эта команда получает расписание задания с ИДЕНТИФИКАТОРом JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="6f71d-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="6f71d-114">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="6f71d-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6f71d-115">Пример 2: получение расписаний заданий с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="6f71d-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="6f71d-116">Эта команда получает все расписания заданий с идентификаторами, которые начинаются с задания, указав параметр *фильтра* .</span><span class="sxs-lookup"><span data-stu-id="6f71d-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="6f71d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f71d-117">PARAMETERS</span></span>

### <span data-ttu-id="6f71d-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6f71d-118">-BatchContext</span></span>
<span data-ttu-id="6f71d-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="6f71d-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6f71d-120">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="6f71d-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6f71d-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="6f71d-121">-Expand</span></span>
<span data-ttu-id="6f71d-122">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="6f71d-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="6f71d-123">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="6f71d-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="6f71d-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="6f71d-124">-Filter</span></span>
<span data-ttu-id="6f71d-125">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="6f71d-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="6f71d-126">Этот командлет возвращает расписания заданий, соответствующие фильтру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="6f71d-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="6f71d-127">Если фильтр не указан, этот командлет возвращает все расписания заданий для контекста пакета.</span><span class="sxs-lookup"><span data-stu-id="6f71d-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="6f71d-128">-ID</span><span class="sxs-lookup"><span data-stu-id="6f71d-128">-Id</span></span>
<span data-ttu-id="6f71d-129">Указывает идентификатор расписания задания, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f71d-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="6f71d-130">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="6f71d-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="6f71d-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6f71d-131">-MaxCount</span></span>
<span data-ttu-id="6f71d-132">Задает максимальное количество возвращаемых расписаний задач.</span><span class="sxs-lookup"><span data-stu-id="6f71d-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="6f71d-133">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="6f71d-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6f71d-134">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="6f71d-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="6f71d-135">-SELECT</span><span class="sxs-lookup"><span data-stu-id="6f71d-135">-Select</span></span>
<span data-ttu-id="6f71d-136">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="6f71d-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="6f71d-137">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="6f71d-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6f71d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f71d-138">-DefaultProfile</span></span>
<span data-ttu-id="6f71d-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f71d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f71d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f71d-140">CommonParameters</span></span>
<span data-ttu-id="6f71d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f71d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f71d-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f71d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f71d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f71d-143">INPUTS</span></span>

### <span data-ttu-id="6f71d-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6f71d-144">BatchAccountContext</span></span>
<span data-ttu-id="6f71d-145">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6f71d-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6f71d-146">Подстрок</span><span class="sxs-lookup"><span data-stu-id="6f71d-146">String</span></span>
<span data-ttu-id="6f71d-147">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6f71d-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6f71d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f71d-148">OUTPUTS</span></span>

### <span data-ttu-id="6f71d-149">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="6f71d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f71d-150">NOTES</span></span>

## <span data-ttu-id="6f71d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f71d-151">RELATED LINKS</span></span>

[<span data-ttu-id="6f71d-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6f71d-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6f71d-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6f71d-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6f71d-155">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6f71d-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="6f71d-157">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6f71d-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="6f71d-158">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="6f71d-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


