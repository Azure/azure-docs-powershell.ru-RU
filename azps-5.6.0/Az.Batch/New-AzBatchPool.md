---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992967"
---
# <span data-ttu-id="723e1-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="723e1-101">New-AzBatchPool</span></span>

## <span data-ttu-id="723e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="723e1-102">SYNOPSIS</span></span>
<span data-ttu-id="723e1-103">Создает пул в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="723e1-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="723e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="723e1-104">SYNTAX</span></span>

### <span data-ttu-id="723e1-105">CloudServiceAndTargetDedicated (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="723e1-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="723e1-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="723e1-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="723e1-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="723e1-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="723e1-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="723e1-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723e1-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="723e1-109">DESCRIPTION</span></span>
<span data-ttu-id="723e1-110">С **помощью cmdlet New-AzBatchPool** создается пул в службе Azure Batch с учетной записью, заданной параметром *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="723e1-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="723e1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="723e1-111">EXAMPLES</span></span>

### <span data-ttu-id="723e1-112">Пример 1. Создание пула с использованием набора параметров TargetDedicated с помощью CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="723e1-113">Пул настроен для использования STANDARD_D1_V2 машин с версией операционной системы для семьи 4.</span><span class="sxs-lookup"><span data-stu-id="723e1-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="723e1-114">Пример 2. Создание пула с использованием набора параметров TargetDedicated с помощью VirtualMa ветвьConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="723e1-115">Эта команда создает новый пул с ID MyPool с использованием набора параметров TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="723e1-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="723e1-116">Целевой объем выделения составляет три вычислительных узла.</span><span class="sxs-lookup"><span data-stu-id="723e1-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="723e1-117">Пул настроен для использования на STANDARD_D1_V2 компьютерах с изображением операционной системы Центра обработки данных Windows-2016.</span><span class="sxs-lookup"><span data-stu-id="723e1-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="723e1-118">Пример 3. Создание пула с использованием набора параметров "Автомасштаб"</span><span class="sxs-lookup"><span data-stu-id="723e1-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="723e1-119">Эта команда создает новый пул с автомасштабом для ID AutoScalePool с использованием набора параметров autoScale.</span><span class="sxs-lookup"><span data-stu-id="723e1-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="723e1-120">Пул настроен для использования виртуальных машин STANDARD_D1_V2 с изображением операционной системы Центра обработки данных Windows 2016, а конечное количество узлов определяется формулой автомасштаби.</span><span class="sxs-lookup"><span data-stu-id="723e1-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="723e1-121">Пример 4. Создание пула с узлами в подсети</span><span class="sxs-lookup"><span data-stu-id="723e1-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="723e1-122">Пример 5. Создание пула с настраиваемой учетной записью пользователя</span><span class="sxs-lookup"><span data-stu-id="723e1-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="723e1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="723e1-123">PARAMETERS</span></span>

