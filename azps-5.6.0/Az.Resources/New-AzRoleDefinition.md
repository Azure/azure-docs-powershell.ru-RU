---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974456"
---
# <span data-ttu-id="e2fbb-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e2fbb-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="e2fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fbb-103">Создает пользовательскую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e2fbb-104">В качестве входных данных можно ввести файл определения роли JSON или объект PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="e2fbb-105">Во-первых, используйте команду Get-AzRoleDefinition для создания объекта определения базовой роли.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="e2fbb-106">Затем измените его свойства, как требуется.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="e2fbb-107">Наконец, используйте эту команду для создания пользовательской роли с помощью определения роли.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="e2fbb-108">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2fbb-108">SYNTAX</span></span>

### <span data-ttu-id="e2fbb-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2fbb-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2fbb-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2fbb-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2fbb-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2fbb-111">DESCRIPTION</span></span>
<span data-ttu-id="e2fbb-112">Этот New-AzRoleDefinition создает пользовательскую роль в azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e2fbb-113">Предопределять определение роли в качестве входных данных для команды в качестве файла JSON или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="e2fbb-114">Определение входной роли ДОЛЖНО содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="e2fbb-115">DisplayName: имя настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="e2fbb-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="e2fbb-116">Описание: краткое описание роли, которая суммирует доступ, который предоставляет роль.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="e2fbb-117">Действия: набор операций, доступ к которым предоставляет пользовательская роль.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="e2fbb-118">Используйте Get-AzProviderOperation, чтобы получить операцию для поставщиков ресурсов Azure, которые можно защищены с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="e2fbb-119">Ниже ются допустимые строки операций.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="e2fbb-120">"\*/read" предоставляет доступ к операциям чтения всем поставщикам ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="e2fbb-121">"Microsoft.Network/\*/read" предоставляет доступ к операциям чтения для всех типов ресурсов в поставщике ресурсов Microsoft.Network Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="e2fbb-122">Microsoft.Compute/virtualMa ветвях/\*" предоставляет доступ ко всем операциям виртуальной машины и ее потомковым типам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="e2fbb-123">AssignableScopes: набор областей (подписки Azure или группы ресурсов), в которых настраиваемая роль будет доступна для назначения.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="e2fbb-124">С помощью AssignableScopes вы можете сделать настраиваемую роль доступной для назначений только в необходимых подписках или группах ресурсов, а не загромождать пользовательский интерфейс для остальных подписок или групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="e2fbb-125">Ниже ются некоторые допустимые области назначения:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="e2fbb-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": делает роль доступной для назначения в двух подписках.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="e2fbb-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": делает роль доступной для назначения по одной подписке.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="e2fbb-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": делает роль доступной для назначения только в группе сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="e2fbb-129">Определение входной роли МОЖЕТ содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e2fbb-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="e2fbb-130">NotActions: набор операций, которые необходимо исключить из действий для определения эффективных действий для настраиваемой роли.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="e2fbb-131">Если вы не хотите предоставлять доступ к определенной роли для определенной операции, удобнее использовать notActions, чтобы исключить ее, а не указывать все операции, кроме конкретной.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="e2fbb-132">DataActions — набор операций с данными, доступ к которым предоставляет пользовательская роль.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="e2fbb-133">NotDataActions: набор операций, которые необходимо исключить из действий dataActions для определения эффективных действий с данными для настраиваемой роли.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="e2fbb-134">Если вы не хотите предоставлять доступ к определенной роли для определенной операции данных, удобнее использовать NotDataActions, чтобы исключить ее, а не указывать все операции, кроме этой, в действиях.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="e2fbb-135">ПРИМЕЧАНИЕ. Если пользователю назначена роль, которая указывает операцию в notActions, а также назначена другая роль, предоставляет доступ к этой же операции — пользователь сможет выполнить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="e2fbb-136">NotActions не является правилом запрета— это просто удобный способ создать набор разрешенных операций, когда нужно исключить определенные операции.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="e2fbb-137">Ниже представлен пример определения роли json, которое можно ввести { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmaоes/restart/action", "Microsoft.ClassicCompute/virtualmaиes/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="e2fbb-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="e2fbb-138">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2fbb-138">EXAMPLES</span></span>

### <span data-ttu-id="e2fbb-139">Пример 1. Создание с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="e2fbb-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="e2fbb-140">Пример 2. Создание с помощью файла JSON</span><span class="sxs-lookup"><span data-stu-id="e2fbb-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="e2fbb-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2fbb-141">PARAMETERS</span></span>

### <span data-ttu-id="e2fbb-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fbb-142">-DefaultProfile</span></span>
<span data-ttu-id="e2fbb-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2fbb-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2fbb-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e2fbb-144">-InputFile</span></span>
<span data-ttu-id="e2fbb-145">Имя файла, содержащее одно определение роли json.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fbb-146">-Роль</span><span class="sxs-lookup"><span data-stu-id="e2fbb-146">-Role</span></span>
<span data-ttu-id="e2fbb-147">Объект определения роли.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fbb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fbb-148">CommonParameters</span></span>
<span data-ttu-id="e2fbb-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fbb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fbb-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2fbb-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fbb-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2fbb-151">INPUTS</span></span>

### <span data-ttu-id="e2fbb-152">Нет</span><span class="sxs-lookup"><span data-stu-id="e2fbb-152">None</span></span>

## <span data-ttu-id="e2fbb-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2fbb-153">OUTPUTS</span></span>

### <span data-ttu-id="e2fbb-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e2fbb-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="e2fbb-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2fbb-155">NOTES</span></span>
<span data-ttu-id="e2fbb-156">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e2fbb-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e2fbb-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2fbb-157">RELATED LINKS</span></span>

[<span data-ttu-id="e2fbb-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e2fbb-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="e2fbb-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e2fbb-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="e2fbb-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e2fbb-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="e2fbb-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e2fbb-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

