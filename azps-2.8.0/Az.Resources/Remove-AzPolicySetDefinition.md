---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 5141b4b0c7639580fbb8037193f91ac41464e233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905526"
---
# <span data-ttu-id="47a2e-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="47a2e-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="47a2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="47a2e-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="47a2e-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="47a2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47a2e-104">SYNTAX</span></span>

### <span data-ttu-id="47a2e-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47a2e-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a2e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a2e-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a2e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a2e-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a2e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a2e-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a2e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47a2e-109">DESCRIPTION</span></span>
<span data-ttu-id="47a2e-110">Командлет **Remove-AzPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="47a2e-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="47a2e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47a2e-111">EXAMPLES</span></span>

### <span data-ttu-id="47a2e-112">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="47a2e-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="47a2e-113">Первая команда получает определение политики с помощью командлета Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="47a2e-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="47a2e-114">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="47a2e-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="47a2e-115">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="47a2e-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="47a2e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47a2e-116">PARAMETERS</span></span>

### <span data-ttu-id="47a2e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47a2e-117">-ApiVersion</span></span>
<span data-ttu-id="47a2e-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47a2e-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="47a2e-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="47a2e-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="47a2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a2e-120">-DefaultProfile</span></span>
<span data-ttu-id="47a2e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47a2e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47a2e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="47a2e-122">-Force</span></span>
<span data-ttu-id="47a2e-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="47a2e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47a2e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="47a2e-124">-Id</span></span>
<span data-ttu-id="47a2e-125">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="47a2e-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="47a2e-126">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="47a2e-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="47a2e-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="47a2e-127">-ManagementGroupName</span></span>
<span data-ttu-id="47a2e-128">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="47a2e-128">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a2e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47a2e-129">-Name</span></span>
<span data-ttu-id="47a2e-130">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="47a2e-130">The policy set definition name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a2e-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="47a2e-131">-Pre</span></span>
<span data-ttu-id="47a2e-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="47a2e-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="47a2e-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47a2e-133">-SubscriptionId</span></span>
<span data-ttu-id="47a2e-134">Идентификатор подписки для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="47a2e-134">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a2e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47a2e-135">-Confirm</span></span>
<span data-ttu-id="47a2e-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47a2e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a2e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a2e-137">-WhatIf</span></span>
<span data-ttu-id="47a2e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47a2e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a2e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47a2e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a2e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a2e-140">CommonParameters</span></span>
<span data-ttu-id="47a2e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47a2e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a2e-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47a2e-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a2e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47a2e-143">INPUTS</span></span>

### <span data-ttu-id="47a2e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="47a2e-144">System.String</span></span>

### <span data-ttu-id="47a2e-145">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47a2e-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="47a2e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47a2e-146">OUTPUTS</span></span>

### <span data-ttu-id="47a2e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47a2e-147">System.Boolean</span></span>

## <span data-ttu-id="47a2e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="47a2e-148">NOTES</span></span>

## <span data-ttu-id="47a2e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47a2e-149">RELATED LINKS</span></span>
