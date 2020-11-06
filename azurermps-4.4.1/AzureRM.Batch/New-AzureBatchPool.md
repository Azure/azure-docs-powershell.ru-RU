---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565652"
---
# <span data-ttu-id="19c29-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="19c29-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="19c29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19c29-102">SYNOPSIS</span></span>
<span data-ttu-id="19c29-103">Создание пула в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="19c29-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19c29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19c29-104">SYNTAX</span></span>

### <span data-ttu-id="19c29-105">CloudServiceAndTargetDedicated (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19c29-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19c29-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="19c29-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c29-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="19c29-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19c29-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="19c29-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c29-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c29-109">DESCRIPTION</span></span>
<span data-ttu-id="19c29-110">Командлет **New-AzureBatchPool** создает пул в пакетной службе Azure в учетной записи, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="19c29-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="19c29-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19c29-111">EXAMPLES</span></span>

### <span data-ttu-id="19c29-112">Пример 1: создание нового пула с помощью набор параметров TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="19c29-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="19c29-113">Эта команда создает новый пул с ИДЕНТИФИКАТОРом MyPool, используя набор параметров TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="19c29-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="19c29-114">Цель выделения — это три вычислительных узла.</span><span class="sxs-lookup"><span data-stu-id="19c29-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="19c29-115">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4.</span><span class="sxs-lookup"><span data-stu-id="19c29-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="19c29-116">Пример 2: создание нового пула с помощью параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="19c29-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="19c29-117">Эта команда создает новый пул с ИДЕНТИФИКАТОРом AutoScalePool, используя набор параметров автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="19c29-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="19c29-118">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4 и конечным количеством вычислительных узлов, которые определяются формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="19c29-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="19c29-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19c29-119">PARAMETERS</span></span>

### <span data-ttu-id="19c29-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="19c29-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="19c29-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="19c29-122">Определяет интервал времени (в минутах), по истечении которого размер пула автоматически корректируется в соответствии с формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="19c29-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="19c29-123">По умолчанию используется значение 15 минут, а минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="19c29-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="19c29-124">-AutoScaleFormula</span></span>
<span data-ttu-id="19c29-125">Задает формулу для автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="19c29-126">-BatchContext</span></span>
<span data-ttu-id="19c29-127">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="19c29-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19c29-128">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="19c29-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="19c29-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="19c29-129">-CertificateReferences</span></span>
<span data-ttu-id="19c29-130">Определяет сертификаты, связанные с пулом.</span><span class="sxs-lookup"><span data-stu-id="19c29-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="19c29-131">Служба Batch устанавливает сертификаты, на которые указывают ссылки, на каждый вычислительный узел пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="19c29-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="19c29-133">Задает параметры конфигурации для пула на основе платформы облачных служб Azure.</span><span class="sxs-lookup"><span data-stu-id="19c29-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19c29-134">-DisplayName</span></span>
<span data-ttu-id="19c29-135">Указывает отображаемое имя пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="19c29-136">-ID</span><span class="sxs-lookup"><span data-stu-id="19c29-136">-Id</span></span>
<span data-ttu-id="19c29-137">Указывает идентификатор создаваемого пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="19c29-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="19c29-139">Указывает на то, что этот командлет настраивает пул для прямой связи между выделенными вычислительными узлами.</span><span class="sxs-lookup"><span data-stu-id="19c29-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="19c29-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="19c29-141">Указывает максимальное количество задач, которые можно выполнять на одном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="19c29-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="19c29-142">-Metadata</span></span>
<span data-ttu-id="19c29-143">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в новый пул.</span><span class="sxs-lookup"><span data-stu-id="19c29-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="19c29-144">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="19c29-144">The key is the metadata name.</span></span>
<span data-ttu-id="19c29-145">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="19c29-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="19c29-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="19c29-147">-ResizeTimeout</span></span>
<span data-ttu-id="19c29-148">Указывает время ожидания для выделения кластерных узлов.</span><span class="sxs-lookup"><span data-stu-id="19c29-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="19c29-149">-StartTask</span></span>
<span data-ttu-id="19c29-150">Указывает спецификацию начальной задачи для пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="19c29-151">Начальная задача выполняется, когда вычислительный узел присоединяется к пулу, или когда выполняется перезагрузка или повторное создание образа.</span><span class="sxs-lookup"><span data-stu-id="19c29-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="19c29-152">-TargetDedicated</span></span>
<span data-ttu-id="19c29-153">Указывает целевое количество целевых кластерных узлов, которые нужно выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="19c29-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="19c29-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="19c29-155">Указывает политику планирования задач, например ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="19c29-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="19c29-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="19c29-157">Задает параметры конфигурации для пула в инфраструктуре виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="19c29-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="19c29-158">-VirtualMachineSize</span></span>
<span data-ttu-id="19c29-159">Указывает размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="19c29-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="19c29-160">Дополнительные сведения о размерах виртуальных машин можно найти в разделе размеры виртуальных машин https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) на сайте Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="19c29-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c29-161">-Confirm</span></span>
<span data-ttu-id="19c29-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19c29-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c29-163">-WhatIf</span></span>
<span data-ttu-id="19c29-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19c29-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c29-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19c29-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c29-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c29-166">-DefaultProfile</span></span>
<span data-ttu-id="19c29-167">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19c29-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c29-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c29-168">CommonParameters</span></span>
<span data-ttu-id="19c29-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19c29-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c29-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c29-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c29-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19c29-171">INPUTS</span></span>

### <span data-ttu-id="19c29-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19c29-172">BatchAccountContext</span></span>
<span data-ttu-id="19c29-173">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="19c29-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="19c29-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c29-174">OUTPUTS</span></span>

## <span data-ttu-id="19c29-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="19c29-175">NOTES</span></span>

## <span data-ttu-id="19c29-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19c29-176">RELATED LINKS</span></span>

[<span data-ttu-id="19c29-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="19c29-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="19c29-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="19c29-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="19c29-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="19c29-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="19c29-180">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="19c29-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


