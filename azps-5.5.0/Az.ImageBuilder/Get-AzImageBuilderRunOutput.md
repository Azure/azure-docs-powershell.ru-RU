---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226521"
---
# <span data-ttu-id="842ed-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="842ed-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="842ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="842ed-102">SYNOPSIS</span></span>
<span data-ttu-id="842ed-103">Получить указанный выход запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="842ed-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="842ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="842ed-104">SYNTAX</span></span>

### <span data-ttu-id="842ed-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="842ed-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="842ed-106">Получить</span><span class="sxs-lookup"><span data-stu-id="842ed-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="842ed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="842ed-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="842ed-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="842ed-108">DESCRIPTION</span></span>
<span data-ttu-id="842ed-109">Получить указанный выход запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="842ed-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="842ed-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="842ed-110">EXAMPLES</span></span>

### <span data-ttu-id="842ed-111">Пример 1. Список всех результатов запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="842ed-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="842ed-112">Эта команда содержит все результаты запуска, полученные по шаблону.</span><span class="sxs-lookup"><span data-stu-id="842ed-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="842ed-113">Пример 2. Получить результат запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="842ed-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="842ed-114">Эта команда возвращает результат запуска в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="842ed-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="842ed-115">Пример 3. Получить результат запуска в шаблоне</span><span class="sxs-lookup"><span data-stu-id="842ed-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="842ed-116">Эта команда возвращает результат запуска в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="842ed-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="842ed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="842ed-117">PARAMETERS</span></span>

### <span data-ttu-id="842ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842ed-118">-DefaultProfile</span></span>
<span data-ttu-id="842ed-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="842ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="842ed-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="842ed-120">-ImageTemplateName</span></span>
<span data-ttu-id="842ed-121">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="842ed-121">The name of the image Template</span></span>

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

### <span data-ttu-id="842ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="842ed-122">-InputObject</span></span>
<span data-ttu-id="842ed-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="842ed-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="842ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="842ed-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="842ed-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="842ed-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="842ed-126">-RunOutputName</span></span>
<span data-ttu-id="842ed-127">Имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="842ed-127">The name of the run output</span></span>

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

### <span data-ttu-id="842ed-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="842ed-128">-SubscriptionId</span></span>
<span data-ttu-id="842ed-129">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="842ed-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="842ed-130">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="842ed-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="842ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842ed-131">CommonParameters</span></span>
<span data-ttu-id="842ed-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="842ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842ed-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="842ed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842ed-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="842ed-134">INPUTS</span></span>

### <span data-ttu-id="842ed-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="842ed-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="842ed-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="842ed-136">OUTPUTS</span></span>

### <span data-ttu-id="842ed-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="842ed-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="842ed-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="842ed-138">NOTES</span></span>

<span data-ttu-id="842ed-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="842ed-139">ALIASES</span></span>

<span data-ttu-id="842ed-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="842ed-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="842ed-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="842ed-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="842ed-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="842ed-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="842ed-143">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="842ed-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="842ed-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="842ed-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="842ed-145">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="842ed-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="842ed-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="842ed-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="842ed-147">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="842ed-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="842ed-148">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="842ed-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="842ed-149">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="842ed-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="842ed-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="842ed-150">RELATED LINKS</span></span>

