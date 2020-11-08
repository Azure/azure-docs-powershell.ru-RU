---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078083"
---
# <span data-ttu-id="9cdb4-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="9cdb4-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="9cdb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cdb4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdb4-103">Удаление шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9cdb4-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="9cdb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cdb4-104">SYNTAX</span></span>

### <span data-ttu-id="9cdb4-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cdb4-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9cdb4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cdb4-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cdb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-107">DESCRIPTION</span></span>
<span data-ttu-id="9cdb4-108">Удаление шаблона образа виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9cdb4-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="9cdb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-109">EXAMPLES</span></span>

### <span data-ttu-id="9cdb4-110">Пример 1: Удаление шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="9cdb4-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="9cdb4-111">Эта команда удаляет шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-111">This command removes a image template.</span></span>

### <span data-ttu-id="9cdb4-112">Пример 2: Удаление шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="9cdb4-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="9cdb4-113">Эта команда удаляет шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-113">This command removes a image template.</span></span>

## <span data-ttu-id="9cdb4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-114">PARAMETERS</span></span>

### <span data-ttu-id="9cdb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cdb4-115">-AsJob</span></span>
<span data-ttu-id="9cdb4-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9cdb4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9cdb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdb4-117">-DefaultProfile</span></span>
<span data-ttu-id="9cdb4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdb4-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="9cdb4-119">-ImageTemplateName</span></span>
<span data-ttu-id="9cdb4-120">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="9cdb4-120">The name of the image Template</span></span>

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

### <span data-ttu-id="9cdb4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cdb4-121">-InputObject</span></span>
<span data-ttu-id="9cdb4-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cdb4-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="9cdb4-123">-NoWait</span></span>
<span data-ttu-id="9cdb4-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="9cdb4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cdb4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cdb4-125">-PassThru</span></span>
<span data-ttu-id="9cdb4-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9cdb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cdb4-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="9cdb4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cdb4-129">-SubscriptionId</span></span>
<span data-ttu-id="9cdb4-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9cdb4-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cdb4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cdb4-132">-Confirm</span></span>
<span data-ttu-id="9cdb4-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdb4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdb4-134">-WhatIf</span></span>
<span data-ttu-id="9cdb4-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cdb4-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdb4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdb4-137">CommonParameters</span></span>
<span data-ttu-id="9cdb4-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdb4-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cdb4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdb4-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cdb4-140">INPUTS</span></span>

### <span data-ttu-id="9cdb4-141">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="9cdb4-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="9cdb4-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-142">OUTPUTS</span></span>

### <span data-ttu-id="9cdb4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cdb4-143">System.Boolean</span></span>

## <span data-ttu-id="9cdb4-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cdb4-144">NOTES</span></span>

<span data-ttu-id="9cdb4-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-145">ALIASES</span></span>

<span data-ttu-id="9cdb4-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cdb4-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cdb4-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cdb4-149">INPUTOBJECT <IImageBuilderIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9cdb4-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cdb4-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9cdb4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cdb4-151">`[ImageTemplateName <String>]`: Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="9cdb4-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="9cdb4-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9cdb4-153">`[RunOutputName <String>]`: Имя выходных данных запуска</span><span class="sxs-lookup"><span data-stu-id="9cdb4-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="9cdb4-154">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9cdb4-155">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9cdb4-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9cdb4-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cdb4-156">RELATED LINKS</span></span>

