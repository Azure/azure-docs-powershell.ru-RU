---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: c8b51f3822ce52fd21aa1d2b8df45d11108d713a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563131"
---
# <span data-ttu-id="694e6-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="694e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="694e6-102">SYNOPSIS</span></span>
<span data-ttu-id="694e6-103">Получает расписания пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="694e6-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="694e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="694e6-104">SYNTAX</span></span>

### <span data-ttu-id="694e6-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="694e6-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="694e6-106">Номер</span><span class="sxs-lookup"><span data-stu-id="694e6-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="694e6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="694e6-107">DESCRIPTION</span></span>
<span data-ttu-id="694e6-108">Командлет **Get-AzureBatchJobSchedule** получает расписания пакетных заданий Azure для учетной записи пакетной службы, указанной параметром *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="694e6-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="694e6-109">Укажите идентификатор для получения одного расписания задания.</span><span class="sxs-lookup"><span data-stu-id="694e6-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="694e6-110">Укажите параметр *фильтра* для получения расписаний заданий, соответствующих фильтру протокола OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="694e6-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="694e6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="694e6-111">EXAMPLES</span></span>

### <span data-ttu-id="694e6-112">Пример 1: получение расписания задания с указанием идентификатора</span><span class="sxs-lookup"><span data-stu-id="694e6-112">Example 1: Get a job schedule by specifying an ID</span></span>
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

<span data-ttu-id="694e6-113">Эта команда получает расписание задания с ИДЕНТИФИКАТОРом JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="694e6-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="694e6-114">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="694e6-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="694e6-115">Пример 2: получение расписаний заданий с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="694e6-115">Example 2: Get job schedules by using a filter</span></span>
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

<span data-ttu-id="694e6-116">Эта команда получает все расписания заданий с идентификаторами, которые начинаются с задания, указав параметр *фильтра* .</span><span class="sxs-lookup"><span data-stu-id="694e6-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="694e6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="694e6-117">PARAMETERS</span></span>

### <span data-ttu-id="694e6-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="694e6-118">-BatchContext</span></span>
<span data-ttu-id="694e6-119">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="694e6-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="694e6-120">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="694e6-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="694e6-121">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="694e6-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="694e6-122">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="694e6-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="694e6-123">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="694e6-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="694e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694e6-124">-DefaultProfile</span></span>
<span data-ttu-id="694e6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="694e6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694e6-126">-Expand</span><span class="sxs-lookup"><span data-stu-id="694e6-126">-Expand</span></span>
<span data-ttu-id="694e6-127">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="694e6-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="694e6-128">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="694e6-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="694e6-129">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="694e6-129">-Filter</span></span>
<span data-ttu-id="694e6-130">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="694e6-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="694e6-131">Этот командлет возвращает расписания заданий, соответствующие фильтру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="694e6-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="694e6-132">Если фильтр не указан, этот командлет возвращает все расписания заданий для контекста пакета.</span><span class="sxs-lookup"><span data-stu-id="694e6-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="694e6-133">-ID</span><span class="sxs-lookup"><span data-stu-id="694e6-133">-Id</span></span>
<span data-ttu-id="694e6-134">Указывает идентификатор расписания задания, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="694e6-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="694e6-135">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="694e6-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="694e6-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="694e6-136">-MaxCount</span></span>
<span data-ttu-id="694e6-137">Задает максимальное количество возвращаемых расписаний задач.</span><span class="sxs-lookup"><span data-stu-id="694e6-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="694e6-138">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="694e6-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="694e6-139">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="694e6-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="694e6-140">-SELECT</span><span class="sxs-lookup"><span data-stu-id="694e6-140">-Select</span></span>
<span data-ttu-id="694e6-141">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="694e6-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="694e6-142">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="694e6-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="694e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694e6-143">CommonParameters</span></span>
<span data-ttu-id="694e6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="694e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694e6-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694e6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694e6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="694e6-146">INPUTS</span></span>

### <span data-ttu-id="694e6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="694e6-147">System.String</span></span>

### <span data-ttu-id="694e6-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="694e6-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="694e6-149">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="694e6-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="694e6-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="694e6-150">OUTPUTS</span></span>

### <span data-ttu-id="694e6-151">Microsoft.Azure.Commands.BatCH. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-151">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="694e6-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="694e6-152">NOTES</span></span>

## <span data-ttu-id="694e6-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="694e6-153">RELATED LINKS</span></span>

[<span data-ttu-id="694e6-154">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-154">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="694e6-155">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-155">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="694e6-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="694e6-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="694e6-157">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-157">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="694e6-158">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-158">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="694e6-159">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="694e6-159">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="694e6-160">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="694e6-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


