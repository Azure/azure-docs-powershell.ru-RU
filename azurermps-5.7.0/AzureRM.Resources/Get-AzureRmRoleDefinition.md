---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567407"
---
# <span data-ttu-id="76254-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="76254-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="76254-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76254-102">SYNOPSIS</span></span>
<span data-ttu-id="76254-103">Список всех ролей Azure RBAC, доступных для назначения.</span><span class="sxs-lookup"><span data-stu-id="76254-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76254-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76254-104">SYNTAX</span></span>

### <span data-ttu-id="76254-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76254-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76254-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76254-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76254-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="76254-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76254-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76254-108">DESCRIPTION</span></span>
<span data-ttu-id="76254-109">Используйте команду Get-AzureRmRoleDefinition с определенным именем роли, чтобы просмотреть сведения о ней.</span><span class="sxs-lookup"><span data-stu-id="76254-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="76254-110">Для проверки отдельных операций, к которым роль предоставляет доступ, просмотрите свойства Actions и "ненужные" роли.</span><span class="sxs-lookup"><span data-stu-id="76254-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="76254-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76254-111">EXAMPLES</span></span>

### <span data-ttu-id="76254-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76254-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="76254-113">Получение определения роли читателя</span><span class="sxs-lookup"><span data-stu-id="76254-113">Get the Reader role definition</span></span>

### <span data-ttu-id="76254-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="76254-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="76254-115">Список всех определений ролей RBAC</span><span class="sxs-lookup"><span data-stu-id="76254-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="76254-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76254-116">PARAMETERS</span></span>

### <span data-ttu-id="76254-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="76254-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="76254-118">При указании отображаются все определения ролей.</span><span class="sxs-lookup"><span data-stu-id="76254-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76254-119">-Custom</span><span class="sxs-lookup"><span data-stu-id="76254-119">-Custom</span></span>
<span data-ttu-id="76254-120">Если задано, в каталоге отображаются только пользовательские роли, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="76254-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76254-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76254-121">-DefaultProfile</span></span>
<span data-ttu-id="76254-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76254-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76254-123">-ID</span><span class="sxs-lookup"><span data-stu-id="76254-123">-Id</span></span>
<span data-ttu-id="76254-124">Идентификатор определения роли.</span><span class="sxs-lookup"><span data-stu-id="76254-124">Role definition Id.</span></span>

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

### <span data-ttu-id="76254-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76254-125">-Name</span></span>
<span data-ttu-id="76254-126">Имя определения роли.</span><span class="sxs-lookup"><span data-stu-id="76254-126">Role definition name.</span></span>
<span data-ttu-id="76254-127">Например, читатель, участник, участник виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76254-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76254-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="76254-128">-Scope</span></span>
<span data-ttu-id="76254-129">Область определения роли.</span><span class="sxs-lookup"><span data-stu-id="76254-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76254-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76254-130">CommonParameters</span></span>
<span data-ttu-id="76254-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76254-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76254-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76254-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76254-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76254-133">INPUTS</span></span>

### <span data-ttu-id="76254-134">Подстрок</span><span class="sxs-lookup"><span data-stu-id="76254-134">String</span></span>
<span data-ttu-id="76254-135">Параметр scope принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="76254-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="76254-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76254-136">OUTPUTS</span></span>

### <span data-ttu-id="76254-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. System. Resources. Authorization. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="76254-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="76254-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="76254-138">NOTES</span></span>
<span data-ttu-id="76254-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="76254-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="76254-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76254-140">RELATED LINKS</span></span>

[<span data-ttu-id="76254-141">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="76254-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="76254-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="76254-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="76254-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="76254-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="76254-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="76254-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

