---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411423"
---
# <span data-ttu-id="f134e-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="f134e-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="f134e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f134e-102">SYNOPSIS</span></span>
<span data-ttu-id="f134e-103">Сведения о шаблоне образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f134e-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="f134e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f134e-104">SYNTAX</span></span>

### <span data-ttu-id="f134e-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f134e-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f134e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f134e-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f134e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f134e-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f134e-108">List1</span><span class="sxs-lookup"><span data-stu-id="f134e-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f134e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f134e-109">DESCRIPTION</span></span>
<span data-ttu-id="f134e-110">Сведения о шаблоне образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f134e-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="f134e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f134e-111">EXAMPLES</span></span>

### <span data-ttu-id="f134e-112">Пример 1. Список всех шаблонов в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="f134e-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f134e-113">Эта команда содержит список всех шаблонов, которые указаны в подписке.</span><span class="sxs-lookup"><span data-stu-id="f134e-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="f134e-114">Пример 2. Список всех шаблонов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f134e-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f134e-115">Эта команда содержит список всех шаблонов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f134e-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="f134e-116">Пример 3. Получить шаблон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f134e-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f134e-117">Эта команда получает шаблон в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f134e-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="f134e-118">Пример 4. Получить шаблон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f134e-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="f134e-119">Эта команда получает шаблон в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f134e-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="f134e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f134e-120">PARAMETERS</span></span>

### <span data-ttu-id="f134e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f134e-121">-DefaultProfile</span></span>
<span data-ttu-id="f134e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f134e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f134e-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f134e-123">-ImageTemplateName</span></span>
<span data-ttu-id="f134e-124">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f134e-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f134e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f134e-125">-InputObject</span></span>
<span data-ttu-id="f134e-126">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f134e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f134e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f134e-127">-ResourceGroupName</span></span>
<span data-ttu-id="f134e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f134e-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f134e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f134e-129">-SubscriptionId</span></span>
<span data-ttu-id="f134e-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f134e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f134e-131">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f134e-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f134e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f134e-132">CommonParameters</span></span>
<span data-ttu-id="f134e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f134e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f134e-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f134e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f134e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f134e-135">INPUTS</span></span>

### <span data-ttu-id="f134e-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="f134e-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f134e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f134e-137">OUTPUTS</span></span>

### <span data-ttu-id="f134e-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="f134e-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="f134e-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f134e-139">NOTES</span></span>

<span data-ttu-id="f134e-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f134e-140">ALIASES</span></span>

<span data-ttu-id="f134e-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f134e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f134e-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f134e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f134e-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f134e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f134e-144">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f134e-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f134e-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f134e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f134e-146">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f134e-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f134e-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f134e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f134e-148">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="f134e-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f134e-149">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f134e-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f134e-150">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f134e-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f134e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f134e-151">RELATED LINKS</span></span>