### <span data-ttu-id="723e1-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="723e1-124">-ApplicationLicenses</span></span>
<span data-ttu-id="723e1-125">Список лицензий на приложения, которые пакетная служба сделает доступными на каждом узле компьютеров в пуле.</span><span class="sxs-lookup"><span data-stu-id="723e1-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="723e1-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="723e1-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="723e1-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="723e1-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="723e1-128">Определяет время (в минутах), которое будет задано до того, как размер пула будет автоматически скорректирован в соответствии с формулой автомасштаби.</span><span class="sxs-lookup"><span data-stu-id="723e1-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="723e1-129">Значение по умолчанию — 15 минут, минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="723e1-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="723e1-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="723e1-130">-AutoScaleFormula</span></span>
<span data-ttu-id="723e1-131">Формула для автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="723e1-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="723e1-132">-BatchContext</span></span>
<span data-ttu-id="723e1-133">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="723e1-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="723e1-134">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="723e1-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="723e1-135">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="723e1-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="723e1-136">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="723e1-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="723e1-137">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="723e1-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="723e1-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="723e1-138">-CertificateReferences</span></span>
<span data-ttu-id="723e1-139">Сертификаты, связанные с пулом.</span><span class="sxs-lookup"><span data-stu-id="723e1-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="723e1-140">Пакетная служба устанавливает сертификаты, на которые ссылается эта служба, на каждый вычислительный узел пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="723e1-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="723e1-142">Определяет параметры конфигурации для пула, основанного на платформе облачных служб Azure.</span><span class="sxs-lookup"><span data-stu-id="723e1-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="723e1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723e1-143">-DefaultProfile</span></span>
<span data-ttu-id="723e1-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="723e1-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="723e1-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="723e1-145">-DisplayName</span></span>
<span data-ttu-id="723e1-146">Отображает имя пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="723e1-147">-Id</span><span class="sxs-lookup"><span data-stu-id="723e1-147">-Id</span></span>
<span data-ttu-id="723e1-148">Определяет ИД создаемого пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="723e1-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="723e1-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="723e1-150">Указывает на то, что этот cmdlet создает пул для прямой связи между выделенными узлами компьютеров.</span><span class="sxs-lookup"><span data-stu-id="723e1-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="723e1-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="723e1-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="723e1-152">Указывает максимальное количество задач, которые могут выполняться на одном узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="723e1-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="723e1-153">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="723e1-153">-Metadata</span></span>
<span data-ttu-id="723e1-154">Метаданные (ключевые и важные), которые нужно добавить в новый пул.</span><span class="sxs-lookup"><span data-stu-id="723e1-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="723e1-155">Ключ — это имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="723e1-155">The key is the metadata name.</span></span>
<span data-ttu-id="723e1-156">Значение — это значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="723e1-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="723e1-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-157">-MountConfiguration</span></span>
<span data-ttu-id="723e1-158">Список файловых систем для установки на каждом узле пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="723e1-159">Это поддерживает файлы Azure, NFS, CIFS/SMB и BLOB-файлы.</span><span class="sxs-lookup"><span data-stu-id="723e1-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723e1-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-160">-NetworkConfiguration</span></span>
<span data-ttu-id="723e1-161">Конфигурация сети для пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="723e1-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="723e1-162">-ResizeTimeout</span></span>
<span data-ttu-id="723e1-163">Время и время времени, заданное для узлы на компьютере, в пуле.</span><span class="sxs-lookup"><span data-stu-id="723e1-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="723e1-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="723e1-164">-StartTask</span></span>
<span data-ttu-id="723e1-165">Указывает спецификацию задачи начала для пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="723e1-166">Задача начала происходит, когда узел компьютеров присоединяется к пулу или перезагружается или перезагружается.</span><span class="sxs-lookup"><span data-stu-id="723e1-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="723e1-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="723e1-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="723e1-168">Определяет целевое количество выделенных вычислительных узлов для пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="723e1-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="723e1-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="723e1-170">Определяет целевое количество узлов для вычисления с низким приоритетом, которые необходимо выделить для пула.</span><span class="sxs-lookup"><span data-stu-id="723e1-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="723e1-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="723e1-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="723e1-172">Определяет политику планирования задач, например ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="723e1-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="723e1-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="723e1-173">-UserAccount</span></span>
<span data-ttu-id="723e1-174">Список учетных записей пользователей, которые будут созданы для каждого узла в пуле.</span><span class="sxs-lookup"><span data-stu-id="723e1-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="723e1-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="723e1-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="723e1-176">Определяет параметры конфигурации для пула на инфраструктуре виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="723e1-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="723e1-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="723e1-177">-VirtualMachineSize</span></span>
<span data-ttu-id="723e1-178">Определяет размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="723e1-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="723e1-179">Дополнительные сведения о размерах виртуальных машин см. в сведениях о размерах виртуальных машин https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) (на сайте Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="723e1-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="723e1-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="723e1-180">-Confirm</span></span>
<span data-ttu-id="723e1-181">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723e1-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723e1-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723e1-182">-WhatIf</span></span>
<span data-ttu-id="723e1-183">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723e1-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723e1-184">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="723e1-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723e1-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723e1-185">CommonParameters</span></span>
<span data-ttu-id="723e1-186">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723e1-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723e1-187">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="723e1-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723e1-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="723e1-188">INPUTS</span></span>

### <span data-ttu-id="723e1-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="723e1-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="723e1-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="723e1-190">OUTPUTS</span></span>

### <span data-ttu-id="723e1-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="723e1-191">System.Void</span></span>

## <span data-ttu-id="723e1-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="723e1-192">NOTES</span></span>

## <span data-ttu-id="723e1-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="723e1-193">RELATED LINKS</span></span>

[<span data-ttu-id="723e1-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="723e1-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="723e1-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="723e1-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="723e1-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="723e1-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="723e1-197">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="723e1-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
