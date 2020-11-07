---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 255db3680707af4e3658ce8a526cfa7b4a4d6f1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731852"
---
# <span data-ttu-id="15dfa-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="15dfa-101">New-AzBatchPool</span></span>

## <span data-ttu-id="15dfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="15dfa-103">Создание пула в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="15dfa-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="15dfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15dfa-104">SYNTAX</span></span>

### <span data-ttu-id="15dfa-105">CloudServiceAndTargetDedicated (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15dfa-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15dfa-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="15dfa-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
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

### <span data-ttu-id="15dfa-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="15dfa-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

### <span data-ttu-id="15dfa-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="15dfa-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

## <span data-ttu-id="15dfa-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15dfa-109">DESCRIPTION</span></span>
<span data-ttu-id="15dfa-110">Командлет **New-AzBatchPool** создает пул в пакетной службе Azure в учетной записи, указанной в параметре *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="15dfa-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="15dfa-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15dfa-111">EXAMPLES</span></span>

### <span data-ttu-id="15dfa-112">Пример 1: создание нового пула с помощью параметра TargetDedicated, установленного с помощью CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="15dfa-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="15dfa-113">Пример 2: создание нового пула с помощью параметра TargetDedicated, установленного с помощью VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="15dfa-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="15dfa-114">Эта команда создает новый пул с ИДЕНТИФИКАТОРом MyPool, используя набор параметров TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="15dfa-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="15dfa-115">Цель выделения — это три вычислительных узла.</span><span class="sxs-lookup"><span data-stu-id="15dfa-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="15dfa-116">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4.</span><span class="sxs-lookup"><span data-stu-id="15dfa-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="15dfa-117">Пример 3: создание нового пула с помощью параметра автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="15dfa-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="15dfa-118">Эта команда создает новый пул с ИДЕНТИФИКАТОРом AutoScalePool, используя набор параметров автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="15dfa-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="15dfa-119">Пул настроен на использование небольших виртуальных компьютеров с последней версией операционной системы семейства 4 и конечным количеством вычислительных узлов, которые определяются формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="15dfa-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="15dfa-120">Пример 4: создание пула с узлами в подсети</span><span class="sxs-lookup"><span data-stu-id="15dfa-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="15dfa-121">Пример 5: создание пула с настраиваемыми учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="15dfa-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="15dfa-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15dfa-122">PARAMETERS</span></span>

