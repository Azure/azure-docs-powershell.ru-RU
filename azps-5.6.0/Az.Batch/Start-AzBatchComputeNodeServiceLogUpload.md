---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/Start-AzBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 84d0d1711c9ed29aa48c4845787529a46686da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975955"
---
# <span data-ttu-id="1f203-101">Start-AzBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="1f203-101">Start-AzBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="1f203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f203-102">SYNOPSIS</span></span>
<span data-ttu-id="1f203-103">Отправка файлов журнала журнала службы вычислений в контейнер хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-103">Upload compute node service log files to an Azure Storage container.</span></span>

## <span data-ttu-id="1f203-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f203-104">SYNTAX</span></span>

### <span data-ttu-id="1f203-105">AzureBatchComputeNodeServiceLogUpload (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f203-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f203-106">ИД</span><span class="sxs-lookup"><span data-stu-id="1f203-106">Id</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f203-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="1f203-107">ParentObject</span></span>
```
Start-AzBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f203-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f203-108">DESCRIPTION</span></span>
<span data-ttu-id="1f203-109">Этот cmdlet собирает файлы журнала пакетной службы Azure с узлов компьютеров, если вы столкнулись с ошибкой и хотите зайти в службу поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="1f203-110">Чтобы решить проблемы с обработкой пакетной службы, необходимо делиться файлами журнала пакетных служб Azure с помощью службы Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="1f203-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f203-111">EXAMPLES</span></span>

### <span data-ttu-id="1f203-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f203-112">Example 1</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="1f203-113">Журналы службы отправки вычислительных узлов, написанные 1 января 2018 г. в полночь или после 1 января 2018 г., которые были получены из узла вычислений, с учетом того, какой id пула находится в этом пуле, и его ид.</span><span class="sxs-lookup"><span data-stu-id="1f203-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="1f203-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1f203-114">Example 2</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="1f203-115">Журналы службы отправки вычислительных узлов, написанные 1 января 2018 г. в полночь и до полуночи 10 января 2018 г., которые были получены из узла вычислений, заданный пул пула, в котором находится узел вычислений, и его ид.</span><span class="sxs-lookup"><span data-stu-id="1f203-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="1f203-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1f203-116">Example 3</span></span>
```
PS C:\> $storageContext = New-AzStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="1f203-117">Журналы службы вычислительных узлов, написанные 1 января 2018 г. в полночь и до полуночи 10 января 2018 г., были получены из объекта вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="1f203-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="1f203-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f203-118">PARAMETERS</span></span>

### <span data-ttu-id="1f203-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1f203-119">-BatchContext</span></span>
<span data-ttu-id="1f203-120">Экземпляр BatchAccountContext, который используется при взаимодействии со службой batch.</span><span class="sxs-lookup"><span data-stu-id="1f203-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="1f203-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f203-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="1f203-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="1f203-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="1f203-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f203-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="1f203-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1f203-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1f203-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1f203-125">-ComputeNode</span></span>
<span data-ttu-id="1f203-126">Определяет объект **PSComputeNode,** из которого извлекаются журналы служб.</span><span class="sxs-lookup"><span data-stu-id="1f203-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="1f203-127">-ComputeNodeId</span></span>
<span data-ttu-id="1f203-128">ID узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="1f203-128">The id of the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="1f203-129">-ContainerUrl</span></span>
<span data-ttu-id="1f203-130">URL-адрес контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-130">The container url to Azure Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f203-131">-DefaultProfile</span></span>
<span data-ttu-id="1f203-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f203-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1f203-133">-EndTime</span></span>
<span data-ttu-id="1f203-134">Время окончания отправки журнала службы (необязательно).</span><span class="sxs-lookup"><span data-stu-id="1f203-134">The end time of service log to be uploaded (optional).</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1f203-135">-PoolId</span></span>
<span data-ttu-id="1f203-136">Id пула, который содержит узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="1f203-136">The id of the pool that contains the compute node.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1f203-137">-StartTime</span></span>
<span data-ttu-id="1f203-138">Время начала отправки журнала службы.</span><span class="sxs-lookup"><span data-stu-id="1f203-138">The start time of service log to be uploaded.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f203-139">-Confirm</span></span>
<span data-ttu-id="1f203-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1f203-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f203-141">-WhatIf</span></span>
<span data-ttu-id="1f203-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f203-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f203-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f203-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f203-144">CommonParameters</span></span>
<span data-ttu-id="1f203-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f203-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f203-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f203-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f203-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f203-147">INPUTS</span></span>

### <span data-ttu-id="1f203-148">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1f203-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="1f203-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1f203-149">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1f203-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f203-150">OUTPUTS</span></span>

### <span data-ttu-id="1f203-151">Microsoft.Azure.Commands.Batch. Models.PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="1f203-151">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="1f203-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f203-152">NOTES</span></span>

## <span data-ttu-id="1f203-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f203-153">RELATED LINKS</span></span>
