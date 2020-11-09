---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311756"
---
# <span data-ttu-id="a16f4-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="a16f4-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="a16f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a16f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a16f4-103">Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a16f4-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="a16f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a16f4-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a16f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a16f4-106">Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a16f4-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="a16f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a16f4-107">EXAMPLES</span></span>

### <span data-ttu-id="a16f4-108">Пример 1: Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a16f4-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="a16f4-109">Эти команды создают шаблон образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a16f4-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="a16f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a16f4-110">PARAMETERS</span></span>

### <span data-ttu-id="a16f4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a16f4-111">-AsJob</span></span>
<span data-ttu-id="a16f4-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a16f4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a16f4-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="a16f4-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="a16f4-114">Максимальная длительность ожидания при построении шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="a16f4-115">Чтобы использовать значение по умолчанию (4 часа), не заключайте или указывайте 0.</span><span class="sxs-lookup"><span data-stu-id="a16f4-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-116">-Настройка</span><span class="sxs-lookup"><span data-stu-id="a16f4-116">-Customize</span></span>
<span data-ttu-id="a16f4-117">Задает свойства, используемые для описания этапов настройки изображения, например источника изображения и т. д. Для конструирования ознакомьтесь с разделом "Заметки" для настройки свойств и создания хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a16f4-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16f4-118">-DefaultProfile</span></span>
<span data-ttu-id="a16f4-119">Region HideParameter учетные данные, учетную запись, клиента и подписку, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a16f4-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-120">-Распространение</span><span class="sxs-lookup"><span data-stu-id="a16f4-120">-Distribute</span></span>
<span data-ttu-id="a16f4-121">Целевые объекты распространения, к которым нужно перейти из вывода изображения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="a16f4-122">Для конструирования ознакомьтесь с разделом "Заметки" в разделе "распространение свойств" и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a16f4-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="a16f4-123">-ImageTemplateName</span></span>
<span data-ttu-id="a16f4-124">Имя шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="a16f4-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="a16f4-126">Время окончания последнего выполнения (UTC).</span><span class="sxs-lookup"><span data-stu-id="a16f4-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="a16f4-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="a16f4-128">Подробные сведения о состоянии последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="a16f4-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="a16f4-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="a16f4-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="a16f4-130">Состояние последнего прогона.</span><span class="sxs-lookup"><span data-stu-id="a16f4-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="a16f4-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="a16f4-132">Дочернее состояние последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="a16f4-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="a16f4-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="a16f4-134">Время начала последнего выполнения (UTC).</span><span class="sxs-lookup"><span data-stu-id="a16f4-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-135">-Location</span><span class="sxs-lookup"><span data-stu-id="a16f4-135">-Location</span></span>
<span data-ttu-id="a16f4-136">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a16f4-136">Resource location.</span></span>

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

### <span data-ttu-id="a16f4-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="a16f4-137">-NoWait</span></span>
<span data-ttu-id="a16f4-138">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a16f4-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a16f4-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="a16f4-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="a16f4-140">Код ошибки при подготовке.</span><span class="sxs-lookup"><span data-stu-id="a16f4-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="a16f4-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="a16f4-142">Подробное сообщение об ошибке при подготовке.</span><span class="sxs-lookup"><span data-stu-id="a16f4-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="a16f4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16f4-143">-ResourceGroupName</span></span>
<span data-ttu-id="a16f4-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a16f4-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="a16f4-145">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="a16f4-145">-Source</span></span>
<span data-ttu-id="a16f4-146">Описывает источник образа виртуальной машины для сборки, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="a16f4-147">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SOURCE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a16f4-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a16f4-148">-SubscriptionId</span></span>
<span data-ttu-id="a16f4-149">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a16f4-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="a16f4-150">-Tag</span></span>
<span data-ttu-id="a16f4-151">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a16f4-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a16f4-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a16f4-153">Идентификатор пользователя, которому назначена идентификация.</span><span class="sxs-lookup"><span data-stu-id="a16f4-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="a16f4-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a16f4-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="a16f4-155">Размер диска операционной системы в ГБ.</span><span class="sxs-lookup"><span data-stu-id="a16f4-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="a16f4-156">Чтобы использовать размер диска ОС Azure по умолчанию, пропустите или укажите значение 0.</span><span class="sxs-lookup"><span data-stu-id="a16f4-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16f4-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="a16f4-157">-VMProfileVmSize</span></span>
<span data-ttu-id="a16f4-158">Размер виртуальной машины, используемой для создания, настройки и захвата изображений.</span><span class="sxs-lookup"><span data-stu-id="a16f4-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="a16f4-159">Пропустите или укажите пустую строку, чтобы использовать значение по умолчанию (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="a16f4-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="a16f4-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="a16f4-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="a16f4-161">Идентификатор ресурса уже существующей подсети.</span><span class="sxs-lookup"><span data-stu-id="a16f4-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="a16f4-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a16f4-162">-Confirm</span></span>
<span data-ttu-id="a16f4-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a16f4-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16f4-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16f4-164">-WhatIf</span></span>
<span data-ttu-id="a16f4-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a16f4-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16f4-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a16f4-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16f4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16f4-167">CommonParameters</span></span>
<span data-ttu-id="a16f4-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a16f4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16f4-169">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16f4-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16f4-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a16f4-170">INPUTS</span></span>

## <span data-ttu-id="a16f4-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16f4-171">OUTPUTS</span></span>

### <span data-ttu-id="a16f4-172">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="a16f4-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="a16f4-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a16f4-173">NOTES</span></span>

<span data-ttu-id="a16f4-174">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a16f4-174">ALIASES</span></span>

<span data-ttu-id="a16f4-175">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a16f4-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a16f4-176">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a16f4-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a16f4-177">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a16f4-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a16f4-178">Настройка <IImageTemplateCustomizer [] >: определяет свойства, используемые для описания шагов настройки изображения, таких как источник изображения и т. д.</span><span class="sxs-lookup"><span data-stu-id="a16f4-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="a16f4-179">`Type <String>`: Тип средства настройки, которое вы хотите использовать для изображения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="a16f4-180">Например, Shell может быть настройка оболочки</span><span class="sxs-lookup"><span data-stu-id="a16f4-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="a16f4-181">`[Name <String>]`: Понятное имя, которое предоставляет контекст на этапе настройки</span><span class="sxs-lookup"><span data-stu-id="a16f4-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="a16f4-182">Выровнять <IImageTemplateDistributor [] >: целевые объекты распределения, на которые нужно перейти в выходном изображении.</span><span class="sxs-lookup"><span data-stu-id="a16f4-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="a16f4-183">`RunOutputName <String>`: Имя, которое будет использоваться для связанного RunOutput.</span><span class="sxs-lookup"><span data-stu-id="a16f4-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="a16f4-184">`Type <String>`: Тип распределения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="a16f4-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Теги, которые будут применяться к артефакту после его создания или обновления распространителем.</span><span class="sxs-lookup"><span data-stu-id="a16f4-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="a16f4-186">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="a16f4-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="a16f4-187">SOURCE <IImageTemplateSource> (источник): описывает источник образа виртуальной машины для сборки, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="a16f4-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="a16f4-188">`Type <String>`: Определяет тип исходного изображения, с которым вы хотите начать.</span><span class="sxs-lookup"><span data-stu-id="a16f4-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="a16f4-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a16f4-189">RELATED LINKS</span></span>