### <span data-ttu-id="15dfa-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="15dfa-123">-ApplicationLicenses</span></span>
<span data-ttu-id="15dfa-124">Список лицензий приложения, которые служба пакетной обработки будет доступна на каждом вычислительном узле в пуле.</span><span class="sxs-lookup"><span data-stu-id="15dfa-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="15dfa-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="15dfa-125">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dfa-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="15dfa-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="15dfa-127">Определяет интервал времени (в минутах), по истечении которого размер пула автоматически корректируется в соответствии с формулой автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="15dfa-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="15dfa-128">По умолчанию используется значение 15 минут, а минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="15dfa-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="15dfa-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="15dfa-129">-AutoScaleFormula</span></span>
<span data-ttu-id="15dfa-130">Задает формулу для автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-130">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="15dfa-131">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="15dfa-131">-BatchContext</span></span>
<span data-ttu-id="15dfa-132">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="15dfa-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="15dfa-133">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="15dfa-133">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="15dfa-134">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="15dfa-134">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="15dfa-135">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="15dfa-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="15dfa-136">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="15dfa-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="15dfa-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="15dfa-137">-CertificateReferences</span></span>
<span data-ttu-id="15dfa-138">Определяет сертификаты, связанные с пулом.</span><span class="sxs-lookup"><span data-stu-id="15dfa-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="15dfa-139">Служба Batch устанавливает сертификаты, на которые указывают ссылки, на каждый вычислительный узел пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dfa-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="15dfa-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="15dfa-141">Задает параметры конфигурации для пула на основе платформы облачных служб Azure.</span><span class="sxs-lookup"><span data-stu-id="15dfa-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="15dfa-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15dfa-142">-DefaultProfile</span></span>
<span data-ttu-id="15dfa-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15dfa-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15dfa-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15dfa-144">-DisplayName</span></span>
<span data-ttu-id="15dfa-145">Указывает отображаемое имя пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="15dfa-146">-ID</span><span class="sxs-lookup"><span data-stu-id="15dfa-146">-Id</span></span>
<span data-ttu-id="15dfa-147">Указывает идентификатор создаваемого пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="15dfa-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="15dfa-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="15dfa-149">Указывает на то, что этот командлет настраивает пул для прямой связи между выделенными вычислительными узлами.</span><span class="sxs-lookup"><span data-stu-id="15dfa-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="15dfa-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="15dfa-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="15dfa-151">Указывает максимальное количество задач, которые можно выполнять на одном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="15dfa-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="15dfa-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="15dfa-152">-Metadata</span></span>
<span data-ttu-id="15dfa-153">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в новый пул.</span><span class="sxs-lookup"><span data-stu-id="15dfa-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="15dfa-154">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="15dfa-154">The key is the metadata name.</span></span>
<span data-ttu-id="15dfa-155">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="15dfa-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="15dfa-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="15dfa-156">-NetworkConfiguration</span></span>
<span data-ttu-id="15dfa-157">Сетевая конфигурация для пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-157">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="15dfa-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="15dfa-158">-ResizeTimeout</span></span>
<span data-ttu-id="15dfa-159">Указывает время ожидания для выделения кластерных узлов.</span><span class="sxs-lookup"><span data-stu-id="15dfa-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="15dfa-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="15dfa-160">-StartTask</span></span>
<span data-ttu-id="15dfa-161">Указывает спецификацию начальной задачи для пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="15dfa-162">Начальная задача выполняется, когда вычислительный узел присоединяется к пулу, или когда выполняется перезагрузка или повторное создание образа.</span><span class="sxs-lookup"><span data-stu-id="15dfa-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="15dfa-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="15dfa-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="15dfa-164">Указывает целевое количество выделенных вычислительных узлов, которые нужно выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dfa-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="15dfa-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="15dfa-166">Указывает целевое количество вычислительных узлов с низким приоритетом, которые нужно выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="15dfa-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="15dfa-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="15dfa-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="15dfa-168">Указывает политику планирования задач, например ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="15dfa-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="15dfa-169">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="15dfa-169">-UserAccount</span></span>
<span data-ttu-id="15dfa-170">Список учетных записей пользователей, которые нужно создать на каждом узле в пуле.</span><span class="sxs-lookup"><span data-stu-id="15dfa-170">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15dfa-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="15dfa-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="15dfa-172">Задает параметры конфигурации для пула в инфраструктуре виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="15dfa-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="15dfa-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="15dfa-173">-VirtualMachineSize</span></span>
<span data-ttu-id="15dfa-174">Указывает размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="15dfa-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="15dfa-175">Дополнительные сведения о размерах виртуальных машин можно найти в разделе размеры виртуальных машин https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) на сайте Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="15dfa-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="15dfa-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15dfa-176">-Confirm</span></span>
<span data-ttu-id="15dfa-177">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15dfa-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15dfa-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15dfa-178">-WhatIf</span></span>
<span data-ttu-id="15dfa-179">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15dfa-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15dfa-180">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15dfa-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15dfa-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15dfa-181">CommonParameters</span></span>
<span data-ttu-id="15dfa-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15dfa-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15dfa-183">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15dfa-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15dfa-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15dfa-184">INPUTS</span></span>

### <span data-ttu-id="15dfa-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="15dfa-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="15dfa-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15dfa-186">OUTPUTS</span></span>

### <span data-ttu-id="15dfa-187">System. void</span><span class="sxs-lookup"><span data-stu-id="15dfa-187">System.Void</span></span>

## <span data-ttu-id="15dfa-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="15dfa-188">NOTES</span></span>

## <span data-ttu-id="15dfa-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15dfa-189">RELATED LINKS</span></span>

[<span data-ttu-id="15dfa-190">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="15dfa-190">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="15dfa-191">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="15dfa-191">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="15dfa-192">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="15dfa-192">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="15dfa-193">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="15dfa-193">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


