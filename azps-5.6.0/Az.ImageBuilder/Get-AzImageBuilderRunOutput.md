---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013080"
---
# <span data-ttu-id="2ad83-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="2ad83-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="2ad83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad83-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad83-103">Получить указанный выход запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="2ad83-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="2ad83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ad83-104">SYNTAX</span></span>

### <span data-ttu-id="2ad83-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ad83-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ad83-106">Получить</span><span class="sxs-lookup"><span data-stu-id="2ad83-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ad83-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ad83-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ad83-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ad83-108">DESCRIPTION</span></span>
<span data-ttu-id="2ad83-109">Получить указанный выход запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="2ad83-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="2ad83-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ad83-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad83-111">Пример 1. Список всех результатов запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad83-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2ad83-112">Эта команда содержит все результаты запуска, полученные по шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad83-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="2ad83-113">Пример 2. Получить результат запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad83-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2ad83-114">Эта команда возвращает результат запуска в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="2ad83-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="2ad83-115">Пример 3. Получить результат запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad83-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="2ad83-116">Эта команда возвращает результат запуска в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="2ad83-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="2ad83-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ad83-117">PARAMETERS</span></span>

### <span data-ttu-id="2ad83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad83-118">-DefaultProfile</span></span>
<span data-ttu-id="2ad83-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad83-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="2ad83-120">-ImageTemplateName</span></span>
<span data-ttu-id="2ad83-121">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="2ad83-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad83-122">-InputObject</span></span>
<span data-ttu-id="2ad83-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2ad83-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ad83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad83-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ad83-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ad83-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad83-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="2ad83-126">-RunOutputName</span></span>
<span data-ttu-id="2ad83-127">Имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="2ad83-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad83-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ad83-128">-SubscriptionId</span></span>
<span data-ttu-id="2ad83-129">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad83-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ad83-130">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2ad83-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad83-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad83-131">CommonParameters</span></span>
<span data-ttu-id="2ad83-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad83-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad83-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ad83-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad83-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ad83-134">INPUTS</span></span>

### <span data-ttu-id="2ad83-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="2ad83-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="2ad83-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ad83-136">OUTPUTS</span></span>

### <span data-ttu-id="2ad83-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="2ad83-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="2ad83-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ad83-138">NOTES</span></span>

<span data-ttu-id="2ad83-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2ad83-139">ALIASES</span></span>

<span data-ttu-id="2ad83-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2ad83-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ad83-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2ad83-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ad83-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ad83-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ad83-143">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2ad83-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ad83-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2ad83-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ad83-145">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="2ad83-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="2ad83-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ad83-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2ad83-147">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="2ad83-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="2ad83-148">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad83-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2ad83-149">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2ad83-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2ad83-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ad83-150">RELATED LINKS</span></span>

