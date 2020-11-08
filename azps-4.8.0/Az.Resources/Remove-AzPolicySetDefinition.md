---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235417"
---
# <span data-ttu-id="d9b37-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d9b37-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="d9b37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9b37-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b37-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="d9b37-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="d9b37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9b37-104">SYNTAX</span></span>

### <span data-ttu-id="d9b37-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9b37-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b37-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b37-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b37-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b37-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b37-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b37-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b37-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9b37-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b37-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b37-110">DESCRIPTION</span></span>
<span data-ttu-id="d9b37-111">Командлет **Remove-AzPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="d9b37-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="d9b37-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9b37-112">EXAMPLES</span></span>

### <span data-ttu-id="d9b37-113">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="d9b37-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="d9b37-114">Первая команда получает определение политики с помощью командлета Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d9b37-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="d9b37-115">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d9b37-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="d9b37-116">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d9b37-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="d9b37-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9b37-117">PARAMETERS</span></span>

### <span data-ttu-id="d9b37-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9b37-118">-ApiVersion</span></span>
<span data-ttu-id="d9b37-119">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9b37-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9b37-120">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="d9b37-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d9b37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b37-121">-DefaultProfile</span></span>
<span data-ttu-id="d9b37-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9b37-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9b37-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d9b37-123">-Force</span></span>
<span data-ttu-id="d9b37-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d9b37-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d9b37-125">-ID</span><span class="sxs-lookup"><span data-stu-id="d9b37-125">-Id</span></span>
<span data-ttu-id="d9b37-126">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="d9b37-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="d9b37-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d9b37-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="d9b37-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b37-128">-InputObject</span></span>
<span data-ttu-id="d9b37-129">Объект определения политики для удаления данных из другого командлета.</span><span class="sxs-lookup"><span data-stu-id="d9b37-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="d9b37-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b37-130">-ManagementGroupName</span></span>
<span data-ttu-id="d9b37-131">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d9b37-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="d9b37-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9b37-132">-Name</span></span>
<span data-ttu-id="d9b37-133">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="d9b37-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="d9b37-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9b37-134">-Pre</span></span>
<span data-ttu-id="d9b37-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="d9b37-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9b37-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9b37-136">-SubscriptionId</span></span>
<span data-ttu-id="d9b37-137">Идентификатор подписки для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d9b37-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="d9b37-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b37-138">-Confirm</span></span>
<span data-ttu-id="d9b37-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9b37-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b37-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b37-140">-WhatIf</span></span>
<span data-ttu-id="d9b37-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9b37-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b37-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9b37-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b37-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b37-143">CommonParameters</span></span>
<span data-ttu-id="d9b37-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9b37-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b37-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9b37-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b37-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9b37-146">INPUTS</span></span>

### <span data-ttu-id="d9b37-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d9b37-147">System.String</span></span>

### <span data-ttu-id="d9b37-148">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9b37-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d9b37-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b37-149">OUTPUTS</span></span>

### <span data-ttu-id="d9b37-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9b37-150">System.Boolean</span></span>

## <span data-ttu-id="d9b37-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9b37-151">NOTES</span></span>

## <span data-ttu-id="d9b37-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9b37-152">RELATED LINKS</span></span>
