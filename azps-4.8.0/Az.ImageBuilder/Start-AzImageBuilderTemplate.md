---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242756"
---
# <span data-ttu-id="4e173-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="4e173-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="4e173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e173-102">SYNOPSIS</span></span>
<span data-ttu-id="4e173-103">Создание артефактов из существующего шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="4e173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e173-104">SYNTAX</span></span>

### <span data-ttu-id="4e173-105">Выполнить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e173-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4e173-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e173-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e173-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e173-107">DESCRIPTION</span></span>
<span data-ttu-id="4e173-108">Создание артефактов из существующего шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="4e173-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e173-109">EXAMPLES</span></span>

### <span data-ttu-id="4e173-110">Пример 1: запуск шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="4e173-111">Эта команда запускает шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="4e173-111">This command starts an image template.</span></span>

### <span data-ttu-id="4e173-112">Пример 2: запуск шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="4e173-113">Эта команда запускает шаблон изображения.</span><span class="sxs-lookup"><span data-stu-id="4e173-113">This command starts an image template.</span></span>

## <span data-ttu-id="4e173-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e173-114">PARAMETERS</span></span>

### <span data-ttu-id="4e173-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e173-115">-AsJob</span></span>
<span data-ttu-id="4e173-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e173-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4e173-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e173-117">-DefaultProfile</span></span>
<span data-ttu-id="4e173-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e173-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e173-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="4e173-119">-ImageTemplateName</span></span>
<span data-ttu-id="4e173-120">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-120">The name of the image Template</span></span>

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

### <span data-ttu-id="4e173-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e173-121">-InputObject</span></span>
<span data-ttu-id="4e173-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4e173-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e173-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="4e173-123">-NoWait</span></span>
<span data-ttu-id="4e173-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="4e173-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e173-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e173-125">-PassThru</span></span>
<span data-ttu-id="4e173-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4e173-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4e173-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e173-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e173-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e173-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e173-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e173-129">-SubscriptionId</span></span>
<span data-ttu-id="4e173-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e173-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e173-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4e173-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e173-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e173-132">-Confirm</span></span>
<span data-ttu-id="4e173-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e173-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e173-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e173-134">-WhatIf</span></span>
<span data-ttu-id="4e173-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e173-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e173-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e173-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e173-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e173-137">CommonParameters</span></span>
<span data-ttu-id="4e173-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e173-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e173-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e173-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e173-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e173-140">INPUTS</span></span>

### <span data-ttu-id="4e173-141">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="4e173-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="4e173-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e173-142">OUTPUTS</span></span>

### <span data-ttu-id="4e173-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e173-143">System.Boolean</span></span>

## <span data-ttu-id="4e173-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e173-144">NOTES</span></span>

<span data-ttu-id="4e173-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4e173-145">ALIASES</span></span>

<span data-ttu-id="4e173-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e173-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e173-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e173-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e173-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e173-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e173-149">INPUTOBJECT <IImageBuilderIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4e173-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e173-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4e173-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e173-151">`[ImageTemplateName <String>]`: Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="4e173-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="4e173-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e173-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4e173-153">`[RunOutputName <String>]`: Имя выходных данных запуска</span><span class="sxs-lookup"><span data-stu-id="4e173-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="4e173-154">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e173-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e173-155">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4e173-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4e173-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e173-156">RELATED LINKS</span></span>

