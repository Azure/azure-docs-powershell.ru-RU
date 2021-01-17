---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405652"
---
# <span data-ttu-id="a3103-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3103-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="a3103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3103-102">SYNOPSIS</span></span>
<span data-ttu-id="a3103-103">Удаляет пользовательскую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a3103-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a3103-104">Удаляемая роль определяется с помощью свойства "ИД" роли.</span><span class="sxs-lookup"><span data-stu-id="a3103-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="a3103-105">При существующих назначениях ролей для настраиваемой роли удаление не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="a3103-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="a3103-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3103-106">SYNTAX</span></span>

### <span data-ttu-id="a3103-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3103-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3103-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3103-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3103-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3103-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3103-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3103-110">DESCRIPTION</span></span>
<span data-ttu-id="a3103-111">Новый Remove-AzRoleDefinition удаляет настраиваемую роль в azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="a3103-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a3103-112">Задайте параметр Id для существующей настраиваемой роли, чтобы удалить ее.</span><span class="sxs-lookup"><span data-stu-id="a3103-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="a3103-113">По умолчанию Remove-AzRoleDefinition запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a3103-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="a3103-114">Чтобы скрыть запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="a3103-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="a3103-115">При удалении существующих назначений ролей для настраиваемой роли удаление не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="a3103-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="a3103-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3103-116">EXAMPLES</span></span>

### <span data-ttu-id="a3103-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3103-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="a3103-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3103-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="a3103-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3103-119">PARAMETERS</span></span>

### <span data-ttu-id="a3103-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3103-120">-DefaultProfile</span></span>
<span data-ttu-id="a3103-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a3103-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3103-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a3103-122">-Force</span></span>
<span data-ttu-id="a3103-123">Если за установлено, не вы запрос на подтверждение перед удалением настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="a3103-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="a3103-124">-Id</span><span class="sxs-lookup"><span data-stu-id="a3103-124">-Id</span></span>
<span data-ttu-id="a3103-125">Id of the Role definition to be deleted</span><span class="sxs-lookup"><span data-stu-id="a3103-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3103-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3103-126">-InputObject</span></span>
<span data-ttu-id="a3103-127">Объект, представляющий удаляемую роль.</span><span class="sxs-lookup"><span data-stu-id="a3103-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3103-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a3103-128">-Name</span></span>
<span data-ttu-id="a3103-129">Имя удаляемого определения роли.</span><span class="sxs-lookup"><span data-stu-id="a3103-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3103-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3103-130">-PassThru</span></span>
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

### <span data-ttu-id="a3103-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="a3103-131">-Scope</span></span>
<span data-ttu-id="a3103-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="a3103-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3103-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3103-133">-Confirm</span></span>
<span data-ttu-id="a3103-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a3103-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3103-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3103-135">-WhatIf</span></span>
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

### <span data-ttu-id="a3103-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3103-136">CommonParameters</span></span>
<span data-ttu-id="a3103-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3103-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3103-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3103-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3103-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3103-139">INPUTS</span></span>

### <span data-ttu-id="a3103-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a3103-140">System.Guid</span></span>

### <span data-ttu-id="a3103-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a3103-141">System.String</span></span>

### <span data-ttu-id="a3103-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3103-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="a3103-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3103-143">OUTPUTS</span></span>

### <span data-ttu-id="a3103-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3103-144">System.Boolean</span></span>

## <span data-ttu-id="a3103-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3103-145">NOTES</span></span>
<span data-ttu-id="a3103-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="a3103-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a3103-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3103-147">RELATED LINKS</span></span>

[<span data-ttu-id="a3103-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3103-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="a3103-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3103-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="a3103-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3103-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

