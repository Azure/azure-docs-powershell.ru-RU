---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990783"
---
# <span data-ttu-id="c2361-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2361-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="c2361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2361-102">SYNOPSIS</span></span>
<span data-ttu-id="c2361-103">Здесь перечислены все доступные для назначения роли azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="c2361-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="c2361-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2361-104">SYNTAX</span></span>

### <span data-ttu-id="c2361-105">RoleDefinitionNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2361-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2361-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2361-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2361-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2361-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2361-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2361-108">DESCRIPTION</span></span>
<span data-ttu-id="c2361-109">Используйте команду Get-AzRoleDefinition с именем конкретной роли, чтобы просмотреть сведения о ней.</span><span class="sxs-lookup"><span data-stu-id="c2361-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="c2361-110">Чтобы проверить отдельные операции, доступ к которые предоставляет роль, просмотрите свойства "Действия" и "Действия" для роли.</span><span class="sxs-lookup"><span data-stu-id="c2361-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="c2361-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2361-111">EXAMPLES</span></span>

### <span data-ttu-id="c2361-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2361-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="c2361-113">Получить определение роли "Читатель"</span><span class="sxs-lookup"><span data-stu-id="c2361-113">Get the Reader role definition</span></span>

### <span data-ttu-id="c2361-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2361-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="c2361-115">Список всех определений ролей СРБ</span><span class="sxs-lookup"><span data-stu-id="c2361-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="c2361-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2361-116">PARAMETERS</span></span>

### <span data-ttu-id="c2361-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="c2361-117">-Custom</span></span>
<span data-ttu-id="c2361-118">Если задан этот условия, отображаются только настраиваемые созданные роли в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c2361-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2361-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2361-119">-DefaultProfile</span></span>
<span data-ttu-id="c2361-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2361-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2361-121">-Id</span><span class="sxs-lookup"><span data-stu-id="c2361-121">-Id</span></span>
<span data-ttu-id="c2361-122">ИД определения роли.</span><span class="sxs-lookup"><span data-stu-id="c2361-122">Role definition Id.</span></span>

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

### <span data-ttu-id="c2361-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c2361-123">-Name</span></span>
<span data-ttu-id="c2361-124">Имя определения роли.</span><span class="sxs-lookup"><span data-stu-id="c2361-124">Role definition name.</span></span>
<span data-ttu-id="c2361-125">Например, читатель, участник, участник виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c2361-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2361-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="c2361-126">-Scope</span></span>
<span data-ttu-id="c2361-127">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="c2361-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2361-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2361-128">CommonParameters</span></span>
<span data-ttu-id="c2361-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2361-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2361-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2361-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2361-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2361-131">INPUTS</span></span>

### <span data-ttu-id="c2361-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c2361-132">System.String</span></span>

### <span data-ttu-id="c2361-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c2361-133">System.Guid</span></span>

### <span data-ttu-id="c2361-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2361-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2361-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2361-135">OUTPUTS</span></span>

### <span data-ttu-id="c2361-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2361-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="c2361-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2361-137">NOTES</span></span>
<span data-ttu-id="c2361-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="c2361-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c2361-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2361-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2361-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2361-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="c2361-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c2361-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="c2361-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2361-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="c2361-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c2361-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

