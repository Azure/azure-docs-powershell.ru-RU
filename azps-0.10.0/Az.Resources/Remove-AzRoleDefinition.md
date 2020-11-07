---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f31a09f0d148d25796e157eb300a6f5918dade44
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910839"
---
# <span data-ttu-id="45605-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="45605-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="45605-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45605-102">SYNOPSIS</span></span>
<span data-ttu-id="45605-103">Удаляет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="45605-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="45605-104">Роль, которую нужно удалить, задается с помощью свойства ID роли.</span><span class="sxs-lookup"><span data-stu-id="45605-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="45605-105">Удаление завершится сбоем, если для настраиваемой роли были заданы существующие назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="45605-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="45605-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45605-106">SYNTAX</span></span>

### <span data-ttu-id="45605-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45605-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45605-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45605-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45605-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45605-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45605-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45605-110">DESCRIPTION</span></span>
<span data-ttu-id="45605-111">Командлет Remove-AzRoleDefinition удаляет настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="45605-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="45605-112">Укажите параметр идентификатора существующей настраиваемой роли, чтобы удалить эту настраиваемую роль.</span><span class="sxs-lookup"><span data-stu-id="45605-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="45605-113">По умолчанию Remove-AzRoleDefinition запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="45605-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="45605-114">Чтобы отключить запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="45605-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="45605-115">Если вы уже намерены существующие назначения ролей для удаления, удаление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="45605-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="45605-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45605-116">EXAMPLES</span></span>

### <span data-ttu-id="45605-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45605-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="45605-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="45605-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="45605-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45605-119">PARAMETERS</span></span>

### <span data-ttu-id="45605-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45605-120">-DefaultProfile</span></span>
<span data-ttu-id="45605-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="45605-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45605-122">-Force</span><span class="sxs-lookup"><span data-stu-id="45605-122">-Force</span></span>
<span data-ttu-id="45605-123">Если этот параметр установлен, подтверждение перед удалением настраиваемой роли не запрашивается</span><span class="sxs-lookup"><span data-stu-id="45605-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="45605-124">-ID</span><span class="sxs-lookup"><span data-stu-id="45605-124">-Id</span></span>
<span data-ttu-id="45605-125">Идентификатор удаляемого определения роли</span><span class="sxs-lookup"><span data-stu-id="45605-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="45605-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45605-126">-InputObject</span></span>
<span data-ttu-id="45605-127">Объект, представляющий определение роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="45605-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="45605-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45605-128">-Name</span></span>
<span data-ttu-id="45605-129">Имя определения роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="45605-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="45605-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45605-130">-PassThru</span></span>
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

### <span data-ttu-id="45605-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="45605-131">-Scope</span></span>
<span data-ttu-id="45605-132">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="45605-132">Role definition scope.</span></span>

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

### <span data-ttu-id="45605-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45605-133">-Confirm</span></span>
<span data-ttu-id="45605-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45605-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45605-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45605-135">-WhatIf</span></span>
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

### <span data-ttu-id="45605-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45605-136">CommonParameters</span></span>
<span data-ttu-id="45605-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45605-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45605-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45605-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45605-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45605-139">INPUTS</span></span>

### <span data-ttu-id="45605-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="45605-140">System.Guid</span></span>

### <span data-ttu-id="45605-141">System. String</span><span class="sxs-lookup"><span data-stu-id="45605-141">System.String</span></span>

### <span data-ttu-id="45605-142">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="45605-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="45605-143">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45605-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="45605-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45605-144">OUTPUTS</span></span>

### <span data-ttu-id="45605-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45605-145">System.Boolean</span></span>

## <span data-ttu-id="45605-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="45605-146">NOTES</span></span>
<span data-ttu-id="45605-147">Ключевые слова: Azure, AZ, ARM, ресурс, управление, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="45605-147">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="45605-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45605-148">RELATED LINKS</span></span>

[<span data-ttu-id="45605-149">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="45605-149">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="45605-150">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="45605-150">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="45605-151">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="45605-151">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

