---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735068"
---
# <span data-ttu-id="b49ea-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b49ea-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="b49ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b49ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b49ea-103">Получение пулов пакетов под указанной пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="b49ea-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b49ea-104">SYNTAX</span></span>

### <span data-ttu-id="b49ea-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b49ea-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b49ea-106">Номер</span><span class="sxs-lookup"><span data-stu-id="b49ea-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b49ea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b49ea-108">Командлет **Get-AzureBatchPool** возвращает пулы пакетов Azure под учетной записью пакетной службы, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="b49ea-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="b49ea-109">Вы можете использовать параметр *ID* для получения одного пула или с помощью параметра *Filter* , чтобы получить доступ к пулам, которые соответствуют фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b49ea-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b49ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b49ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b49ea-111">Пример 1: получение пула по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="b49ea-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="b49ea-112">Эта команда получает пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="b49ea-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="b49ea-113">Пример 2: получение всех пулов с помощью фильтра OData</span><span class="sxs-lookup"><span data-stu-id="b49ea-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="b49ea-114">Эта команда получает пулы, идентификаторы которых начинаются с "My", с помощью параметра " *Фильтр* ".</span><span class="sxs-lookup"><span data-stu-id="b49ea-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="b49ea-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b49ea-115">PARAMETERS</span></span>

### <span data-ttu-id="b49ea-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b49ea-116">-BatchContext</span></span>
<span data-ttu-id="b49ea-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b49ea-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b49ea-118">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b49ea-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b49ea-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="b49ea-119">-Expand</span></span>
<span data-ttu-id="b49ea-120">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="b49ea-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b49ea-121">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="b49ea-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="b49ea-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b49ea-122">-Filter</span></span>
<span data-ttu-id="b49ea-123">Задает предложение фильтра OData для использования при запросе пулов.</span><span class="sxs-lookup"><span data-stu-id="b49ea-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="b49ea-124">Если фильтр не указан, возвращаются все пулы под учетной записью пакета, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="b49ea-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="b49ea-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b49ea-125">-Id</span></span>
<span data-ttu-id="b49ea-126">Указывает идентификатор пула, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b49ea-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="b49ea-127">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="b49ea-127">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b49ea-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b49ea-128">-MaxCount</span></span>
<span data-ttu-id="b49ea-129">Задает максимальное количество возвращаемых пулов.</span><span class="sxs-lookup"><span data-stu-id="b49ea-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="b49ea-130">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="b49ea-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b49ea-131">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="b49ea-131">The default value is 1000.</span></span>

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

### <span data-ttu-id="b49ea-132">-SELECT</span><span class="sxs-lookup"><span data-stu-id="b49ea-132">-Select</span></span>
<span data-ttu-id="b49ea-133">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="b49ea-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="b49ea-134">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="b49ea-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b49ea-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49ea-135">-DefaultProfile</span></span>
<span data-ttu-id="b49ea-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b49ea-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49ea-137">CommonParameters</span></span>
<span data-ttu-id="b49ea-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b49ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49ea-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49ea-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49ea-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b49ea-140">INPUTS</span></span>

### <span data-ttu-id="b49ea-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b49ea-141">BatchAccountContext</span></span>
<span data-ttu-id="b49ea-142">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b49ea-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b49ea-143">Подстрок</span><span class="sxs-lookup"><span data-stu-id="b49ea-143">String</span></span>
<span data-ttu-id="b49ea-144">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b49ea-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b49ea-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49ea-145">OUTPUTS</span></span>

### <span data-ttu-id="b49ea-146">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="b49ea-146">PSCloudPool</span></span>

## <span data-ttu-id="b49ea-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b49ea-147">NOTES</span></span>

## <span data-ttu-id="b49ea-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b49ea-148">RELATED LINKS</span></span>

[<span data-ttu-id="b49ea-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b49ea-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b49ea-150">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b49ea-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="b49ea-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b49ea-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="b49ea-152">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b49ea-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


