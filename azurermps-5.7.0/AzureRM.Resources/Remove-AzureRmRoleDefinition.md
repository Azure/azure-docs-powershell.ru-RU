---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567941"
---
# <span data-ttu-id="a6904-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a6904-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="a6904-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6904-102">SYNOPSIS</span></span>
<span data-ttu-id="a6904-103">Удаляет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a6904-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a6904-104">Роль, которую нужно удалить, задается с помощью свойства ID роли.</span><span class="sxs-lookup"><span data-stu-id="a6904-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="a6904-105">Удаление завершится сбоем, если для настраиваемой роли были заданы существующие назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="a6904-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6904-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6904-106">SYNTAX</span></span>

### <span data-ttu-id="a6904-107">RoleDefinitionIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6904-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6904-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6904-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6904-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6904-109">DESCRIPTION</span></span>
<span data-ttu-id="a6904-110">Командлет Remove-AzureRmRoleDefinition удаляет настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="a6904-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a6904-111">Укажите параметр идентификатора существующей настраиваемой роли, чтобы удалить эту настраиваемую роль.</span><span class="sxs-lookup"><span data-stu-id="a6904-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="a6904-112">По умолчанию Remove-AzureRmRoleDefinition запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a6904-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="a6904-113">Чтобы отключить запрос, используйте параметр Force.</span><span class="sxs-lookup"><span data-stu-id="a6904-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="a6904-114">Если вы уже намерены существующие назначения ролей для удаления, удаление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="a6904-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="a6904-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6904-115">EXAMPLES</span></span>

### <span data-ttu-id="a6904-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6904-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="a6904-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6904-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="a6904-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6904-118">PARAMETERS</span></span>

### <span data-ttu-id="a6904-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6904-119">-DefaultProfile</span></span>
<span data-ttu-id="a6904-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a6904-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a6904-121">-Force</span></span>
<span data-ttu-id="a6904-122">Если этот параметр установлен, подтверждение перед удалением настраиваемой роли не запрашивается</span><span class="sxs-lookup"><span data-stu-id="a6904-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-123">-ID</span><span class="sxs-lookup"><span data-stu-id="a6904-123">-Id</span></span>
<span data-ttu-id="a6904-124">Идентификатор удаляемого определения роли</span><span class="sxs-lookup"><span data-stu-id="a6904-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6904-125">-Name</span></span>
<span data-ttu-id="a6904-126">Имя определения роли, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a6904-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6904-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="a6904-128">-Scope</span></span>
<span data-ttu-id="a6904-129">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="a6904-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6904-130">-Confirm</span></span>
<span data-ttu-id="a6904-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6904-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6904-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6904-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6904-133">CommonParameters</span></span>
<span data-ttu-id="a6904-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6904-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6904-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6904-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6904-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6904-136">INPUTS</span></span>

### <span data-ttu-id="a6904-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="a6904-137">None</span></span>
<span data-ttu-id="a6904-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a6904-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6904-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6904-139">OUTPUTS</span></span>

### <span data-ttu-id="a6904-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6904-140">System.Boolean</span></span>

## <span data-ttu-id="a6904-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6904-141">NOTES</span></span>
<span data-ttu-id="a6904-142">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="a6904-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a6904-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6904-143">RELATED LINKS</span></span>

[<span data-ttu-id="a6904-144">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a6904-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="a6904-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a6904-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="a6904-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a6904-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

