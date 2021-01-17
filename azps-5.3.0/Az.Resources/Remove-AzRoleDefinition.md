---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419772"
---
# <span data-ttu-id="3aedf-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3aedf-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="3aedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3aedf-103">Удаляет пользовательскую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3aedf-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="3aedf-104">Удаляемая роль определяется с помощью свойства "ИД" роли.</span><span class="sxs-lookup"><span data-stu-id="3aedf-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="3aedf-105">При существующих назначениях ролей для настраиваемой роли удаление не будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="3aedf-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="3aedf-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3aedf-106">SYNTAX</span></span>

### <span data-ttu-id="3aedf-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3aedf-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aedf-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aedf-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aedf-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aedf-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aedf-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aedf-110">DESCRIPTION</span></span>
<span data-ttu-id="3aedf-111">Новый Remove-AzRoleDefinition удаляет настраиваемую роль в azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="3aedf-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="3aedf-112">Задайте параметр Id для существующей настраиваемой роли, чтобы удалить ее.</span><span class="sxs-lookup"><span data-stu-id="3aedf-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="3aedf-113">По умолчанию Remove-AzRoleDefinition запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3aedf-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="3aedf-114">Чтобы скрыть запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="3aedf-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="3aedf-115">При удалении существующих назначений ролей для настраиваемой роли удаление не удастся.</span><span class="sxs-lookup"><span data-stu-id="3aedf-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="3aedf-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3aedf-116">EXAMPLES</span></span>

### <span data-ttu-id="3aedf-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3aedf-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="3aedf-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3aedf-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="3aedf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aedf-119">PARAMETERS</span></span>

### <span data-ttu-id="3aedf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aedf-120">-DefaultProfile</span></span>
<span data-ttu-id="3aedf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3aedf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aedf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3aedf-122">-Force</span></span>
<span data-ttu-id="3aedf-123">Если за установлено, не вы запросит подтверждение перед удалением настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="3aedf-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="3aedf-124">-Id</span><span class="sxs-lookup"><span data-stu-id="3aedf-124">-Id</span></span>
<span data-ttu-id="3aedf-125">Id of the Role definition to be deleted</span><span class="sxs-lookup"><span data-stu-id="3aedf-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="3aedf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aedf-126">-InputObject</span></span>
<span data-ttu-id="3aedf-127">Объект, представляющий удаляемую роль.</span><span class="sxs-lookup"><span data-stu-id="3aedf-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="3aedf-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3aedf-128">-Name</span></span>
<span data-ttu-id="3aedf-129">Имя удаляемого определения роли.</span><span class="sxs-lookup"><span data-stu-id="3aedf-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="3aedf-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aedf-130">-PassThru</span></span>
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

### <span data-ttu-id="3aedf-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="3aedf-131">-Scope</span></span>
<span data-ttu-id="3aedf-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="3aedf-132">Role definition scope.</span></span>

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

### <span data-ttu-id="3aedf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3aedf-133">-Confirm</span></span>
<span data-ttu-id="3aedf-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aedf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aedf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aedf-135">-WhatIf</span></span>
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

### <span data-ttu-id="3aedf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aedf-136">CommonParameters</span></span>
<span data-ttu-id="3aedf-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aedf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aedf-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aedf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aedf-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3aedf-139">INPUTS</span></span>

### <span data-ttu-id="3aedf-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3aedf-140">System.Guid</span></span>

### <span data-ttu-id="3aedf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3aedf-141">System.String</span></span>

### <span data-ttu-id="3aedf-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3aedf-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="3aedf-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3aedf-143">OUTPUTS</span></span>

### <span data-ttu-id="3aedf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3aedf-144">System.Boolean</span></span>

## <span data-ttu-id="3aedf-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3aedf-145">NOTES</span></span>
<span data-ttu-id="3aedf-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="3aedf-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3aedf-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aedf-147">RELATED LINKS</span></span>

[<span data-ttu-id="3aedf-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3aedf-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="3aedf-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3aedf-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="3aedf-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3aedf-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

