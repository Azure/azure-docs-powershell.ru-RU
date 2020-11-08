---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: f861397569671d5269e12edee564acdb55519977
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242617"
---
# <span data-ttu-id="e71cc-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e71cc-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="e71cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e71cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e71cc-103">Получение пулов пакетов под указанной пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="e71cc-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="e71cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e71cc-104">SYNTAX</span></span>

### <span data-ttu-id="e71cc-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e71cc-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e71cc-106">Номер</span><span class="sxs-lookup"><span data-stu-id="e71cc-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e71cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71cc-107">DESCRIPTION</span></span>
<span data-ttu-id="e71cc-108">Командлет **Get-AzBatchPool** возвращает пулы пакетов Azure под учетной записью пакетной службы, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="e71cc-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="e71cc-109">Вы можете использовать параметр *ID* для получения одного пула или с помощью параметра *Filter* , чтобы получить доступ к пулам, которые соответствуют фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="e71cc-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e71cc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e71cc-110">EXAMPLES</span></span>

### <span data-ttu-id="e71cc-111">Пример 1: получение пула по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="e71cc-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="e71cc-112">Эта команда получает пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="e71cc-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="e71cc-113">Пример 2: получение всех пулов с помощью фильтра OData</span><span class="sxs-lookup"><span data-stu-id="e71cc-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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
VirtualMachineSize                   : standard_d1_v2
```

<span data-ttu-id="e71cc-114">Эта команда получает пулы, идентификаторы которых начинаются с "My", с помощью параметра " *Фильтр* ".</span><span class="sxs-lookup"><span data-stu-id="e71cc-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="e71cc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e71cc-115">PARAMETERS</span></span>

### <span data-ttu-id="e71cc-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e71cc-116">-BatchContext</span></span>
<span data-ttu-id="e71cc-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e71cc-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e71cc-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="e71cc-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e71cc-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e71cc-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e71cc-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e71cc-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e71cc-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e71cc-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e71cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71cc-122">-DefaultProfile</span></span>
<span data-ttu-id="e71cc-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e71cc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71cc-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="e71cc-124">-Expand</span></span>
<span data-ttu-id="e71cc-125">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="e71cc-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="e71cc-126">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="e71cc-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="e71cc-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="e71cc-127">-Filter</span></span>
<span data-ttu-id="e71cc-128">Задает предложение фильтра OData для использования при запросе пулов.</span><span class="sxs-lookup"><span data-stu-id="e71cc-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="e71cc-129">Если фильтр не указан, возвращаются все пулы под учетной записью пакета, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="e71cc-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="e71cc-130">-ID</span><span class="sxs-lookup"><span data-stu-id="e71cc-130">-Id</span></span>
<span data-ttu-id="e71cc-131">Указывает идентификатор пула, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="e71cc-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="e71cc-132">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="e71cc-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e71cc-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e71cc-133">-MaxCount</span></span>
<span data-ttu-id="e71cc-134">Задает максимальное количество возвращаемых пулов.</span><span class="sxs-lookup"><span data-stu-id="e71cc-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="e71cc-135">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="e71cc-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e71cc-136">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="e71cc-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="e71cc-137">-SELECT</span><span class="sxs-lookup"><span data-stu-id="e71cc-137">-Select</span></span>
<span data-ttu-id="e71cc-138">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="e71cc-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="e71cc-139">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="e71cc-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="e71cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71cc-140">CommonParameters</span></span>
<span data-ttu-id="e71cc-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e71cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71cc-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71cc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71cc-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e71cc-143">INPUTS</span></span>

### <span data-ttu-id="e71cc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e71cc-144">System.String</span></span>

### <span data-ttu-id="e71cc-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e71cc-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e71cc-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71cc-146">OUTPUTS</span></span>

### <span data-ttu-id="e71cc-147">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="e71cc-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="e71cc-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="e71cc-148">NOTES</span></span>

## <span data-ttu-id="e71cc-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e71cc-149">RELATED LINKS</span></span>

[<span data-ttu-id="e71cc-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e71cc-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e71cc-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e71cc-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="e71cc-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e71cc-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="e71cc-153">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="e71cc-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
