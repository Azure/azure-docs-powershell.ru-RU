---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078764"
---
# <span data-ttu-id="98739-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98739-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="98739-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98739-102">SYNOPSIS</span></span>
<span data-ttu-id="98739-103">Удаляет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="98739-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="98739-104">Роль, которую нужно удалить, задается с помощью свойства ID роли.</span><span class="sxs-lookup"><span data-stu-id="98739-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="98739-105">Удаление завершится сбоем, если для настраиваемой роли были заданы существующие назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="98739-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="98739-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98739-106">SYNTAX</span></span>

### <span data-ttu-id="98739-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98739-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98739-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98739-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98739-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98739-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98739-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98739-110">DESCRIPTION</span></span>
<span data-ttu-id="98739-111">Командлет Remove-AzRoleDefinition удаляет настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="98739-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="98739-112">Укажите параметр идентификатора существующей настраиваемой роли, чтобы удалить эту настраиваемую роль.</span><span class="sxs-lookup"><span data-stu-id="98739-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="98739-113">По умолчанию Remove-AzRoleDefinition запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="98739-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="98739-114">Чтобы отключить запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="98739-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="98739-115">Если вы уже намерены существующие назначения ролей для удаления, удаление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="98739-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="98739-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98739-116">EXAMPLES</span></span>

### <span data-ttu-id="98739-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98739-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="98739-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98739-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="98739-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98739-119">PARAMETERS</span></span>

### <span data-ttu-id="98739-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98739-120">-DefaultProfile</span></span>
<span data-ttu-id="98739-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98739-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98739-122">-Force</span><span class="sxs-lookup"><span data-stu-id="98739-122">-Force</span></span>
<span data-ttu-id="98739-123">Если этот параметр установлен, подтверждение перед удалением настраиваемой роли не запрашивается</span><span class="sxs-lookup"><span data-stu-id="98739-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="98739-124">-ID</span><span class="sxs-lookup"><span data-stu-id="98739-124">-Id</span></span>
<span data-ttu-id="98739-125">Идентификатор удаляемого определения роли</span><span class="sxs-lookup"><span data-stu-id="98739-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="98739-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98739-126">-InputObject</span></span>
<span data-ttu-id="98739-127">Объект, представляющий определение роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="98739-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="98739-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98739-128">-Name</span></span>
<span data-ttu-id="98739-129">Имя определения роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="98739-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="98739-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98739-130">-PassThru</span></span>
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

### <span data-ttu-id="98739-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="98739-131">-Scope</span></span>
<span data-ttu-id="98739-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="98739-132">Role definition scope.</span></span>

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

### <span data-ttu-id="98739-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98739-133">-Confirm</span></span>
<span data-ttu-id="98739-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98739-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98739-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98739-135">-WhatIf</span></span>
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

### <span data-ttu-id="98739-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98739-136">CommonParameters</span></span>
<span data-ttu-id="98739-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98739-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98739-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98739-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98739-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98739-139">INPUTS</span></span>

### <span data-ttu-id="98739-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="98739-140">System.Guid</span></span>

### <span data-ttu-id="98739-141">System. String</span><span class="sxs-lookup"><span data-stu-id="98739-141">System.String</span></span>

### <span data-ttu-id="98739-142">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98739-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="98739-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98739-143">OUTPUTS</span></span>

### <span data-ttu-id="98739-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98739-144">System.Boolean</span></span>

## <span data-ttu-id="98739-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="98739-145">NOTES</span></span>
<span data-ttu-id="98739-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="98739-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="98739-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98739-147">RELATED LINKS</span></span>

[<span data-ttu-id="98739-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98739-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="98739-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98739-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="98739-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98739-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

