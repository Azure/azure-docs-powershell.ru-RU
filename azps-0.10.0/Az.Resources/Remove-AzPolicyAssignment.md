---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8fbf6c16dce1f8d96dcc9546c801e389493e7bcd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910854"
---
# <span data-ttu-id="2a266-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2a266-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="2a266-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a266-102">SYNOPSIS</span></span>
<span data-ttu-id="2a266-103">Удаление назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2a266-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="2a266-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a266-104">SYNTAX</span></span>

### <span data-ttu-id="2a266-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a266-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a266-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a266-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a266-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a266-107">DESCRIPTION</span></span>
<span data-ttu-id="2a266-108">Командлет **Remove-AzPolicyAssignment** удаляет указанное назначение политики.</span><span class="sxs-lookup"><span data-stu-id="2a266-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="2a266-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a266-109">EXAMPLES</span></span>

### <span data-ttu-id="2a266-110">Пример 1: Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="2a266-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="2a266-111">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a266-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2a266-112">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a266-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2a266-113">Вторая команда удаляет назначение политики с именем PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a266-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="2a266-114">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a266-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="2a266-115">Пример 2: Удаление назначения политики по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="2a266-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="2a266-116">Первая команда получает группу ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a266-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2a266-117">Вторая команда получает назначение политики на уровне группы ресурсов и сохраняет его в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2a266-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2a266-118">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a266-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="2a266-119">В последней команде удаляется назначение политики, идентифицирующее свойство **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="2a266-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="2a266-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a266-120">PARAMETERS</span></span>

### <span data-ttu-id="2a266-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2a266-121">-ApiVersion</span></span>
<span data-ttu-id="2a266-122">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a266-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2a266-123">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="2a266-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2a266-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a266-124">-DefaultProfile</span></span>
<span data-ttu-id="2a266-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2a266-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a266-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2a266-126">-Id</span></span>
<span data-ttu-id="2a266-127">Указывает полный идентификатор ресурса для назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2a266-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a266-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2a266-128">-InformationAction</span></span>
<span data-ttu-id="2a266-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2a266-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2a266-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2a266-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a266-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2a266-131">Continue</span></span>
- <span data-ttu-id="2a266-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2a266-132">Ignore</span></span>
- <span data-ttu-id="2a266-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2a266-133">Inquire</span></span>
- <span data-ttu-id="2a266-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2a266-134">SilentlyContinue</span></span>
- <span data-ttu-id="2a266-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="2a266-135">Stop</span></span>
- <span data-ttu-id="2a266-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="2a266-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a266-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2a266-137">-InformationVariable</span></span>
<span data-ttu-id="2a266-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2a266-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a266-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a266-139">-Name</span></span>
<span data-ttu-id="2a266-140">Указывает имя назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2a266-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2a266-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a266-141">-Pre</span></span>
<span data-ttu-id="2a266-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2a266-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2a266-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="2a266-143">-Scope</span></span>
<span data-ttu-id="2a266-144">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="2a266-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="2a266-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a266-145">-Confirm</span></span>
<span data-ttu-id="2a266-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a266-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a266-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a266-147">-WhatIf</span></span>
<span data-ttu-id="2a266-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a266-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a266-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a266-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a266-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a266-150">CommonParameters</span></span>
<span data-ttu-id="2a266-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a266-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a266-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a266-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a266-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a266-153">INPUTS</span></span>

## <span data-ttu-id="2a266-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a266-154">OUTPUTS</span></span>

## <span data-ttu-id="2a266-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a266-155">NOTES</span></span>

## <span data-ttu-id="2a266-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a266-156">RELATED LINKS</span></span>

[<span data-ttu-id="2a266-157">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2a266-157">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2a266-158">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2a266-158">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2a266-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2a266-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


