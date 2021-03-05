---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 3d22fa9626d7e0e6de8baf36a07ae679ffb9ed0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013016"
---
# <span data-ttu-id="57b9f-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="57b9f-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="57b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="57b9f-103">Удаление шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="57b9f-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="57b9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57b9f-104">SYNTAX</span></span>

### <span data-ttu-id="57b9f-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57b9f-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="57b9f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57b9f-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57b9f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57b9f-107">DESCRIPTION</span></span>
<span data-ttu-id="57b9f-108">Удаление шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="57b9f-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="57b9f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="57b9f-110">Пример 1. Удаление шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="57b9f-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="57b9f-111">Эта команда удаляет шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="57b9f-111">This command removes a image template.</span></span>

### <span data-ttu-id="57b9f-112">Пример 2. Удаление шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="57b9f-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="57b9f-113">Эта команда удаляет шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="57b9f-113">This command removes a image template.</span></span>

## <span data-ttu-id="57b9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="57b9f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57b9f-115">-AsJob</span></span>
<span data-ttu-id="57b9f-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="57b9f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="57b9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b9f-117">-DefaultProfile</span></span>
<span data-ttu-id="57b9f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57b9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b9f-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="57b9f-119">-ImageTemplateName</span></span>
<span data-ttu-id="57b9f-120">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="57b9f-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b9f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57b9f-121">-InputObject</span></span>
<span data-ttu-id="57b9f-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="57b9f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57b9f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57b9f-123">-NoWait</span></span>
<span data-ttu-id="57b9f-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="57b9f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57b9f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57b9f-125">-PassThru</span></span>
<span data-ttu-id="57b9f-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="57b9f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57b9f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b9f-127">-ResourceGroupName</span></span>
<span data-ttu-id="57b9f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57b9f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b9f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57b9f-129">-SubscriptionId</span></span>
<span data-ttu-id="57b9f-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57b9f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57b9f-131">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="57b9f-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b9f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57b9f-132">-Confirm</span></span>
<span data-ttu-id="57b9f-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b9f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b9f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b9f-134">-WhatIf</span></span>
<span data-ttu-id="57b9f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b9f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b9f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57b9f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b9f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b9f-137">CommonParameters</span></span>
<span data-ttu-id="57b9f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b9f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b9f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57b9f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b9f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57b9f-140">INPUTS</span></span>

### <span data-ttu-id="57b9f-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="57b9f-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="57b9f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57b9f-142">OUTPUTS</span></span>

### <span data-ttu-id="57b9f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57b9f-143">System.Boolean</span></span>

## <span data-ttu-id="57b9f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57b9f-144">NOTES</span></span>

<span data-ttu-id="57b9f-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57b9f-145">ALIASES</span></span>

<span data-ttu-id="57b9f-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="57b9f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57b9f-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="57b9f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57b9f-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57b9f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57b9f-149">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="57b9f-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57b9f-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="57b9f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57b9f-151">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="57b9f-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="57b9f-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57b9f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="57b9f-153">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="57b9f-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="57b9f-154">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57b9f-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57b9f-155">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="57b9f-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="57b9f-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57b9f-156">RELATED LINKS</span></span>

