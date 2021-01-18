---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518697"
---
# <span data-ttu-id="f2ad2-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="f2ad2-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="f2ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ad2-103">Отмена длинной сборки изображения на основе шаблона</span><span class="sxs-lookup"><span data-stu-id="f2ad2-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="f2ad2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2ad2-104">SYNTAX</span></span>

### <span data-ttu-id="f2ad2-105">Отмена (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2ad2-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2ad2-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2ad2-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2ad2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2ad2-107">DESCRIPTION</span></span>
<span data-ttu-id="f2ad2-108">Отмена длинной сборки изображения на основе шаблона</span><span class="sxs-lookup"><span data-stu-id="f2ad2-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="f2ad2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2ad2-109">EXAMPLES</span></span>

### <span data-ttu-id="f2ad2-110">Пример 1. Остановка создания шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f2ad2-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="f2ad2-111">Эта команда останавливает создание шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-111">This command stops image template creation.</span></span>

### <span data-ttu-id="f2ad2-112">Пример 2. Остановка создания шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f2ad2-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="f2ad2-113">Эта команда останавливает создание шаблона изображения.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-113">This command stops image template creation.</span></span>

## <span data-ttu-id="f2ad2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2ad2-114">PARAMETERS</span></span>

### <span data-ttu-id="f2ad2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2ad2-115">-AsJob</span></span>
<span data-ttu-id="f2ad2-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f2ad2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f2ad2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ad2-117">-DefaultProfile</span></span>
<span data-ttu-id="f2ad2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ad2-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f2ad2-119">-ImageTemplateName</span></span>
<span data-ttu-id="f2ad2-120">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f2ad2-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ad2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2ad2-121">-InputObject</span></span>
<span data-ttu-id="f2ad2-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ad2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2ad2-123">-NoWait</span></span>
<span data-ttu-id="f2ad2-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f2ad2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2ad2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2ad2-125">-PassThru</span></span>
<span data-ttu-id="f2ad2-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2ad2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ad2-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2ad2-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ad2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2ad2-129">-SubscriptionId</span></span>
<span data-ttu-id="f2ad2-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2ad2-131">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2ad2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2ad2-132">-Confirm</span></span>
<span data-ttu-id="f2ad2-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ad2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ad2-134">-WhatIf</span></span>
<span data-ttu-id="f2ad2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ad2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ad2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ad2-137">CommonParameters</span></span>
<span data-ttu-id="f2ad2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ad2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2ad2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ad2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2ad2-140">INPUTS</span></span>

### <span data-ttu-id="f2ad2-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="f2ad2-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f2ad2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2ad2-142">OUTPUTS</span></span>

### <span data-ttu-id="f2ad2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2ad2-143">System.Boolean</span></span>

## <span data-ttu-id="f2ad2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2ad2-144">NOTES</span></span>

<span data-ttu-id="f2ad2-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f2ad2-145">ALIASES</span></span>

<span data-ttu-id="f2ad2-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f2ad2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2ad2-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2ad2-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2ad2-149">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f2ad2-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2ad2-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f2ad2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2ad2-151">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="f2ad2-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f2ad2-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f2ad2-153">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="f2ad2-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f2ad2-154">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f2ad2-155">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="f2ad2-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f2ad2-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2ad2-156">RELATED LINKS</span></span>

