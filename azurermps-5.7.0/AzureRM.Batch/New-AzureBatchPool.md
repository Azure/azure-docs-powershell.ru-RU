---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569992"
---
# <span data-ttu-id="84786-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="84786-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="84786-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84786-102">SYNOPSIS</span></span>
<span data-ttu-id="84786-103">Создание пула в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="84786-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84786-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84786-104">SYNTAX</span></span>

### <span data-ttu-id="84786-105">CloudServiceAndTargetDedicated (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84786-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84786-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="84786-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84786-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="84786-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84786-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="84786-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84786-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84786-109">DESCRIPTION</span></span>
<span data-ttu-id="84786-110">Командлет **New-AzureBatchPool** создает пул в пакетной службе Azure в учетной записи, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="84786-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="84786-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84786-111">EXAMPLES</span></span>

### <span data-ttu-id="84786-112">Пример 1: создание нового пула с помощью набор параметров TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="84786-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="84786-113">Эта команда создает новый пул с ИДЕНТИФИКАТОРом MyPool, используя набор параметров TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="84786-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="84786-114">Цель выделения — это три вычислительных узла.</span><span class="sxs-lookup"><span data-stu-id="84786-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="84786-115">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4.</span><span class="sxs-lookup"><span data-stu-id="84786-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="84786-116">Пример 2: создание нового пула с помощью параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="84786-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="84786-117">Эта команда создает новый пул с ИДЕНТИФИКАТОРом AutoScalePool, используя набор параметров автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="84786-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="84786-118">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4 и конечным количеством вычислительных узлов, которые определяются формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="84786-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="84786-119">Пример 3: создание пула с узлами в подсети</span><span class="sxs-lookup"><span data-stu-id="84786-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="84786-120">Пример 4: создание пула с настраиваемыми учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="84786-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="84786-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84786-121">PARAMETERS</span></span>

### <span data-ttu-id="84786-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="84786-122">-ApplicationLicenses</span></span>
<span data-ttu-id="84786-123">Список лицензий приложения, которые служба пакетной обработки будет доступна на каждом вычислительном узле в пуле.</span><span class="sxs-lookup"><span data-stu-id="84786-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="84786-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="84786-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="84786-126">Определяет интервал времени (в минутах), по истечении которого размер пула автоматически корректируется в соответствии с формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="84786-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="84786-127">По умолчанию используется значение 15 минут, а минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="84786-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="84786-128">-AutoScaleFormula</span></span>
<span data-ttu-id="84786-129">Задает формулу для автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="84786-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84786-130">-BatchContext</span></span>
<span data-ttu-id="84786-131">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="84786-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="84786-132">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="84786-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="84786-133">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="84786-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="84786-134">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="84786-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="84786-135">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="84786-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="84786-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="84786-136">-CertificateReferences</span></span>
<span data-ttu-id="84786-137">Определяет сертификаты, связанные с пулом.</span><span class="sxs-lookup"><span data-stu-id="84786-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="84786-138">Служба Batch устанавливает сертификаты, на которые указывают ссылки, на каждый вычислительный узел пула.</span><span class="sxs-lookup"><span data-stu-id="84786-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="84786-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="84786-140">Задает параметры конфигурации для пула на основе платформы облачных служб Azure.</span><span class="sxs-lookup"><span data-stu-id="84786-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84786-141">-DefaultProfile</span></span>
<span data-ttu-id="84786-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84786-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84786-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="84786-143">-DisplayName</span></span>
<span data-ttu-id="84786-144">Указывает отображаемое имя пула.</span><span class="sxs-lookup"><span data-stu-id="84786-144">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="84786-145">-ID</span><span class="sxs-lookup"><span data-stu-id="84786-145">-Id</span></span>
<span data-ttu-id="84786-146">Указывает идентификатор создаваемого пула.</span><span class="sxs-lookup"><span data-stu-id="84786-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="84786-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="84786-148">Указывает на то, что этот командлет настраивает пул для прямой связи между выделенными вычислительными узлами.</span><span class="sxs-lookup"><span data-stu-id="84786-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="84786-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="84786-150">Указывает максимальное количество задач, которые можно выполнять на одном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="84786-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="84786-151">-Metadata</span></span>
<span data-ttu-id="84786-152">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в новый пул.</span><span class="sxs-lookup"><span data-stu-id="84786-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="84786-153">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="84786-153">The key is the metadata name.</span></span>
<span data-ttu-id="84786-154">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="84786-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="84786-155">-NetworkConfiguration</span></span>
<span data-ttu-id="84786-156">Сетевая конфигурация для пула.</span><span class="sxs-lookup"><span data-stu-id="84786-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="84786-157">-ResizeTimeout</span></span>
<span data-ttu-id="84786-158">Указывает время ожидания для выделения кластерных узлов.</span><span class="sxs-lookup"><span data-stu-id="84786-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="84786-159">-StartTask</span></span>
<span data-ttu-id="84786-160">Указывает спецификацию начальной задачи для пула.</span><span class="sxs-lookup"><span data-stu-id="84786-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="84786-161">Начальная задача выполняется, когда вычислительный узел присоединяется к пулу, или когда выполняется перезагрузка или повторное создание образа.</span><span class="sxs-lookup"><span data-stu-id="84786-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="84786-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="84786-163">Указывает целевое количество выделенных вычислительных узлов, которые нужно выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="84786-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="84786-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="84786-165">Указывает целевое количество вычислительных узлов с низким приоритетом, которые нужно выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="84786-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="84786-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="84786-167">Указывает политику планирования задач, например ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="84786-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-168">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="84786-168">-UserAccount</span></span>
<span data-ttu-id="84786-169">Список учетных записей пользователей, которые нужно создать на каждом узле в пуле.</span><span class="sxs-lookup"><span data-stu-id="84786-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="84786-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="84786-171">Задает параметры конфигурации для пула в инфраструктуре виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="84786-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="84786-172">-VirtualMachineSize</span></span>
<span data-ttu-id="84786-173">Указывает размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="84786-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="84786-174">Дополнительные сведения о размерах виртуальных машин можно найти в разделе размеры виртуальных машин https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) на сайте Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="84786-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84786-175">-Confirm</span></span>
<span data-ttu-id="84786-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84786-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84786-177">-WhatIf</span></span>
<span data-ttu-id="84786-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84786-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84786-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84786-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84786-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84786-180">CommonParameters</span></span>
<span data-ttu-id="84786-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84786-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84786-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84786-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84786-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84786-183">INPUTS</span></span>

### <span data-ttu-id="84786-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84786-184">BatchAccountContext</span></span>
<span data-ttu-id="84786-185">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="84786-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="84786-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84786-186">OUTPUTS</span></span>

## <span data-ttu-id="84786-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="84786-187">NOTES</span></span>

## <span data-ttu-id="84786-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84786-188">RELATED LINKS</span></span>

[<span data-ttu-id="84786-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="84786-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="84786-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="84786-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="84786-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="84786-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="84786-192">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="84786-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


