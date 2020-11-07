---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6972d4df51222804843aa965577f7044ed4bf987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915021"
---
# <span data-ttu-id="fb555-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb555-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="fb555-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb555-102">SYNOPSIS</span></span>
<span data-ttu-id="fb555-103">Удаление назначения политики.</span><span class="sxs-lookup"><span data-stu-id="fb555-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb555-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb555-104">SYNTAX</span></span>

### <span data-ttu-id="fb555-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb555-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb555-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb555-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb555-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb555-107">DESCRIPTION</span></span>
<span data-ttu-id="fb555-108">Командлет **Remove-AzureRmPolicyAssignment** удаляет указанное назначение политики.</span><span class="sxs-lookup"><span data-stu-id="fb555-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="fb555-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb555-109">EXAMPLES</span></span>

### <span data-ttu-id="fb555-110">Пример 1: Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="fb555-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="fb555-111">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fb555-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="fb555-112">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fb555-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fb555-113">Вторая команда удаляет назначение политики с именем PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb555-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="fb555-114">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb555-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="fb555-115">Пример 2: Удаление назначения политики по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fb555-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="fb555-116">Первая команда получает группу ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fb555-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="fb555-117">Вторая команда получает назначение политики на уровне группы ресурсов и сохраняет его в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb555-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="fb555-118">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb555-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="fb555-119">В последней команде удаляется назначение политики, идентифицирующее свойство **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb555-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="fb555-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb555-120">PARAMETERS</span></span>

### <span data-ttu-id="fb555-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb555-121">-ApiVersion</span></span>
<span data-ttu-id="fb555-122">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb555-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb555-123">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="fb555-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fb555-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb555-124">-DefaultProfile</span></span>
<span data-ttu-id="fb555-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fb555-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb555-126">-ID</span><span class="sxs-lookup"><span data-stu-id="fb555-126">-Id</span></span>
<span data-ttu-id="fb555-127">Указывает полный идентификатор ресурса для назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb555-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb555-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fb555-128">-InformationAction</span></span>
<span data-ttu-id="fb555-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fb555-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="fb555-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb555-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb555-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fb555-131">Continue</span></span>
- <span data-ttu-id="fb555-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fb555-132">Ignore</span></span>
- <span data-ttu-id="fb555-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fb555-133">Inquire</span></span>
- <span data-ttu-id="fb555-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fb555-134">SilentlyContinue</span></span>
- <span data-ttu-id="fb555-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="fb555-135">Stop</span></span>
- <span data-ttu-id="fb555-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="fb555-136">Suspend</span></span>

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

### <span data-ttu-id="fb555-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fb555-137">-InformationVariable</span></span>
<span data-ttu-id="fb555-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fb555-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fb555-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb555-139">-Name</span></span>
<span data-ttu-id="fb555-140">Указывает имя назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb555-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb555-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb555-141">-Pre</span></span>
<span data-ttu-id="fb555-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="fb555-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fb555-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="fb555-143">-Scope</span></span>
<span data-ttu-id="fb555-144">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="fb555-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="fb555-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb555-145">-Confirm</span></span>
<span data-ttu-id="fb555-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb555-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb555-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb555-147">-WhatIf</span></span>
<span data-ttu-id="fb555-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb555-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb555-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb555-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb555-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb555-150">CommonParameters</span></span>
<span data-ttu-id="fb555-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb555-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb555-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb555-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb555-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb555-153">INPUTS</span></span>

## <span data-ttu-id="fb555-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb555-154">OUTPUTS</span></span>

## <span data-ttu-id="fb555-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb555-155">NOTES</span></span>

## <span data-ttu-id="fb555-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb555-156">RELATED LINKS</span></span>

[<span data-ttu-id="fb555-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb555-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fb555-158">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb555-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="fb555-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb555-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


