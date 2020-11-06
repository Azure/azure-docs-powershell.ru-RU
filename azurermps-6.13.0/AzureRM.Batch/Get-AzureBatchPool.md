---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 8f5a4aee0087f34769f099b6e9b44d249b53f7d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566850"
---
# <span data-ttu-id="09121-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="09121-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="09121-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09121-102">SYNOPSIS</span></span>
<span data-ttu-id="09121-103">Получение пулов пакетов под указанной пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="09121-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09121-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09121-104">SYNTAX</span></span>

### <span data-ttu-id="09121-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09121-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09121-106">Номер</span><span class="sxs-lookup"><span data-stu-id="09121-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09121-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09121-107">DESCRIPTION</span></span>
<span data-ttu-id="09121-108">Командлет **Get-AzureBatchPool** возвращает пулы пакетов Azure под учетной записью пакетной службы, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="09121-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="09121-109">Вы можете использовать параметр *ID* для получения одного пула или с помощью параметра *Filter* , чтобы получить доступ к пулам, которые соответствуют фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="09121-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="09121-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09121-110">EXAMPLES</span></span>

### <span data-ttu-id="09121-111">Пример 1: получение пула по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="09121-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="09121-112">Эта команда получает пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="09121-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="09121-113">Пример 2: получение всех пулов с помощью фильтра OData</span><span class="sxs-lookup"><span data-stu-id="09121-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="09121-114">Эта команда получает пулы, идентификаторы которых начинаются с "My", с помощью параметра " *Фильтр* ".</span><span class="sxs-lookup"><span data-stu-id="09121-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="09121-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09121-115">PARAMETERS</span></span>

### <span data-ttu-id="09121-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="09121-116">-BatchContext</span></span>
<span data-ttu-id="09121-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="09121-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="09121-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="09121-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="09121-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="09121-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="09121-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="09121-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="09121-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="09121-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="09121-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09121-122">-DefaultProfile</span></span>
<span data-ttu-id="09121-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09121-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09121-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="09121-124">-Expand</span></span>
<span data-ttu-id="09121-125">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="09121-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="09121-126">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="09121-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="09121-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="09121-127">-Filter</span></span>
<span data-ttu-id="09121-128">Задает предложение фильтра OData для использования при запросе пулов.</span><span class="sxs-lookup"><span data-stu-id="09121-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="09121-129">Если фильтр не указан, возвращаются все пулы под учетной записью пакета, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="09121-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="09121-130">-ID</span><span class="sxs-lookup"><span data-stu-id="09121-130">-Id</span></span>
<span data-ttu-id="09121-131">Указывает идентификатор пула, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="09121-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="09121-132">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="09121-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="09121-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="09121-133">-MaxCount</span></span>
<span data-ttu-id="09121-134">Задает максимальное количество возвращаемых пулов.</span><span class="sxs-lookup"><span data-stu-id="09121-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="09121-135">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="09121-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="09121-136">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="09121-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="09121-137">-SELECT</span><span class="sxs-lookup"><span data-stu-id="09121-137">-Select</span></span>
<span data-ttu-id="09121-138">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="09121-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="09121-139">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="09121-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="09121-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09121-140">CommonParameters</span></span>
<span data-ttu-id="09121-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09121-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09121-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09121-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09121-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09121-143">INPUTS</span></span>

### <span data-ttu-id="09121-144">System. String</span><span class="sxs-lookup"><span data-stu-id="09121-144">System.String</span></span>

### <span data-ttu-id="09121-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="09121-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="09121-146">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="09121-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="09121-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09121-147">OUTPUTS</span></span>

### <span data-ttu-id="09121-148">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="09121-148">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="09121-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="09121-149">NOTES</span></span>

## <span data-ttu-id="09121-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09121-150">RELATED LINKS</span></span>

[<span data-ttu-id="09121-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="09121-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="09121-152">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="09121-152">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="09121-153">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="09121-153">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="09121-154">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="09121-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


