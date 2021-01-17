---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408140"
---
# <span data-ttu-id="ff773-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ff773-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="ff773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff773-102">SYNOPSIS</span></span>
<span data-ttu-id="ff773-103">Удаляет назначение политики.</span><span class="sxs-lookup"><span data-stu-id="ff773-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="ff773-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff773-104">SYNTAX</span></span>

### <span data-ttu-id="ff773-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff773-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff773-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff773-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff773-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff773-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff773-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff773-108">DESCRIPTION</span></span>
<span data-ttu-id="ff773-109">Для удаления указанного назначения политики удаляется **cmdlet Remove-AzPolicyAssignment.**</span><span class="sxs-lookup"><span data-stu-id="ff773-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="ff773-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff773-110">EXAMPLES</span></span>

### <span data-ttu-id="ff773-111">Пример 1. Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="ff773-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="ff773-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="ff773-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ff773-113">Эта команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ff773-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ff773-114">Вторая команда удаляет назначение политики PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff773-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="ff773-115">Свойство **ResourceId** свойства $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff773-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="ff773-116">Пример 2. Удаление назначения политики по ИД</span><span class="sxs-lookup"><span data-stu-id="ff773-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="ff773-117">Первая команда получает группу ресурсов с именем ResourceGroup11, а затем сохраняет этот объект в $ResourceGroup переменной.</span><span class="sxs-lookup"><span data-stu-id="ff773-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="ff773-118">Вторая команда получает назначение политики на уровне группы ресурсов, а затем сохраняет его в переменной $PolicyAssignment ресурса.</span><span class="sxs-lookup"><span data-stu-id="ff773-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="ff773-119">Свойство **ResourceId** свойства $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff773-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="ff773-120">Конечная команда удаляет назначение политики, которое определяет свойство **ResourceId** $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="ff773-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="ff773-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff773-121">PARAMETERS</span></span>

### <span data-ttu-id="ff773-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ff773-122">-ApiVersion</span></span>
<span data-ttu-id="ff773-123">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff773-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ff773-124">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="ff773-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff773-125">-DefaultProfile</span></span>
<span data-ttu-id="ff773-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff773-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff773-127">-Id</span><span class="sxs-lookup"><span data-stu-id="ff773-127">-Id</span></span>
<span data-ttu-id="ff773-128">Определяет полностью определенный код ресурса для назначения политики, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff773-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff773-129">-InputObject</span></span>
<span data-ttu-id="ff773-130">Объект назначения политики, который нужно удалить из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff773-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ff773-131">-Name</span></span>
<span data-ttu-id="ff773-132">Указывает имя назначения политики, которое этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="ff773-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="ff773-133">-Pre</span></span>
<span data-ttu-id="ff773-134">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="ff773-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ff773-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="ff773-135">-Scope</span></span>
<span data-ttu-id="ff773-136">Определяет область применения политики.</span><span class="sxs-lookup"><span data-stu-id="ff773-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff773-137">-Confirm</span></span>
<span data-ttu-id="ff773-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff773-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff773-139">-WhatIf</span></span>
<span data-ttu-id="ff773-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff773-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff773-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff773-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff773-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff773-142">CommonParameters</span></span>
<span data-ttu-id="ff773-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff773-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff773-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff773-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff773-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff773-145">INPUTS</span></span>

### <span data-ttu-id="ff773-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ff773-146">System.String</span></span>

## <span data-ttu-id="ff773-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff773-147">OUTPUTS</span></span>

### <span data-ttu-id="ff773-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff773-148">System.Boolean</span></span>

## <span data-ttu-id="ff773-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff773-149">NOTES</span></span>

## <span data-ttu-id="ff773-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff773-150">RELATED LINKS</span></span>

[<span data-ttu-id="ff773-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ff773-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="ff773-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ff773-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="ff773-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="ff773-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


