---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235419"
---
# <span data-ttu-id="666fb-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="666fb-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="666fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="666fb-102">SYNOPSIS</span></span>
<span data-ttu-id="666fb-103">Удаление назначения политики.</span><span class="sxs-lookup"><span data-stu-id="666fb-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="666fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="666fb-104">SYNTAX</span></span>

### <span data-ttu-id="666fb-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="666fb-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="666fb-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="666fb-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="666fb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="666fb-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="666fb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="666fb-108">DESCRIPTION</span></span>
<span data-ttu-id="666fb-109">Командлет **Remove-AzPolicyAssignment** удаляет указанное назначение политики.</span><span class="sxs-lookup"><span data-stu-id="666fb-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="666fb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="666fb-110">EXAMPLES</span></span>

### <span data-ttu-id="666fb-111">Пример 1: Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="666fb-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="666fb-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="666fb-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="666fb-113">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="666fb-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="666fb-114">Вторая команда удаляет назначение политики с именем PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="666fb-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="666fb-115">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="666fb-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="666fb-116">Пример 2: Удаление назначения политики по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="666fb-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="666fb-117">Первая команда получает группу ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="666fb-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="666fb-118">Вторая команда получает назначение политики на уровне группы ресурсов и сохраняет его в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="666fb-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="666fb-119">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="666fb-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="666fb-120">В последней команде удаляется назначение политики, идентифицирующее свойство **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="666fb-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="666fb-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="666fb-121">PARAMETERS</span></span>

### <span data-ttu-id="666fb-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="666fb-122">-ApiVersion</span></span>
<span data-ttu-id="666fb-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="666fb-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="666fb-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="666fb-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="666fb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666fb-125">-DefaultProfile</span></span>
<span data-ttu-id="666fb-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="666fb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="666fb-127">-ID</span><span class="sxs-lookup"><span data-stu-id="666fb-127">-Id</span></span>
<span data-ttu-id="666fb-128">Указывает полный идентификатор ресурса для назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="666fb-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="666fb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="666fb-129">-InputObject</span></span>
<span data-ttu-id="666fb-130">Объект назначения политики для удаления данных из другого командлета.</span><span class="sxs-lookup"><span data-stu-id="666fb-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="666fb-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="666fb-131">-Name</span></span>
<span data-ttu-id="666fb-132">Указывает имя назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="666fb-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="666fb-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="666fb-133">-Pre</span></span>
<span data-ttu-id="666fb-134">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="666fb-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="666fb-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="666fb-135">-Scope</span></span>
<span data-ttu-id="666fb-136">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="666fb-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="666fb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="666fb-137">-Confirm</span></span>
<span data-ttu-id="666fb-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="666fb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666fb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666fb-139">-WhatIf</span></span>
<span data-ttu-id="666fb-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="666fb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="666fb-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="666fb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="666fb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666fb-142">CommonParameters</span></span>
<span data-ttu-id="666fb-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="666fb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666fb-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="666fb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666fb-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="666fb-145">INPUTS</span></span>

### <span data-ttu-id="666fb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="666fb-146">System.String</span></span>

## <span data-ttu-id="666fb-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="666fb-147">OUTPUTS</span></span>

### <span data-ttu-id="666fb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="666fb-148">System.Boolean</span></span>

## <span data-ttu-id="666fb-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="666fb-149">NOTES</span></span>

## <span data-ttu-id="666fb-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="666fb-150">RELATED LINKS</span></span>

[<span data-ttu-id="666fb-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="666fb-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="666fb-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="666fb-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="666fb-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="666fb-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


