---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242461"
---
# <span data-ttu-id="03c6f-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="03c6f-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="03c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="03c6f-103">Удаляет пользовательскую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="03c6f-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="03c6f-104">Удаляемая роль задана с помощью свойства "ИД" роли.</span><span class="sxs-lookup"><span data-stu-id="03c6f-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="03c6f-105">При существующих назначениях ролей для настраиваемой роли удаление не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="03c6f-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="03c6f-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03c6f-106">SYNTAX</span></span>

### <span data-ttu-id="03c6f-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03c6f-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c6f-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c6f-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c6f-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c6f-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c6f-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03c6f-110">DESCRIPTION</span></span>
<span data-ttu-id="03c6f-111">Новый Remove-AzRoleDefinition удаляет настраиваемую роль в azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="03c6f-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="03c6f-112">Задайте параметр Id для существующей настраиваемой роли, чтобы удалить ее.</span><span class="sxs-lookup"><span data-stu-id="03c6f-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="03c6f-113">По умолчанию Remove-AzRoleDefinition запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="03c6f-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="03c6f-114">Чтобы скрыть запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="03c6f-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="03c6f-115">При удалении существующих назначений ролей для настраиваемой роли удаление не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="03c6f-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="03c6f-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03c6f-116">EXAMPLES</span></span>

### <span data-ttu-id="03c6f-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03c6f-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="03c6f-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03c6f-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="03c6f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c6f-119">PARAMETERS</span></span>

### <span data-ttu-id="03c6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c6f-120">-DefaultProfile</span></span>
<span data-ttu-id="03c6f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03c6f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03c6f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="03c6f-122">-Force</span></span>
<span data-ttu-id="03c6f-123">Если за установлено, не вы запросит подтверждение перед удалением настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="03c6f-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="03c6f-124">-Id</span><span class="sxs-lookup"><span data-stu-id="03c6f-124">-Id</span></span>
<span data-ttu-id="03c6f-125">Id of the Role definition to be deleted</span><span class="sxs-lookup"><span data-stu-id="03c6f-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="03c6f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c6f-126">-InputObject</span></span>
<span data-ttu-id="03c6f-127">Объект, представляющий удаляемую роль.</span><span class="sxs-lookup"><span data-stu-id="03c6f-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="03c6f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="03c6f-128">-Name</span></span>
<span data-ttu-id="03c6f-129">Имя удаляемого определения роли.</span><span class="sxs-lookup"><span data-stu-id="03c6f-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="03c6f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c6f-130">-PassThru</span></span>
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

### <span data-ttu-id="03c6f-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="03c6f-131">-Scope</span></span>
<span data-ttu-id="03c6f-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="03c6f-132">Role definition scope.</span></span>

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

### <span data-ttu-id="03c6f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c6f-133">-Confirm</span></span>
<span data-ttu-id="03c6f-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="03c6f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c6f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c6f-135">-WhatIf</span></span>
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

### <span data-ttu-id="03c6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c6f-136">CommonParameters</span></span>
<span data-ttu-id="03c6f-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c6f-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c6f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c6f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03c6f-139">INPUTS</span></span>

### <span data-ttu-id="03c6f-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="03c6f-140">System.Guid</span></span>

### <span data-ttu-id="03c6f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="03c6f-141">System.String</span></span>

### <span data-ttu-id="03c6f-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="03c6f-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="03c6f-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03c6f-143">OUTPUTS</span></span>

### <span data-ttu-id="03c6f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03c6f-144">System.Boolean</span></span>

## <span data-ttu-id="03c6f-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03c6f-145">NOTES</span></span>
<span data-ttu-id="03c6f-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="03c6f-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="03c6f-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03c6f-147">RELATED LINKS</span></span>

[<span data-ttu-id="03c6f-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="03c6f-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="03c6f-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="03c6f-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="03c6f-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="03c6f-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

