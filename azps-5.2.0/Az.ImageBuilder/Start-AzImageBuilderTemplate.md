---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397148"
---
# <span data-ttu-id="97eb7-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="97eb7-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="97eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="97eb7-103">Создание артефактов из существующего шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="97eb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97eb7-104">SYNTAX</span></span>

### <span data-ttu-id="97eb7-105">Выполнить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97eb7-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="97eb7-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97eb7-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97eb7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="97eb7-108">Создание артефактов из существующего шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="97eb7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97eb7-109">EXAMPLES</span></span>

### <span data-ttu-id="97eb7-110">Пример 1. Запуск шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="97eb7-111">Эта команда запускает шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="97eb7-111">This command starts an image template.</span></span>

### <span data-ttu-id="97eb7-112">Пример 2. Запуск шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="97eb7-113">Эта команда запускает шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="97eb7-113">This command starts an image template.</span></span>

## <span data-ttu-id="97eb7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97eb7-114">PARAMETERS</span></span>

### <span data-ttu-id="97eb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97eb7-115">-AsJob</span></span>
<span data-ttu-id="97eb7-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="97eb7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="97eb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97eb7-117">-DefaultProfile</span></span>
<span data-ttu-id="97eb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97eb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97eb7-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="97eb7-119">-ImageTemplateName</span></span>
<span data-ttu-id="97eb7-120">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97eb7-121">-InputObject</span></span>
<span data-ttu-id="97eb7-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="97eb7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eb7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="97eb7-123">-NoWait</span></span>
<span data-ttu-id="97eb7-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="97eb7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="97eb7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97eb7-125">-PassThru</span></span>
<span data-ttu-id="97eb7-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="97eb7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97eb7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97eb7-127">-ResourceGroupName</span></span>
<span data-ttu-id="97eb7-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97eb7-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97eb7-129">-SubscriptionId</span></span>
<span data-ttu-id="97eb7-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97eb7-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97eb7-131">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="97eb7-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97eb7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97eb7-132">-Confirm</span></span>
<span data-ttu-id="97eb7-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97eb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97eb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97eb7-134">-WhatIf</span></span>
<span data-ttu-id="97eb7-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97eb7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97eb7-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97eb7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97eb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97eb7-137">CommonParameters</span></span>
<span data-ttu-id="97eb7-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97eb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97eb7-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97eb7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97eb7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97eb7-140">INPUTS</span></span>

### <span data-ttu-id="97eb7-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="97eb7-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="97eb7-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97eb7-142">OUTPUTS</span></span>

### <span data-ttu-id="97eb7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97eb7-143">System.Boolean</span></span>

## <span data-ttu-id="97eb7-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97eb7-144">NOTES</span></span>

<span data-ttu-id="97eb7-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97eb7-145">ALIASES</span></span>

<span data-ttu-id="97eb7-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="97eb7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97eb7-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="97eb7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97eb7-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97eb7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97eb7-149">INPUTOBJECT <IImageBuilderIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="97eb7-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97eb7-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="97eb7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97eb7-151">`[ImageTemplateName <String>]`: имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="97eb7-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="97eb7-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97eb7-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="97eb7-153">`[RunOutputName <String>]`: имя результата запуска</span><span class="sxs-lookup"><span data-stu-id="97eb7-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="97eb7-154">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97eb7-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="97eb7-155">ИД подписки является частью URI для каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="97eb7-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="97eb7-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97eb7-156">RELATED LINKS</span></span>

