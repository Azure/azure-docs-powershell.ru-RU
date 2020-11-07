---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914350"
---
# <span data-ttu-id="e28bd-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e28bd-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="e28bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e28bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e28bd-103">Удаляет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e28bd-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e28bd-104">Роль, которую нужно удалить, задается с помощью свойства ID роли.</span><span class="sxs-lookup"><span data-stu-id="e28bd-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="e28bd-105">Удаление завершится сбоем, если для настраиваемой роли были заданы существующие назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="e28bd-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e28bd-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e28bd-106">SYNTAX</span></span>

### <span data-ttu-id="e28bd-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e28bd-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e28bd-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e28bd-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e28bd-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e28bd-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e28bd-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e28bd-110">DESCRIPTION</span></span>
<span data-ttu-id="e28bd-111">Командлет Remove-AzureRmRoleDefinition удаляет настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e28bd-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e28bd-112">Укажите параметр идентификатора существующей настраиваемой роли, чтобы удалить эту настраиваемую роль.</span><span class="sxs-lookup"><span data-stu-id="e28bd-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="e28bd-113">По умолчанию Remove-AzureRmRoleDefinition запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e28bd-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="e28bd-114">Чтобы отключить запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="e28bd-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="e28bd-115">Если вы уже намерены существующие назначения ролей для удаления, удаление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="e28bd-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="e28bd-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e28bd-116">EXAMPLES</span></span>

### <span data-ttu-id="e28bd-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e28bd-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="e28bd-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e28bd-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="e28bd-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e28bd-119">PARAMETERS</span></span>

### <span data-ttu-id="e28bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28bd-120">-DefaultProfile</span></span>
<span data-ttu-id="e28bd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e28bd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e28bd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e28bd-122">-Force</span></span>
<span data-ttu-id="e28bd-123">Если этот параметр установлен, подтверждение перед удалением настраиваемой роли не запрашивается</span><span class="sxs-lookup"><span data-stu-id="e28bd-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="e28bd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="e28bd-124">-Id</span></span>
<span data-ttu-id="e28bd-125">Идентификатор удаляемого определения роли</span><span class="sxs-lookup"><span data-stu-id="e28bd-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="e28bd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e28bd-126">-InputObject</span></span>
<span data-ttu-id="e28bd-127">Объект, представляющий определение роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e28bd-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="e28bd-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e28bd-128">-Name</span></span>
<span data-ttu-id="e28bd-129">Имя определения роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e28bd-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="e28bd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e28bd-130">-PassThru</span></span>
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

### <span data-ttu-id="e28bd-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="e28bd-131">-Scope</span></span>
<span data-ttu-id="e28bd-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="e28bd-132">Role definition scope.</span></span>

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

### <span data-ttu-id="e28bd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e28bd-133">-Confirm</span></span>
<span data-ttu-id="e28bd-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e28bd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e28bd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28bd-135">-WhatIf</span></span>
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

### <span data-ttu-id="e28bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28bd-136">CommonParameters</span></span>
<span data-ttu-id="e28bd-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e28bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28bd-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e28bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28bd-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e28bd-139">INPUTS</span></span>

### <span data-ttu-id="e28bd-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e28bd-140">System.Guid</span></span>

### <span data-ttu-id="e28bd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e28bd-141">System.String</span></span>

### <span data-ttu-id="e28bd-142">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e28bd-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="e28bd-143">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e28bd-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e28bd-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e28bd-144">OUTPUTS</span></span>

### <span data-ttu-id="e28bd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e28bd-145">System.Boolean</span></span>

## <span data-ttu-id="e28bd-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e28bd-146">NOTES</span></span>
<span data-ttu-id="e28bd-147">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="e28bd-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e28bd-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e28bd-148">RELATED LINKS</span></span>

[<span data-ttu-id="e28bd-149">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e28bd-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="e28bd-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e28bd-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="e28bd-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e28bd-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

