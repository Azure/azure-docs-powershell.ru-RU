---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397151"
---
# <span data-ttu-id="79a7d-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="79a7d-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="79a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="79a7d-103">Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="79a7d-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="79a7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79a7d-104">SYNTAX</span></span>

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

## <span data-ttu-id="79a7d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="79a7d-106">Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="79a7d-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="79a7d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="79a7d-108">Пример 1. Создание шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="79a7d-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="79a7d-109">Эти команды создают шаблон изображения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="79a7d-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="79a7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="79a7d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a7d-111">-AsJob</span></span>
<span data-ttu-id="79a7d-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="79a7d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="79a7d-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="79a7d-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="79a7d-114">Максимальная длительность, которая нужно выждать при создании шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="79a7d-115">Опустить или указать значение 0, используемого по умолчанию (4 часа).</span><span class="sxs-lookup"><span data-stu-id="79a7d-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="79a7d-116">-Customize</span><span class="sxs-lookup"><span data-stu-id="79a7d-116">-Customize</span></span>
<span data-ttu-id="79a7d-117">Определяет свойства, используемые для описания этапов настройки изображения, например источника изображений и т. д. Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для настройки свойств и создания hash table.</span><span class="sxs-lookup"><span data-stu-id="79a7d-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="79a7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a7d-118">-DefaultProfile</span></span>
<span data-ttu-id="79a7d-119">region HideParameter — учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79a7d-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a7d-120">-Distribute</span><span class="sxs-lookup"><span data-stu-id="79a7d-120">-Distribute</span></span>
<span data-ttu-id="79a7d-121">Целевые аудитории для вывода изображений.</span><span class="sxs-lookup"><span data-stu-id="79a7d-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="79a7d-122">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" свойства DISTRIBUTE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="79a7d-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="79a7d-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="79a7d-123">-ImageTemplateName</span></span>
<span data-ttu-id="79a7d-124">Имя шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="79a7d-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="79a7d-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="79a7d-126">Время окончания последнего запуска (UTC).</span><span class="sxs-lookup"><span data-stu-id="79a7d-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="79a7d-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="79a7d-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="79a7d-128">Подробные сведения о состоянии последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="79a7d-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="79a7d-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="79a7d-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="79a7d-130">Состояние последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="79a7d-130">State of the last run.</span></span>

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

### <span data-ttu-id="79a7d-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="79a7d-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="79a7d-132">Подчиненное состояние последнего запуска.</span><span class="sxs-lookup"><span data-stu-id="79a7d-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="79a7d-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="79a7d-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="79a7d-134">Время начала последнего запуска (UTC).</span><span class="sxs-lookup"><span data-stu-id="79a7d-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="79a7d-135">-Location</span><span class="sxs-lookup"><span data-stu-id="79a7d-135">-Location</span></span>
<span data-ttu-id="79a7d-136">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="79a7d-136">Resource location.</span></span>

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

### <span data-ttu-id="79a7d-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79a7d-137">-NoWait</span></span>
<span data-ttu-id="79a7d-138">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="79a7d-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79a7d-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="79a7d-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="79a7d-140">Код ошибки при сбое подготовка.</span><span class="sxs-lookup"><span data-stu-id="79a7d-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="79a7d-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="79a7d-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="79a7d-142">Подробное сообщение об ошибке при подготовках.</span><span class="sxs-lookup"><span data-stu-id="79a7d-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="79a7d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a7d-143">-ResourceGroupName</span></span>
<span data-ttu-id="79a7d-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79a7d-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="79a7d-145">-Source</span><span class="sxs-lookup"><span data-stu-id="79a7d-145">-Source</span></span>
<span data-ttu-id="79a7d-146">В нем описывается источник изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="79a7d-147">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств источника и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="79a7d-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="79a7d-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79a7d-148">-SubscriptionId</span></span>
<span data-ttu-id="79a7d-149">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="79a7d-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="79a7d-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="79a7d-150">-Tag</span></span>
<span data-ttu-id="79a7d-151">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79a7d-151">Resource tags.</span></span>

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

### <span data-ttu-id="79a7d-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="79a7d-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="79a7d-153">Идентификатор идентификатора пользователя, назначенного пользователю.</span><span class="sxs-lookup"><span data-stu-id="79a7d-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="79a7d-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="79a7d-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="79a7d-155">Размер диска ОС в ГБ.</span><span class="sxs-lookup"><span data-stu-id="79a7d-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="79a7d-156">Опустить или указать значение 0, чтобы использовать стандартный размер диска ОС Azure.</span><span class="sxs-lookup"><span data-stu-id="79a7d-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="79a7d-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="79a7d-157">-VMProfileVmSize</span></span>
<span data-ttu-id="79a7d-158">Размер виртуальной машины, используемой для создания, настройки и захвата изображений.</span><span class="sxs-lookup"><span data-stu-id="79a7d-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="79a7d-159">Опустить или указать пустую строку для использования по умолчанию (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="79a7d-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="79a7d-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="79a7d-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="79a7d-161">ИД ресурса для существующей подсети.</span><span class="sxs-lookup"><span data-stu-id="79a7d-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="79a7d-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a7d-162">-Confirm</span></span>
<span data-ttu-id="79a7d-163">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="79a7d-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a7d-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a7d-164">-WhatIf</span></span>
<span data-ttu-id="79a7d-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a7d-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a7d-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="79a7d-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a7d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a7d-167">CommonParameters</span></span>
<span data-ttu-id="79a7d-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a7d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a7d-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79a7d-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a7d-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79a7d-170">INPUTS</span></span>

## <span data-ttu-id="79a7d-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79a7d-171">OUTPUTS</span></span>

### <span data-ttu-id="79a7d-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="79a7d-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="79a7d-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79a7d-173">NOTES</span></span>

<span data-ttu-id="79a7d-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="79a7d-174">ALIASES</span></span>

<span data-ttu-id="79a7d-175">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="79a7d-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="79a7d-176">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="79a7d-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="79a7d-177">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="79a7d-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="79a7d-178">НАСТРОЙКА <IImageTemplateCustomizer[]>: определяет свойства, используемые для описания этапов настройки изображения, например источника изображений и т. д.</span><span class="sxs-lookup"><span data-stu-id="79a7d-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="79a7d-179">`Type <String>`: тип инструмента настройки, который вы хотите использовать на изображении.</span><span class="sxs-lookup"><span data-stu-id="79a7d-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="79a7d-180">Например, "Shell" может быть настраиваемым оболочкой</span><span class="sxs-lookup"><span data-stu-id="79a7d-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="79a7d-181">`[Name <String>]`: удобное имя, которое обеспечивает контекст для этого шага настройки</span><span class="sxs-lookup"><span data-stu-id="79a7d-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="79a7d-182">DISTRIBUTE <IImageTemplateDistributor[]>: целевые объекты распространения, к которые нужно перейти к выходу изображения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="79a7d-183">`RunOutputName <String>`: имя, которое будет использоваться для связанной runOutput.</span><span class="sxs-lookup"><span data-stu-id="79a7d-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="79a7d-184">`Type <String>`: Тип распределения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="79a7d-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: теги, которые будут применяться к артефакту после того, как он был создан или обновлен дистрибьютором.</span><span class="sxs-lookup"><span data-stu-id="79a7d-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="79a7d-186">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="79a7d-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="79a7d-187">SOURCE <IImageTemplateSource> : Описание источника изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="79a7d-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="79a7d-188">`Type <String>`Определяет тип изображения источника, с который вы хотите начать.</span><span class="sxs-lookup"><span data-stu-id="79a7d-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="79a7d-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79a7d-189">RELATED LINKS</span></span>

