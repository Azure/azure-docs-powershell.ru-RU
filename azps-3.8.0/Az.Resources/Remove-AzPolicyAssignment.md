---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8c7aa559ad6fde29c32f1958a4a0e2a6406ad42d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066231"
---
# <span data-ttu-id="22a31-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="22a31-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="22a31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22a31-102">SYNOPSIS</span></span>
<span data-ttu-id="22a31-103">Удаление назначения политики.</span><span class="sxs-lookup"><span data-stu-id="22a31-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="22a31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22a31-104">SYNTAX</span></span>

### <span data-ttu-id="22a31-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22a31-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a31-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22a31-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22a31-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a31-107">DESCRIPTION</span></span>
<span data-ttu-id="22a31-108">Командлет **Remove-AzPolicyAssignment** удаляет указанное назначение политики.</span><span class="sxs-lookup"><span data-stu-id="22a31-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="22a31-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22a31-109">EXAMPLES</span></span>

### <span data-ttu-id="22a31-110">Пример 1: Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="22a31-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="22a31-111">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22a31-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="22a31-112">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22a31-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="22a31-113">Вторая команда удаляет назначение политики с именем PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22a31-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="22a31-114">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22a31-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="22a31-115">Пример 2: Удаление назначения политики по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="22a31-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="22a31-116">Первая команда получает группу ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22a31-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="22a31-117">Вторая команда получает назначение политики на уровне группы ресурсов и сохраняет его в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="22a31-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="22a31-118">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22a31-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="22a31-119">В последней команде удаляется назначение политики, идентифицирующее свойство **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="22a31-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="22a31-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22a31-120">PARAMETERS</span></span>

### <span data-ttu-id="22a31-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22a31-121">-ApiVersion</span></span>
<span data-ttu-id="22a31-122">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22a31-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22a31-123">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="22a31-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22a31-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a31-124">-DefaultProfile</span></span>
<span data-ttu-id="22a31-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="22a31-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22a31-126">-ID</span><span class="sxs-lookup"><span data-stu-id="22a31-126">-Id</span></span>
<span data-ttu-id="22a31-127">Указывает полный идентификатор ресурса для назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="22a31-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22a31-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22a31-128">-Name</span></span>
<span data-ttu-id="22a31-129">Указывает имя назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="22a31-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22a31-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="22a31-130">-Pre</span></span>
<span data-ttu-id="22a31-131">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="22a31-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22a31-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="22a31-132">-Scope</span></span>
<span data-ttu-id="22a31-133">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="22a31-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="22a31-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22a31-134">-Confirm</span></span>
<span data-ttu-id="22a31-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22a31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22a31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22a31-136">-WhatIf</span></span>
<span data-ttu-id="22a31-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22a31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22a31-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22a31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22a31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a31-139">CommonParameters</span></span>
<span data-ttu-id="22a31-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22a31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a31-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22a31-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a31-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22a31-142">INPUTS</span></span>

### <span data-ttu-id="22a31-143">System. String</span><span class="sxs-lookup"><span data-stu-id="22a31-143">System.String</span></span>

## <span data-ttu-id="22a31-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a31-144">OUTPUTS</span></span>

### <span data-ttu-id="22a31-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22a31-145">System.Boolean</span></span>

## <span data-ttu-id="22a31-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="22a31-146">NOTES</span></span>

## <span data-ttu-id="22a31-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22a31-147">RELATED LINKS</span></span>

[<span data-ttu-id="22a31-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="22a31-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="22a31-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="22a31-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="22a31-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="22a31-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


