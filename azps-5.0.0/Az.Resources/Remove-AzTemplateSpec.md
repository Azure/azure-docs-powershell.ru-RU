---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249824"
---
# <span data-ttu-id="96530-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="96530-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="96530-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96530-102">SYNOPSIS</span></span>
<span data-ttu-id="96530-103">Удаляет спецификацию шаблона</span><span class="sxs-lookup"><span data-stu-id="96530-103">Removes a Template Spec</span></span>

## <span data-ttu-id="96530-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96530-104">SYNTAX</span></span>

### <span data-ttu-id="96530-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96530-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96530-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96530-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96530-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96530-107">DESCRIPTION</span></span>
<span data-ttu-id="96530-108">Удаляет указанную спецификацию шаблона. Если указан параметр Version **(версия)** , будет удалена только указанная версия.</span><span class="sxs-lookup"><span data-stu-id="96530-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="96530-109">Если определенная версия не указана, будет удалена спецификация шаблона и все ее версии.</span><span class="sxs-lookup"><span data-stu-id="96530-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="96530-110">Если флажок **-Force** установлен, запрос на подтверждение удаления не будет указан.</span><span class="sxs-lookup"><span data-stu-id="96530-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="96530-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96530-111">EXAMPLES</span></span>

### <span data-ttu-id="96530-112">Пример 1: удаление определенной версии по имени</span><span class="sxs-lookup"><span data-stu-id="96530-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="96530-113">Удаляет версию "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="96530-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="96530-114">Пример 2: удаление определенной версии по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="96530-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="96530-115">Удаляет версию "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG" в subId подписку \{ \} .</span><span class="sxs-lookup"><span data-stu-id="96530-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="96530-116">Пример 3: Удаление спецификации шаблона и всех версий по имени</span><span class="sxs-lookup"><span data-stu-id="96530-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="96530-117">Удаляет спецификацию шаблона с именем "MyTemplateSpec" и всеми ее версиями в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="96530-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="96530-118">Пример 3: Удаление спецификации шаблона и всех версий по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="96530-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="96530-119">Удаляет спецификацию шаблона с именем "MyTemplateSpec" и всеми ее версиями в группе ресурсов "myRG" в \{ subId подписку \} .</span><span class="sxs-lookup"><span data-stu-id="96530-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="96530-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96530-120">PARAMETERS</span></span>

### <span data-ttu-id="96530-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96530-121">-DefaultProfile</span></span>
<span data-ttu-id="96530-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96530-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96530-123">-Force</span><span class="sxs-lookup"><span data-stu-id="96530-123">-Force</span></span>
<span data-ttu-id="96530-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="96530-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="96530-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96530-125">-Name</span></span>
<span data-ttu-id="96530-126">Название спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96530-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="96530-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96530-127">-ResourceGroupName</span></span>
<span data-ttu-id="96530-128">Имя группы ресурсов для спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96530-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="96530-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96530-129">-ResourceId</span></span>
<span data-ttu-id="96530-130">Полный идентификатор ресурса спецификации шаблона. Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="96530-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="96530-131">-Version</span><span class="sxs-lookup"><span data-stu-id="96530-131">-Version</span></span>
<span data-ttu-id="96530-132">Версия спецификации шаблона для удаления.</span><span class="sxs-lookup"><span data-stu-id="96530-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="96530-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96530-133">-Confirm</span></span>
<span data-ttu-id="96530-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96530-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96530-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96530-135">-WhatIf</span></span>
<span data-ttu-id="96530-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96530-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96530-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96530-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96530-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96530-138">CommonParameters</span></span>
<span data-ttu-id="96530-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96530-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96530-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96530-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96530-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96530-141">INPUTS</span></span>

### <span data-ttu-id="96530-142">System. String</span><span class="sxs-lookup"><span data-stu-id="96530-142">System.String</span></span>

## <span data-ttu-id="96530-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96530-143">OUTPUTS</span></span>

### <span data-ttu-id="96530-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96530-144">System.Boolean</span></span>

## <span data-ttu-id="96530-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="96530-145">NOTES</span></span>

## <span data-ttu-id="96530-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96530-146">RELATED LINKS</span></span>
