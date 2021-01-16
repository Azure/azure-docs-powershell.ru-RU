---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407663"
---
# <span data-ttu-id="6275e-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="6275e-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="6275e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6275e-102">SYNOPSIS</span></span>
<span data-ttu-id="6275e-103">Удаление спецификации шаблона</span><span class="sxs-lookup"><span data-stu-id="6275e-103">Removes a Template Spec</span></span>

## <span data-ttu-id="6275e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6275e-104">SYNTAX</span></span>

### <span data-ttu-id="6275e-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6275e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6275e-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6275e-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6275e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6275e-107">DESCRIPTION</span></span>
<span data-ttu-id="6275e-108">Удаляет указанную спецификацию шаблона. Если указан параметр version **-Version,** будет удалена только указанная версия.</span><span class="sxs-lookup"><span data-stu-id="6275e-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="6275e-109">Если конкретные версии не предоставляются, шаблон спецификации и все его версии будут удалены.</span><span class="sxs-lookup"><span data-stu-id="6275e-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="6275e-110">Если флаг **-Force** присутствует, запрос на удаление подтверждения не будет.</span><span class="sxs-lookup"><span data-stu-id="6275e-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="6275e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6275e-111">EXAMPLES</span></span>

### <span data-ttu-id="6275e-112">Пример 1. Удаление определенной версии по имени</span><span class="sxs-lookup"><span data-stu-id="6275e-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6275e-113">Удаляет версию "1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="6275e-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6275e-114">Пример 2. Удаление определенной версии по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="6275e-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6275e-115">Удаляет версию "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG из подид \{ \} подписки.</span><span class="sxs-lookup"><span data-stu-id="6275e-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="6275e-116">Пример 3. Удаление спецификации шаблона и всех версий по имени</span><span class="sxs-lookup"><span data-stu-id="6275e-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="6275e-117">Удаляет спецификацию шаблона с именем MyTemplateSpec и все его версии в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="6275e-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6275e-118">Пример 3. Удаление спецификации шаблона и всех версий по кодам ресурсов</span><span class="sxs-lookup"><span data-stu-id="6275e-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="6275e-119">Удаляет спецификацию шаблона с именем MyTemplateSpec и все его версии в группе ресурсов myRG подписки \{ \} subId.</span><span class="sxs-lookup"><span data-stu-id="6275e-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="6275e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6275e-120">PARAMETERS</span></span>

### <span data-ttu-id="6275e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6275e-121">-DefaultProfile</span></span>
<span data-ttu-id="6275e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6275e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6275e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6275e-123">-Force</span></span>
<span data-ttu-id="6275e-124">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6275e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6275e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6275e-125">-Name</span></span>
<span data-ttu-id="6275e-126">Имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="6275e-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6275e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6275e-127">-ResourceGroupName</span></span>
<span data-ttu-id="6275e-128">Имя группы ресурсов шаблона спецификации.</span><span class="sxs-lookup"><span data-stu-id="6275e-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6275e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6275e-129">-ResourceId</span></span>
<span data-ttu-id="6275e-130">Полное имя ресурса спецификации шаблона. Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="6275e-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6275e-131">-Версия</span><span class="sxs-lookup"><span data-stu-id="6275e-131">-Version</span></span>
<span data-ttu-id="6275e-132">Версия спецификации шаблона, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6275e-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6275e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6275e-133">-Confirm</span></span>
<span data-ttu-id="6275e-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6275e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6275e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6275e-135">-WhatIf</span></span>
<span data-ttu-id="6275e-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6275e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6275e-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6275e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6275e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6275e-138">CommonParameters</span></span>
<span data-ttu-id="6275e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6275e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6275e-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6275e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6275e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6275e-141">INPUTS</span></span>

### <span data-ttu-id="6275e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6275e-142">System.String</span></span>

## <span data-ttu-id="6275e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6275e-143">OUTPUTS</span></span>

### <span data-ttu-id="6275e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6275e-144">System.Boolean</span></span>

## <span data-ttu-id="6275e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6275e-145">NOTES</span></span>

## <span data-ttu-id="6275e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6275e-146">RELATED LINKS</span></span>
