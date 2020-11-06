---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559343"
---
# <span data-ttu-id="34c51-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="34c51-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="34c51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34c51-102">SYNOPSIS</span></span>
<span data-ttu-id="34c51-103">Получение пулов пакетов под указанной пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="34c51-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34c51-104">SYNTAX</span></span>

### <span data-ttu-id="34c51-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34c51-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c51-106">Номер</span><span class="sxs-lookup"><span data-stu-id="34c51-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c51-107">DESCRIPTION</span></span>
<span data-ttu-id="34c51-108">Командлет **Get-AzureBatchPool** возвращает пулы пакетов Azure под учетной записью пакетной службы, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="34c51-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="34c51-109">Вы можете использовать параметр *ID* для получения одного пула или с помощью параметра *Filter* , чтобы получить доступ к пулам, которые соответствуют фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="34c51-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="34c51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34c51-110">EXAMPLES</span></span>

### <span data-ttu-id="34c51-111">Пример 1: получение пула по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="34c51-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="34c51-112">Эта команда получает пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="34c51-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="34c51-113">Пример 2: получение всех пулов с помощью фильтра OData</span><span class="sxs-lookup"><span data-stu-id="34c51-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="34c51-114">Эта команда получает пулы, идентификаторы которых начинаются с "My", с помощью параметра " *Фильтр* ".</span><span class="sxs-lookup"><span data-stu-id="34c51-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="34c51-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34c51-115">PARAMETERS</span></span>

### <span data-ttu-id="34c51-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34c51-116">-BatchContext</span></span>
<span data-ttu-id="34c51-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="34c51-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34c51-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="34c51-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34c51-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="34c51-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34c51-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="34c51-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34c51-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="34c51-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c51-122">-DefaultProfile</span></span>
<span data-ttu-id="34c51-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34c51-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="34c51-124">-Expand</span></span>
<span data-ttu-id="34c51-125">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="34c51-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="34c51-126">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="34c51-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="34c51-127">-Filter</span></span>
<span data-ttu-id="34c51-128">Задает предложение фильтра OData для использования при запросе пулов.</span><span class="sxs-lookup"><span data-stu-id="34c51-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="34c51-129">Если фильтр не указан, возвращаются все пулы под учетной записью пакета, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="34c51-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-130">-ID</span><span class="sxs-lookup"><span data-stu-id="34c51-130">-Id</span></span>
<span data-ttu-id="34c51-131">Указывает идентификатор пула, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="34c51-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="34c51-132">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="34c51-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="34c51-133">-MaxCount</span></span>
<span data-ttu-id="34c51-134">Задает максимальное количество возвращаемых пулов.</span><span class="sxs-lookup"><span data-stu-id="34c51-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="34c51-135">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="34c51-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="34c51-136">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="34c51-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-137">-SELECT</span><span class="sxs-lookup"><span data-stu-id="34c51-137">-Select</span></span>
<span data-ttu-id="34c51-138">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="34c51-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="34c51-139">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="34c51-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c51-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c51-140">CommonParameters</span></span>
<span data-ttu-id="34c51-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34c51-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c51-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c51-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c51-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34c51-143">INPUTS</span></span>

### <span data-ttu-id="34c51-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34c51-144">BatchAccountContext</span></span>
<span data-ttu-id="34c51-145">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34c51-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="34c51-146">Подстрок</span><span class="sxs-lookup"><span data-stu-id="34c51-146">String</span></span>
<span data-ttu-id="34c51-147">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34c51-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="34c51-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c51-148">OUTPUTS</span></span>

### <span data-ttu-id="34c51-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="34c51-149">PSCloudPool</span></span>

## <span data-ttu-id="34c51-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="34c51-150">NOTES</span></span>

## <span data-ttu-id="34c51-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34c51-151">RELATED LINKS</span></span>

[<span data-ttu-id="34c51-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="34c51-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="34c51-153">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="34c51-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="34c51-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="34c51-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="34c51-155">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="34c51-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


