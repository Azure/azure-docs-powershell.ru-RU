---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 148f7b22a9df77532f574457da453e9e4b07a846
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910847"
---
# <span data-ttu-id="6cb3a-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6cb3a-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="6cb3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb3a-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="6cb3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cb3a-104">SYNTAX</span></span>

### <span data-ttu-id="6cb3a-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6cb3a-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb3a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb3a-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cb3a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb3a-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb3a-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb3a-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb3a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cb3a-109">DESCRIPTION</span></span>
<span data-ttu-id="6cb3a-110">Командлет **Remove-AzPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6cb3a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cb3a-111">EXAMPLES</span></span>

### <span data-ttu-id="6cb3a-112">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="6cb3a-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="6cb3a-113">Первая команда получает определение политики с помощью командлета Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="6cb3a-114">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="6cb3a-115">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="6cb3a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cb3a-116">PARAMETERS</span></span>

### <span data-ttu-id="6cb3a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cb3a-117">-ApiVersion</span></span>
<span data-ttu-id="6cb3a-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cb3a-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6cb3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb3a-120">-DefaultProfile</span></span>
<span data-ttu-id="6cb3a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6cb3a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb3a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb3a-122">-Force</span></span>
<span data-ttu-id="6cb3a-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6cb3a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6cb3a-124">-Id</span></span>
<span data-ttu-id="6cb3a-125">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="6cb3a-126">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6cb3a-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="6cb3a-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb3a-127">-ManagementGroupName</span></span>
<span data-ttu-id="6cb3a-128">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="6cb3a-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cb3a-129">-Name</span></span>
<span data-ttu-id="6cb3a-130">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="6cb3a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cb3a-131">-Pre</span></span>
<span data-ttu-id="6cb3a-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6cb3a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cb3a-133">-SubscriptionId</span></span>
<span data-ttu-id="6cb3a-134">Идентификатор подписки для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="6cb3a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cb3a-135">-Confirm</span></span>
<span data-ttu-id="6cb3a-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb3a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb3a-137">-WhatIf</span></span>
<span data-ttu-id="6cb3a-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb3a-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb3a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb3a-140">CommonParameters</span></span>
<span data-ttu-id="6cb3a-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cb3a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb3a-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb3a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb3a-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cb3a-143">INPUTS</span></span>

### <span data-ttu-id="6cb3a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb3a-144">System.String</span></span>

### <span data-ttu-id="6cb3a-145">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6cb3a-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6cb3a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cb3a-146">OUTPUTS</span></span>

### <span data-ttu-id="6cb3a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb3a-147">System.Boolean</span></span>

## <span data-ttu-id="6cb3a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cb3a-148">NOTES</span></span>

## <span data-ttu-id="6cb3a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cb3a-149">RELATED LINKS</span></span>
