---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734242"
---
# <span data-ttu-id="8f843-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f843-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="8f843-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f843-102">SYNOPSIS</span></span>
<span data-ttu-id="8f843-103">Удаление назначения политики.</span><span class="sxs-lookup"><span data-stu-id="8f843-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f843-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f843-104">SYNTAX</span></span>

### <span data-ttu-id="8f843-105">Заданный параметр имени назначения политики.</span><span class="sxs-lookup"><span data-stu-id="8f843-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="8f843-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f843-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f843-107">Заданный параметр идентификатора назначения политики.</span><span class="sxs-lookup"><span data-stu-id="8f843-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f843-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f843-108">DESCRIPTION</span></span>
<span data-ttu-id="8f843-109">Командлет **Remove-AzureRmPolicyAssignment** удаляет указанное назначение политики.</span><span class="sxs-lookup"><span data-stu-id="8f843-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="8f843-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f843-110">EXAMPLES</span></span>

### <span data-ttu-id="8f843-111">Пример 1: Удаление назначения политики по имени и области</span><span class="sxs-lookup"><span data-stu-id="8f843-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="8f843-112">Первая команда получает группу ресурсов с именем ResourceGroup11 с помощью командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8f843-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="8f843-113">Команда сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8f843-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="8f843-114">Вторая команда удаляет назначение политики с именем PolicyAssignment07, назначенное на уровне группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f843-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="8f843-115">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f843-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="8f843-116">Пример 2: Удаление назначения политики по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="8f843-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="8f843-117">Первая команда получает группу ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8f843-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="8f843-118">Вторая команда получает назначение политики на уровне группы ресурсов и сохраняет его в переменной $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8f843-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8f843-119">Свойство **ResourceId** для $ResourceGroup определяет группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f843-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="8f843-120">В последней команде удаляется назначение политики, идентифицирующее свойство **ResourceId** для $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8f843-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="8f843-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f843-121">PARAMETERS</span></span>

### <span data-ttu-id="8f843-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f843-122">-ApiVersion</span></span>
<span data-ttu-id="8f843-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f843-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f843-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="8f843-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8f843-125">-ID</span><span class="sxs-lookup"><span data-stu-id="8f843-125">-Id</span></span>
<span data-ttu-id="8f843-126">Указывает полный идентификатор ресурса для назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f843-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f843-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8f843-127">-InformationAction</span></span>
<span data-ttu-id="8f843-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8f843-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8f843-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f843-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f843-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8f843-130">Continue</span></span>
- <span data-ttu-id="8f843-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8f843-131">Ignore</span></span>
- <span data-ttu-id="8f843-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8f843-132">Inquire</span></span>
- <span data-ttu-id="8f843-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8f843-133">SilentlyContinue</span></span>
- <span data-ttu-id="8f843-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="8f843-134">Stop</span></span>
- <span data-ttu-id="8f843-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="8f843-135">Suspend</span></span>

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

### <span data-ttu-id="8f843-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8f843-136">-InformationVariable</span></span>
<span data-ttu-id="8f843-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8f843-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8f843-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f843-138">-Name</span></span>
<span data-ttu-id="8f843-139">Указывает имя назначения политики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8f843-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f843-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f843-140">-Pre</span></span>
<span data-ttu-id="8f843-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="8f843-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8f843-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="8f843-142">-Scope</span></span>
<span data-ttu-id="8f843-143">Указывает область применения политики.</span><span class="sxs-lookup"><span data-stu-id="8f843-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f843-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f843-144">-Confirm</span></span>
<span data-ttu-id="8f843-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f843-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f843-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f843-146">-WhatIf</span></span>
<span data-ttu-id="8f843-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f843-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f843-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f843-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f843-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f843-149">-DefaultProfile</span></span>
<span data-ttu-id="8f843-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f843-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f843-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f843-151">CommonParameters</span></span>
<span data-ttu-id="8f843-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f843-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f843-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f843-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f843-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f843-154">INPUTS</span></span>

## <span data-ttu-id="8f843-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f843-155">OUTPUTS</span></span>

### <span data-ttu-id="8f843-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f843-156">System.Boolean</span></span>

## <span data-ttu-id="8f843-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f843-157">NOTES</span></span>

## <span data-ttu-id="8f843-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f843-158">RELATED LINKS</span></span>

[<span data-ttu-id="8f843-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f843-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8f843-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f843-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8f843-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8f843-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


