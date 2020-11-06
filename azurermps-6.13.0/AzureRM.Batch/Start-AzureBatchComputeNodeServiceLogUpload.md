---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/Start-AzureBatchComputeNodeServiceLogUpload
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchComputeNodeServiceLogUpload.md
ms.openlocfilehash: 8f171b42e3f1e1f087890ec451d5a3ff13cb8c57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565906"
---
# <span data-ttu-id="418e0-101">Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="418e0-101">Start-AzureBatchComputeNodeServiceLogUpload</span></span>

## <span data-ttu-id="418e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="418e0-102">SYNOPSIS</span></span>
<span data-ttu-id="418e0-103">Добавьте файлы журнала службы узлов вычислительной среды в контейнер хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="418e0-103">Upload compute node service log files to an Azure Storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="418e0-104">SYNTAX</span></span>

### <span data-ttu-id="418e0-105">AzureBatchComputeNodeServiceLogUpload (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="418e0-105">AzureBatchComputeNodeServiceLogUpload (Default)</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ContainerUrl] <String> [-StartTime] <DateTime>
 [-EndTime <DateTime>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418e0-106">Номер</span><span class="sxs-lookup"><span data-stu-id="418e0-106">Id</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-PoolId] <String> [-ComputeNodeId] <String>
 [-ContainerUrl] <String> [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418e0-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="418e0-107">ParentObject</span></span>
```
Start-AzureBatchComputeNodeServiceLogUpload [-ComputeNode] <PSComputeNode> [-ContainerUrl] <String>
 [-StartTime] <DateTime> [-EndTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="418e0-108">DESCRIPTION</span></span>
<span data-ttu-id="418e0-109">Этот командлет собирает файлы журнала пакетной службы Azure из вычислительных узлов, если возникла ошибка и вы хотите эскалировать службу поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="418e0-109">This cmdlet gathers Azure Batch service log files from compute nodes if you are experiencing an error and wish to escalate to Azure support.</span></span> <span data-ttu-id="418e0-110">Файлы журнала пакетной службы Azure должны быть предоставлены службе поддержки Azure для облегчения отладки с помощью пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="418e0-110">The Azure Batch service log files should be shared with Azure support to aid in debugging issues with the Batch service.</span></span> 

## <span data-ttu-id="418e0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="418e0-111">EXAMPLES</span></span>

### <span data-ttu-id="418e0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="418e0-112">Example 1</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    4 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="418e0-113">Загружаются журналы служб узла вычислений, написанные на или после 1 января 2018 (полночь), которые были получены из вычислительного узла, заданным идентификатором пула, в котором находится вычислительный узел, и вычисляемым идентификатором узла.</span><span class="sxs-lookup"><span data-stu-id="418e0-113">Upload compute node service logs written on or after January 1, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="418e0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="418e0-114">Example 2</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -PoolId "contosopool" -ComputeNodeId "tvm-1612030122_1-20180405t234700z" -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="418e0-115">Файлы журнала служб COMPUTE Node, созданные на основе 1 января, 2018 и выше 10 января 2018 (полночь), которые были получены из вычислительного узла, задают идентификатор пула, в котором находится вычислительный узел, и COMPUTE ID узла.</span><span class="sxs-lookup"><span data-stu-id="418e0-115">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node, given pool id of the pool in which the compute node resides, and compute node id.</span></span>

### <span data-ttu-id="418e0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="418e0-116">Example 3</span></span>

```powershell
PS C:\> $storageContext = New-AzureStorageContext -StorageAccountName "contosogeneral" -StorageAccountKey "<Storage Key for ContosoGeneral ends with ==>"
PS C:\> $sasToken = New-AzureStorageContainerSASToken -Name "contosocontainer" -Context $storageContext
PS C:\> $containerUrl = "https://contosogeneral.blob.core.windows.net/contosocontainer" + $sasToken
PS C:\> $batchContext = Get-AzureRmBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzureBatchComputeNode -BatchContext $batchContext -Id "tvm-1612030122_1-20180405t234700z" -PoolId "contosopool" | Start-AzureBatchComputeNodeServiceLogUpload -BatchContext $batchContext -ContainerUrl $containerUrl -StartTime "2018-01-01 00:00:00Z" -EndTime "2018-01-10 00:00:00Z"

NumberOfFilesUploaded VirtualDirectoryName
--------------------- --------------------
                    2 contosobatch-22F48D278AD60CC2/contosopool/tvm-1612030122_1-20180405t234700z/bc3dd583-19a5-4665-aa83-87e4e1237d35
```

<span data-ttu-id="418e0-117">Файлы журнала служб COMPUTE node записываются на год или после 1 января 2018 г. и до 10 января 2018 (полночь), которые были получены из объекта COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="418e0-117">Upload compute node service logs written on or after January 1, 2018 midnight and before January 10, 2018 midnight, which were obtained from the compute node object.</span></span>

## <span data-ttu-id="418e0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="418e0-118">PARAMETERS</span></span>

### <span data-ttu-id="418e0-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="418e0-119">-BatchContext</span></span>
<span data-ttu-id="418e0-120">Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="418e0-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="418e0-121">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="418e0-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="418e0-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="418e0-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="418e0-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="418e0-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="418e0-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="418e0-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="418e0-125">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="418e0-125">-ComputeNode</span></span>
<span data-ttu-id="418e0-126">Указывает объект **PSComputeNode** , из которого извлекаются журналы служб.</span><span class="sxs-lookup"><span data-stu-id="418e0-126">Specifies the **PSComputeNode** object from which service logs are retrieved.</span></span>

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

### <span data-ttu-id="418e0-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="418e0-127">-ComputeNodeId</span></span>
<span data-ttu-id="418e0-128">Идентификатор вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="418e0-128">The id of the compute node.</span></span>

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

### <span data-ttu-id="418e0-129">-ContainerUrl</span><span class="sxs-lookup"><span data-stu-id="418e0-129">-ContainerUrl</span></span>
<span data-ttu-id="418e0-130">URL-адрес контейнера для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="418e0-130">The container url to Azure Storage.</span></span>

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

### <span data-ttu-id="418e0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418e0-131">-DefaultProfile</span></span>
<span data-ttu-id="418e0-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="418e0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="418e0-133">-EndTime</span><span class="sxs-lookup"><span data-stu-id="418e0-133">-EndTime</span></span>
<span data-ttu-id="418e0-134">Время завершения журнала службы, которое нужно отправить (необязательно).</span><span class="sxs-lookup"><span data-stu-id="418e0-134">The end time of service log to be uploaded (optional).</span></span>

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

### <span data-ttu-id="418e0-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="418e0-135">-PoolId</span></span>
<span data-ttu-id="418e0-136">Идентификатор пула, содержащего вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="418e0-136">The id of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="418e0-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="418e0-137">-StartTime</span></span>
<span data-ttu-id="418e0-138">Время запуска журнала служб для отправки.</span><span class="sxs-lookup"><span data-stu-id="418e0-138">The start time of service log to be uploaded.</span></span>

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

### <span data-ttu-id="418e0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="418e0-139">-Confirm</span></span>
<span data-ttu-id="418e0-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="418e0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418e0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418e0-141">-WhatIf</span></span>
<span data-ttu-id="418e0-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="418e0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="418e0-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="418e0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418e0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418e0-144">CommonParameters</span></span>
<span data-ttu-id="418e0-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="418e0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418e0-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418e0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418e0-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="418e0-147">INPUTS</span></span>

### <span data-ttu-id="418e0-148">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="418e0-148">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="418e0-149">Параметры: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="418e0-149">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="418e0-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="418e0-150">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="418e0-151">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="418e0-151">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="418e0-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="418e0-152">OUTPUTS</span></span>

### <span data-ttu-id="418e0-153">Microsoft.Azure.Commands.BatCH. Models. PSStartComputeNodeServiceLogUploadResult</span><span class="sxs-lookup"><span data-stu-id="418e0-153">Microsoft.Azure.Commands.Batch.Models.PSStartComputeNodeServiceLogUploadResult</span></span>

## <span data-ttu-id="418e0-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="418e0-154">NOTES</span></span>

## <span data-ttu-id="418e0-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="418e0-155">RELATED LINKS</span></span>
