---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401623"
---
# <span data-ttu-id="769b2-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="769b2-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="769b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="769b2-102">SYNOPSIS</span></span>
<span data-ttu-id="769b2-103">Удаляет определение набора политик.</span><span class="sxs-lookup"><span data-stu-id="769b2-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="769b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="769b2-104">SYNTAX</span></span>

### <span data-ttu-id="769b2-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="769b2-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769b2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="769b2-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769b2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="769b2-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769b2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="769b2-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="769b2-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="769b2-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="769b2-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="769b2-110">DESCRIPTION</span></span>
<span data-ttu-id="769b2-111">Для **удаления определения политики удаляется cmdlet Remove-AzPolicySetDefinition.**</span><span class="sxs-lookup"><span data-stu-id="769b2-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="769b2-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="769b2-112">EXAMPLES</span></span>

### <span data-ttu-id="769b2-113">Пример 1. Удаление определения набора политики по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="769b2-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="769b2-114">Первая команда получает определение набора политики с помощью Get-AzPolicySetDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="769b2-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="769b2-115">Команда сохраняет ее в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="769b2-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="769b2-116">Вторая команда удаляет определение набора политики, заданное **свойством ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="769b2-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="769b2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="769b2-117">PARAMETERS</span></span>

### <span data-ttu-id="769b2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="769b2-118">-ApiVersion</span></span>
<span data-ttu-id="769b2-119">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="769b2-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="769b2-120">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="769b2-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="769b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="769b2-121">-DefaultProfile</span></span>
<span data-ttu-id="769b2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="769b2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="769b2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="769b2-123">-Force</span></span>
<span data-ttu-id="769b2-124">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="769b2-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="769b2-125">-Id</span><span class="sxs-lookup"><span data-stu-id="769b2-125">-Id</span></span>
<span data-ttu-id="769b2-126">Полное определение набора политик, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="769b2-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="769b2-127">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="769b2-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="769b2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="769b2-128">-InputObject</span></span>
<span data-ttu-id="769b2-129">Объект определения, задав политику, удаляет этот результат из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769b2-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="769b2-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="769b2-130">-ManagementGroupName</span></span>
<span data-ttu-id="769b2-131">Имя группы управления определением набора политики, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="769b2-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="769b2-132">-Name</span><span class="sxs-lookup"><span data-stu-id="769b2-132">-Name</span></span>
<span data-ttu-id="769b2-133">Имя определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="769b2-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="769b2-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="769b2-134">-Pre</span></span>
<span data-ttu-id="769b2-135">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="769b2-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="769b2-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="769b2-136">-SubscriptionId</span></span>
<span data-ttu-id="769b2-137">ИД подписки, который нужно удалить в определении набора политик.</span><span class="sxs-lookup"><span data-stu-id="769b2-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="769b2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="769b2-138">-Confirm</span></span>
<span data-ttu-id="769b2-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769b2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="769b2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="769b2-140">-WhatIf</span></span>
<span data-ttu-id="769b2-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="769b2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="769b2-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="769b2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="769b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="769b2-143">CommonParameters</span></span>
<span data-ttu-id="769b2-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="769b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="769b2-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="769b2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="769b2-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="769b2-146">INPUTS</span></span>

### <span data-ttu-id="769b2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="769b2-147">System.String</span></span>

### <span data-ttu-id="769b2-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="769b2-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="769b2-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="769b2-149">OUTPUTS</span></span>

### <span data-ttu-id="769b2-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="769b2-150">System.Boolean</span></span>

## <span data-ttu-id="769b2-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="769b2-151">NOTES</span></span>

## <span data-ttu-id="769b2-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="769b2-152">RELATED LINKS</span></span>
