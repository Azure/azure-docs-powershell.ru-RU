---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235392"
---
# <span data-ttu-id="146f3-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="146f3-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="146f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="146f3-102">SYNOPSIS</span></span>
<span data-ttu-id="146f3-103">Обновление существующего назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="146f3-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="146f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="146f3-104">SYNTAX</span></span>

### <span data-ttu-id="146f3-105">RoleAssignmentParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="146f3-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="146f3-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="146f3-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="146f3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="146f3-107">DESCRIPTION</span></span>
<span data-ttu-id="146f3-108">Для изменения существующего задания используйте команду "New-AzRoleAssignment".</span><span class="sxs-lookup"><span data-stu-id="146f3-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="146f3-109">Описанием может быть любая допустимая строка, используемая для diferentiate друг от друга.</span><span class="sxs-lookup"><span data-stu-id="146f3-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="146f3-110">Если условие не задано, необходимо также настроить версию Condition, но если вы обновляете условие, которое не требуется.</span><span class="sxs-lookup"><span data-stu-id="146f3-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="146f3-111">Версию условия можно обновить с 1,0 на 2,0, но нельзя вернуть обратно.</span><span class="sxs-lookup"><span data-stu-id="146f3-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="146f3-112">Будьте внимательны, так как 2,0 не retrocompatible с 1,0.</span><span class="sxs-lookup"><span data-stu-id="146f3-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="146f3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="146f3-113">EXAMPLES</span></span>

### <span data-ttu-id="146f3-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="146f3-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="146f3-115">Обновление существующего назначения роли путем изменения объекта</span><span class="sxs-lookup"><span data-stu-id="146f3-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="146f3-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="146f3-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="146f3-117">Обновление существующего назначения роли с помощью файла</span><span class="sxs-lookup"><span data-stu-id="146f3-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="146f3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="146f3-118">PARAMETERS</span></span>

### <span data-ttu-id="146f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146f3-119">-DefaultProfile</span></span>
<span data-ttu-id="146f3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="146f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="146f3-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="146f3-121">-InputFile</span></span>
<span data-ttu-id="146f3-122">Имя файла, содержащее одно определение роли.</span><span class="sxs-lookup"><span data-stu-id="146f3-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="146f3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="146f3-123">-InputObject</span></span>
<span data-ttu-id="146f3-124">Назначение ролей.</span><span class="sxs-lookup"><span data-stu-id="146f3-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="146f3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="146f3-125">-PassThru</span></span>
<span data-ttu-id="146f3-126">При указании отображается новое назначение роли</span><span class="sxs-lookup"><span data-stu-id="146f3-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="146f3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="146f3-127">-Confirm</span></span>
<span data-ttu-id="146f3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="146f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="146f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="146f3-129">-WhatIf</span></span>
<span data-ttu-id="146f3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="146f3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="146f3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="146f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="146f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146f3-132">CommonParameters</span></span>
<span data-ttu-id="146f3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="146f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146f3-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="146f3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146f3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="146f3-135">INPUTS</span></span>

### <span data-ttu-id="146f3-136">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="146f3-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="146f3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="146f3-137">OUTPUTS</span></span>

### <span data-ttu-id="146f3-138">Microsoft. Azure. Commands. Resources. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="146f3-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="146f3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="146f3-139">NOTES</span></span>

## <span data-ttu-id="146f3-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="146f3-140">RELATED LINKS</span></span>
