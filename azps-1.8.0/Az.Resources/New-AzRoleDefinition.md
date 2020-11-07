---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 25f0227cad9299de8a04d0bfcfde16e9728dcc7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729371"
---
# <span data-ttu-id="bd742-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd742-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="bd742-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd742-102">SYNOPSIS</span></span>
<span data-ttu-id="bd742-103">Создание настраиваемой роли в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="bd742-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="bd742-104">Укажите в качестве входных данных либо файл определения роли в формате JSON, либо объект PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="bd742-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="bd742-105">Сначала используйте команду Get-AzRoleDefinition, чтобы создать объект определения базовой роли.</span><span class="sxs-lookup"><span data-stu-id="bd742-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="bd742-106">Затем измените его свойства в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="bd742-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="bd742-107">Наконец, используйте эту команду, чтобы создать настраиваемую роль с помощью определения роли.</span><span class="sxs-lookup"><span data-stu-id="bd742-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="bd742-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd742-108">SYNTAX</span></span>

### <span data-ttu-id="bd742-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd742-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd742-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd742-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd742-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd742-111">DESCRIPTION</span></span>
<span data-ttu-id="bd742-112">Командлет New-AzRoleDefinition создает настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="bd742-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="bd742-113">Предоставьте определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="bd742-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="bd742-114">Определение роли ввода должно содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="bd742-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="bd742-115">DisplayName: имя настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="bd742-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="bd742-116">Описание: краткое описание роли, предоставляющей доступ, предоставленный ролью.</span><span class="sxs-lookup"><span data-stu-id="bd742-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="bd742-117">Действия. набор операций, для доступа к которым настраиваемая роль предоставляет доступ.</span><span class="sxs-lookup"><span data-stu-id="bd742-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="bd742-118">Используйте Get-AzProviderOperation для получения операции для поставщиков ресурсов Azure, которые можно защитить с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="bd742-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="bd742-119">Ниже приведены некоторые допустимые строки операций.</span><span class="sxs-lookup"><span data-stu-id="bd742-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="bd742-120">"\*/Read" предоставляет доступ к операциям чтения всех поставщиков ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bd742-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="bd742-121">"Microsoft. Network/\*/Read" предоставляет доступ к операциям чтения для всех типов ресурсов в поставщике ресурсов Microsoft. Network для Azure.</span><span class="sxs-lookup"><span data-stu-id="bd742-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="bd742-122">"Microsoft. COMPUTE/virtualMachines/\*" предоставляет доступ ко всем операциям виртуальных машин и его дочерним типам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd742-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="bd742-123">AssignableScopes: набор областей (подписок или групп ресурсов для Azure), в которых настраиваемая роль будет доступна для назначения.</span><span class="sxs-lookup"><span data-stu-id="bd742-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="bd742-124">С помощью AssignableScopes вы можете сделать настраиваемую роль доступной для назначения только для подписок или групп ресурсов, которым он нужен, и не очень бессрочным для остальных подписок и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd742-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="bd742-125">Ниже перечислены некоторые допустимые назначаемые области.</span><span class="sxs-lookup"><span data-stu-id="bd742-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="bd742-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": делает роль доступной для назначения в двух подписках.</span><span class="sxs-lookup"><span data-stu-id="bd742-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="bd742-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": роль становится доступной для назначения в одной подписке.</span><span class="sxs-lookup"><span data-stu-id="bd742-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="bd742-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": роль станет доступна для задания только в группе сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd742-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="bd742-129">Определение роли ввода может содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="bd742-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="bd742-130">Неизмененные данные: набор операций, которые необходимо исключить из действий для определения действующих действий для настраиваемой роли.</span><span class="sxs-lookup"><span data-stu-id="bd742-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="bd742-131">Если вы не хотите предоставлять доступ в особой роли, вы можете использовать ненужные функции, чтобы исключить их, вместо того чтобы указывать все операции, отличные от той, которые выполняются в действиях.</span><span class="sxs-lookup"><span data-stu-id="bd742-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="bd742-132">Макрокоманды: набор операций с данными, к которым настраиваемая роль предоставляет доступ.</span><span class="sxs-lookup"><span data-stu-id="bd742-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="bd742-133">NotDataActions: набор операций, которые должны быть исключены из действий с типом данных для определения эффективных операций с пользовательскими ролями.</span><span class="sxs-lookup"><span data-stu-id="bd742-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective dataactions for the custom role.</span></span>
<span data-ttu-id="bd742-134">Если вы не хотите предоставлять доступ к определенной операции с данными в настраиваемой роли, вы можете использовать NotDataActions, чтобы исключить ее, вместо того чтобы указывать все операции, кроме указанной в действиях.</span><span class="sxs-lookup"><span data-stu-id="bd742-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="bd742-135">Примечание. Если пользователю назначена роль, указывающая на операцию в состоянии "не отменять", а другая роль предоставляет доступ к одной и той же операции, пользователь сможет выполнить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="bd742-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="bd742-136">"Мои изменения" не является правилом запретов — это просто удобный способ создания набора разрешенных операций, если требуется исключить определенные операции.</span><span class="sxs-lookup"><span data-stu-id="bd742-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="bd742-137">Ниже приведен пример определения роли JSON, которое может быть предоставлено в виде входных данных {"имя": "обновленная роль", "Описание": "может отслеживать все ресурсы, запускать и перезапускать виртуальные машины", "действия": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/Restart/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action", "незащищенные" \] : \[ "* /Write" \] , "Actions": " \[ Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/большие/двоичные \] объекты/BLOB/ \[ записи" \] , "NotDataActions": \[ "storageAccounts") \]</span><span class="sxs-lookup"><span data-stu-id="bd742-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="bd742-138">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd742-138">EXAMPLES</span></span>

### <span data-ttu-id="bd742-139">Создание с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="bd742-139">Create using PSRoleDefinitionObject</span></span>
```
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

### <span data-ttu-id="bd742-140">Создание с помощью JSON File</span><span class="sxs-lookup"><span data-stu-id="bd742-140">Create using JSON file</span></span>
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="bd742-141">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd742-141">PARAMETERS</span></span>

### <span data-ttu-id="bd742-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd742-142">-DefaultProfile</span></span>
<span data-ttu-id="bd742-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd742-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd742-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bd742-144">-InputFile</span></span>
<span data-ttu-id="bd742-145">Имя файла, в котором содержится одно определение роли JSON.</span><span class="sxs-lookup"><span data-stu-id="bd742-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="bd742-146">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="bd742-146">-Role</span></span>
<span data-ttu-id="bd742-147">Объект определения роли.</span><span class="sxs-lookup"><span data-stu-id="bd742-147">Role definition object.</span></span>

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

### <span data-ttu-id="bd742-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd742-148">CommonParameters</span></span>
<span data-ttu-id="bd742-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd742-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd742-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd742-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd742-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd742-151">INPUTS</span></span>

### <span data-ttu-id="bd742-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="bd742-152">None</span></span>

## <span data-ttu-id="bd742-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd742-153">OUTPUTS</span></span>

### <span data-ttu-id="bd742-154">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd742-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="bd742-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd742-155">NOTES</span></span>
<span data-ttu-id="bd742-156">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="bd742-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bd742-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd742-157">RELATED LINKS</span></span>

[<span data-ttu-id="bd742-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="bd742-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="bd742-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd742-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="bd742-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd742-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="bd742-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bd742-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

