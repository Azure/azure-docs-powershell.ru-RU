---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914378"
---
# <span data-ttu-id="59a79-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="59a79-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="59a79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59a79-102">SYNOPSIS</span></span>
<span data-ttu-id="59a79-103">Список всех ролей Azure RBAC, доступных для назначения.</span><span class="sxs-lookup"><span data-stu-id="59a79-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59a79-104">SYNTAX</span></span>

### <span data-ttu-id="59a79-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a79-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a79-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a79-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a79-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a79-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a79-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59a79-108">DESCRIPTION</span></span>
<span data-ttu-id="59a79-109">Используйте команду Get-AzureRmRoleDefinition с определенным именем роли, чтобы просмотреть сведения о ней.</span><span class="sxs-lookup"><span data-stu-id="59a79-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="59a79-110">Для проверки отдельных операций, к которым роль предоставляет доступ, просмотрите свойства Actions и "ненужные" роли.</span><span class="sxs-lookup"><span data-stu-id="59a79-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="59a79-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59a79-111">EXAMPLES</span></span>

### <span data-ttu-id="59a79-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59a79-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="59a79-113">Получение определения роли читателя</span><span class="sxs-lookup"><span data-stu-id="59a79-113">Get the Reader role definition</span></span>

### <span data-ttu-id="59a79-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59a79-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="59a79-115">Список всех определений ролей RBAC</span><span class="sxs-lookup"><span data-stu-id="59a79-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="59a79-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59a79-116">PARAMETERS</span></span>

### <span data-ttu-id="59a79-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="59a79-117">-Custom</span></span>
<span data-ttu-id="59a79-118">Если задано, в каталоге отображаются только пользовательские роли, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="59a79-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="59a79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a79-119">-DefaultProfile</span></span>
<span data-ttu-id="59a79-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59a79-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a79-121">-ID</span><span class="sxs-lookup"><span data-stu-id="59a79-121">-Id</span></span>
<span data-ttu-id="59a79-122">Идентификатор определения роли.</span><span class="sxs-lookup"><span data-stu-id="59a79-122">Role definition Id.</span></span>

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

### <span data-ttu-id="59a79-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59a79-123">-Name</span></span>
<span data-ttu-id="59a79-124">Имя определения роли.</span><span class="sxs-lookup"><span data-stu-id="59a79-124">Role definition name.</span></span>
<span data-ttu-id="59a79-125">Например, читатель, участник, участник виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="59a79-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="59a79-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="59a79-126">-Scope</span></span>
<span data-ttu-id="59a79-127">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="59a79-127">Role definition scope.</span></span>

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

### <span data-ttu-id="59a79-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a79-128">CommonParameters</span></span>
<span data-ttu-id="59a79-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59a79-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a79-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a79-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a79-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59a79-131">INPUTS</span></span>

### <span data-ttu-id="59a79-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59a79-132">System.String</span></span>
<span data-ttu-id="59a79-133">Параметры: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59a79-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="59a79-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="59a79-134">System.Guid</span></span>

### <span data-ttu-id="59a79-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59a79-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59a79-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59a79-136">OUTPUTS</span></span>

### <span data-ttu-id="59a79-137">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="59a79-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="59a79-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="59a79-138">NOTES</span></span>
<span data-ttu-id="59a79-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="59a79-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="59a79-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59a79-140">RELATED LINKS</span></span>

[<span data-ttu-id="59a79-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59a79-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="59a79-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59a79-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="59a79-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="59a79-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="59a79-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="59a79-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

