---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: f861397569671d5269e12edee564acdb55519977
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509710"
---
# <span data-ttu-id="8ea6e-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8ea6e-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="8ea6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea6e-103">Получает пакетные пулы в указанной учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="8ea6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ea6e-104">SYNTAX</span></span>

### <span data-ttu-id="8ea6e-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ea6e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea6e-106">ИД</span><span class="sxs-lookup"><span data-stu-id="8ea6e-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea6e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ea6e-107">DESCRIPTION</span></span>
<span data-ttu-id="8ea6e-108">С **помощью cmdlet Get-AzBatchPool** можно получить пулы Azure Batch в учетной записи Batch, заданной с *параметром BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="8ea6e-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="8ea6e-109">С помощью параметра *Id* можно получить один пул или с помощью параметра *Filter* получить пулы, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8ea6e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ea6e-110">EXAMPLES</span></span>

### <span data-ttu-id="8ea6e-111">Пример 1. Получить пул по ИД</span><span class="sxs-lookup"><span data-stu-id="8ea6e-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="8ea6e-112">Эта команда получает пул с ID MyPool.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="8ea6e-113">Пример 2. Получить все пулы с помощью фильтра OData</span><span class="sxs-lookup"><span data-stu-id="8ea6e-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="8ea6e-114">Эта команда возвращает пулы, ИД которых начинаются с моего, с помощью *параметра Filter.*</span><span class="sxs-lookup"><span data-stu-id="8ea6e-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="8ea6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ea6e-115">PARAMETERS</span></span>

### <span data-ttu-id="8ea6e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8ea6e-116">-BatchContext</span></span>
<span data-ttu-id="8ea6e-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ea6e-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8ea6e-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8ea6e-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8ea6e-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8ea6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea6e-122">-DefaultProfile</span></span>
<span data-ttu-id="8ea6e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea6e-124">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="8ea6e-124">-Expand</span></span>
<span data-ttu-id="8ea6e-125">Указывает предложение развернуть протокол Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="8ea6e-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8ea6e-126">Укажите значение этого параметра, чтобы получить связанные объекты основной сущности, которую вы получаете.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8ea6e-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="8ea6e-127">-Filter</span></span>
<span data-ttu-id="8ea6e-128">Указывает предложение фильтра OData, используемую при запросе пулов.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="8ea6e-129">Если не указать фильтр, возвращаются все пулы в учетной записи Batch, заданной с параметром *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="8ea6e-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="8ea6e-130">-Id</span><span class="sxs-lookup"><span data-stu-id="8ea6e-130">-Id</span></span>
<span data-ttu-id="8ea6e-131">Определяет ИД пула, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="8ea6e-132">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="8ea6e-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8ea6e-133">-MaxCount</span></span>
<span data-ttu-id="8ea6e-134">Указывает максимальное количество пулов, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="8ea6e-135">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8ea6e-136">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="8ea6e-137">-Select</span><span class="sxs-lookup"><span data-stu-id="8ea6e-137">-Select</span></span>
<span data-ttu-id="8ea6e-138">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="8ea6e-139">Укажите значение этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8ea6e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea6e-140">CommonParameters</span></span>
<span data-ttu-id="8ea6e-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea6e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea6e-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ea6e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea6e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ea6e-143">INPUTS</span></span>

### <span data-ttu-id="8ea6e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8ea6e-144">System.String</span></span>

### <span data-ttu-id="8ea6e-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ea6e-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8ea6e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ea6e-146">OUTPUTS</span></span>

### <span data-ttu-id="8ea6e-147">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="8ea6e-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="8ea6e-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ea6e-148">NOTES</span></span>

## <span data-ttu-id="8ea6e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ea6e-149">RELATED LINKS</span></span>

[<span data-ttu-id="8ea6e-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ea6e-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8ea6e-151">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8ea6e-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="8ea6e-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8ea6e-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="8ea6e-153">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="8ea6e-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
