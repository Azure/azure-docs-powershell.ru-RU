---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 6bf44f78c763c0150e31423acd9e3594e1baa717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904065"
---
# <span data-ttu-id="1dde3-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1dde3-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="1dde3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dde3-102">SYNOPSIS</span></span>
<span data-ttu-id="1dde3-103">Список всех ролей Azure RBAC, доступных для назначения.</span><span class="sxs-lookup"><span data-stu-id="1dde3-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="1dde3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dde3-104">SYNTAX</span></span>

### <span data-ttu-id="1dde3-105">RoleDefinitionNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dde3-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dde3-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dde3-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1dde3-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dde3-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dde3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dde3-108">DESCRIPTION</span></span>
<span data-ttu-id="1dde3-109">Используйте команду Get-AzRoleDefinition с определенным именем роли, чтобы просмотреть сведения о ней.</span><span class="sxs-lookup"><span data-stu-id="1dde3-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="1dde3-110">Для проверки отдельных операций, к которым роль предоставляет доступ, просмотрите свойства Actions и "ненужные" роли.</span><span class="sxs-lookup"><span data-stu-id="1dde3-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="1dde3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dde3-111">EXAMPLES</span></span>

### <span data-ttu-id="1dde3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1dde3-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="1dde3-113">Получение определения роли читателя</span><span class="sxs-lookup"><span data-stu-id="1dde3-113">Get the Reader role definition</span></span>

### <span data-ttu-id="1dde3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1dde3-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="1dde3-115">Список всех определений ролей RBAC</span><span class="sxs-lookup"><span data-stu-id="1dde3-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="1dde3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dde3-116">PARAMETERS</span></span>

### <span data-ttu-id="1dde3-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="1dde3-117">-Custom</span></span>
<span data-ttu-id="1dde3-118">Если задано, в каталоге отображаются только пользовательские роли, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="1dde3-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="1dde3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dde3-119">-DefaultProfile</span></span>
<span data-ttu-id="1dde3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1dde3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dde3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1dde3-121">-Id</span></span>
<span data-ttu-id="1dde3-122">Идентификатор определения роли.</span><span class="sxs-lookup"><span data-stu-id="1dde3-122">Role definition Id.</span></span>

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

### <span data-ttu-id="1dde3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1dde3-123">-Name</span></span>
<span data-ttu-id="1dde3-124">Имя определения роли.</span><span class="sxs-lookup"><span data-stu-id="1dde3-124">Role definition name.</span></span>
<span data-ttu-id="1dde3-125">Например, читатель, участник, участник виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1dde3-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="1dde3-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="1dde3-126">-Scope</span></span>
<span data-ttu-id="1dde3-127">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="1dde3-127">Role definition scope.</span></span>

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

### <span data-ttu-id="1dde3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dde3-128">CommonParameters</span></span>
<span data-ttu-id="1dde3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dde3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dde3-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dde3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dde3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dde3-131">INPUTS</span></span>

### <span data-ttu-id="1dde3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1dde3-132">System.String</span></span>

### <span data-ttu-id="1dde3-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1dde3-133">System.Guid</span></span>

### <span data-ttu-id="1dde3-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1dde3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1dde3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dde3-135">OUTPUTS</span></span>

### <span data-ttu-id="1dde3-136">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1dde3-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1dde3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dde3-137">NOTES</span></span>
<span data-ttu-id="1dde3-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="1dde3-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1dde3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dde3-139">RELATED LINKS</span></span>

[<span data-ttu-id="1dde3-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1dde3-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="1dde3-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1dde3-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="1dde3-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1dde3-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="1dde3-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1dde3-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

