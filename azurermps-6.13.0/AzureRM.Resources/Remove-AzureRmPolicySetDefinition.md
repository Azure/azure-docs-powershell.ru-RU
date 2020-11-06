---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9fcae03dba32aff18d2863c557c5827cf3e9d95e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560680"
---
# <span data-ttu-id="16e67-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="16e67-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="16e67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16e67-102">SYNOPSIS</span></span>
<span data-ttu-id="16e67-103">Удаление определения политики.</span><span class="sxs-lookup"><span data-stu-id="16e67-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16e67-104">SYNTAX</span></span>

### <span data-ttu-id="16e67-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16e67-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e67-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e67-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16e67-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e67-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e67-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e67-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e67-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e67-109">DESCRIPTION</span></span>
<span data-ttu-id="16e67-110">Командлет **Remove-AzureRmPolicySetDefinition** удаляет определение политики.</span><span class="sxs-lookup"><span data-stu-id="16e67-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="16e67-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16e67-111">EXAMPLES</span></span>

### <span data-ttu-id="16e67-112">Пример 1: Удаление определения политики для идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="16e67-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="16e67-113">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="16e67-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="16e67-114">Команда сохраняет его в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="16e67-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="16e67-115">Вторая команда удаляет определение политики, определяемое свойством **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="16e67-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="16e67-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16e67-116">PARAMETERS</span></span>

### <span data-ttu-id="16e67-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="16e67-117">-ApiVersion</span></span>
<span data-ttu-id="16e67-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16e67-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="16e67-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="16e67-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="16e67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e67-120">-DefaultProfile</span></span>
<span data-ttu-id="16e67-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16e67-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16e67-122">-Force</span><span class="sxs-lookup"><span data-stu-id="16e67-122">-Force</span></span>
<span data-ttu-id="16e67-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="16e67-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16e67-124">-ID</span><span class="sxs-lookup"><span data-stu-id="16e67-124">-Id</span></span>
<span data-ttu-id="16e67-125">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="16e67-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="16e67-126">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="16e67-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="16e67-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="16e67-127">-ManagementGroupName</span></span>
<span data-ttu-id="16e67-128">Имя группы управления для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="16e67-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="16e67-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16e67-129">-Name</span></span>
<span data-ttu-id="16e67-130">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="16e67-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="16e67-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="16e67-131">-Pre</span></span>
<span data-ttu-id="16e67-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="16e67-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="16e67-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16e67-133">-SubscriptionId</span></span>
<span data-ttu-id="16e67-134">Идентификатор подписки для определения политики, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="16e67-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="16e67-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16e67-135">-Confirm</span></span>
<span data-ttu-id="16e67-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16e67-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e67-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e67-137">-WhatIf</span></span>
<span data-ttu-id="16e67-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16e67-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e67-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16e67-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e67-140">CommonParameters</span></span>
<span data-ttu-id="16e67-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16e67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e67-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e67-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e67-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16e67-143">INPUTS</span></span>

### <span data-ttu-id="16e67-144">System. String</span><span class="sxs-lookup"><span data-stu-id="16e67-144">System.String</span></span>

### <span data-ttu-id="16e67-145">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="16e67-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="16e67-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e67-146">OUTPUTS</span></span>

### <span data-ttu-id="16e67-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16e67-147">System.Boolean</span></span>

## <span data-ttu-id="16e67-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="16e67-148">NOTES</span></span>

## <span data-ttu-id="16e67-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16e67-149">RELATED LINKS</span></span>
