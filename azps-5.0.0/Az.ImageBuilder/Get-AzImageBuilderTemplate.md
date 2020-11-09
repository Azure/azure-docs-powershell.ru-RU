---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311783"
---
# <span data-ttu-id="83f13-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="83f13-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="83f13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83f13-102">SYNOPSIS</span></span>
<span data-ttu-id="83f13-103">Получение сведений о шаблоне образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="83f13-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="83f13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83f13-104">SYNTAX</span></span>

### <span data-ttu-id="83f13-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83f13-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83f13-106">Получить</span><span class="sxs-lookup"><span data-stu-id="83f13-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83f13-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83f13-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83f13-108">List1</span><span class="sxs-lookup"><span data-stu-id="83f13-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83f13-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83f13-109">DESCRIPTION</span></span>
<span data-ttu-id="83f13-110">Получение сведений о шаблоне образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="83f13-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="83f13-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83f13-111">EXAMPLES</span></span>

### <span data-ttu-id="83f13-112">Пример 1: список всех шаблонов в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="83f13-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="83f13-113">В этой команде перечислены все шаблоны в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="83f13-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="83f13-114">Пример 2: список всех шаблонов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="83f13-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="83f13-115">В этой команде перечислены все шаблоны в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83f13-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="83f13-116">Пример 3: получение шаблона в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="83f13-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="83f13-117">Эта команда получает шаблон в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83f13-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="83f13-118">Пример 4: получение шаблона в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="83f13-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="83f13-119">Эта команда получает шаблон в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83f13-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="83f13-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83f13-120">PARAMETERS</span></span>

### <span data-ttu-id="83f13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f13-121">-DefaultProfile</span></span>
<span data-ttu-id="83f13-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83f13-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f13-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="83f13-123">-ImageTemplateName</span></span>
<span data-ttu-id="83f13-124">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="83f13-124">The name of the image Template</span></span>

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

### <span data-ttu-id="83f13-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f13-125">-InputObject</span></span>
<span data-ttu-id="83f13-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="83f13-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83f13-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f13-127">-ResourceGroupName</span></span>
<span data-ttu-id="83f13-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83f13-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="83f13-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83f13-129">-SubscriptionId</span></span>
<span data-ttu-id="83f13-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83f13-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="83f13-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="83f13-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83f13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f13-132">CommonParameters</span></span>
<span data-ttu-id="83f13-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83f13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f13-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83f13-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f13-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83f13-135">INPUTS</span></span>

### <span data-ttu-id="83f13-136">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="83f13-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="83f13-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83f13-137">OUTPUTS</span></span>

### <span data-ttu-id="83f13-138">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="83f13-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="83f13-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="83f13-139">NOTES</span></span>

<span data-ttu-id="83f13-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="83f13-140">ALIASES</span></span>

<span data-ttu-id="83f13-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="83f13-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83f13-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="83f13-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83f13-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83f13-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83f13-144">INPUTOBJECT <IImageBuilderIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="83f13-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83f13-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="83f13-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83f13-146">`[ImageTemplateName <String>]`: Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="83f13-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="83f13-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83f13-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="83f13-148">`[RunOutputName <String>]`: Имя выходных данных запуска</span><span class="sxs-lookup"><span data-stu-id="83f13-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="83f13-149">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83f13-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="83f13-150">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="83f13-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="83f13-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83f13-151">RELATED LINKS</span></span>

