---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567072"
---
# <span data-ttu-id="d0c46-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d0c46-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="d0c46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0c46-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c46-103">Создание настраиваемой роли в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="d0c46-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="d0c46-104">Укажите в качестве входных данных либо файл определения роли в формате JSON, либо объект PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="d0c46-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="d0c46-105">Сначала используйте команду Get-AzureRmRoleDefinition, чтобы создать объект определения базовой роли.</span><span class="sxs-lookup"><span data-stu-id="d0c46-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="d0c46-106">Затем измените его свойства в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="d0c46-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="d0c46-107">Наконец, используйте эту команду, чтобы создать настраиваемую роль с помощью определения роли.</span><span class="sxs-lookup"><span data-stu-id="d0c46-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0c46-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0c46-108">SYNTAX</span></span>

### <span data-ttu-id="d0c46-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0c46-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c46-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0c46-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c46-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0c46-111">DESCRIPTION</span></span>
<span data-ttu-id="d0c46-112">Командлет New-AzureRmRoleDefinition создает настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="d0c46-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="d0c46-113">Предоставьте определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="d0c46-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="d0c46-114">Определение роли ввода должно содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="d0c46-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="d0c46-115">DisplayName: имя настраиваемой роли</span><span class="sxs-lookup"><span data-stu-id="d0c46-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="d0c46-116">Описание: краткое описание роли, предоставляющей доступ, предоставленный ролью.</span><span class="sxs-lookup"><span data-stu-id="d0c46-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="d0c46-117">Действия. набор операций, для доступа к которым настраиваемая роль предоставляет доступ.</span><span class="sxs-lookup"><span data-stu-id="d0c46-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="d0c46-118">Используйте Get-AzureRmProviderOperations для получения операции для поставщиков ресурсов Azure, которые можно защитить с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="d0c46-118">Use Get-AzureRmProviderOperations to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="d0c46-119">Ниже приведены некоторые допустимые строки операций.</span><span class="sxs-lookup"><span data-stu-id="d0c46-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="d0c46-120">"\*/Read" предоставляет доступ к операциям чтения всех поставщиков ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c46-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="d0c46-121">"Microsoft. Network/\*/Read" предоставляет доступ к операциям чтения для всех типов ресурсов в поставщике ресурсов Microsoft. Network для Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c46-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="d0c46-122">"Microsoft. COMPUTE/virtualMachines/\*" предоставляет доступ ко всем операциям виртуальных машин и его дочерним типам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0c46-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="d0c46-123">AssignableScopes: набор областей (подписок или групп ресурсов для Azure), в которых настраиваемая роль будет доступна для назначения.</span><span class="sxs-lookup"><span data-stu-id="d0c46-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="d0c46-124">С помощью AssignableScopes вы можете сделать настраиваемую роль доступной для назначения только для подписок или групп ресурсов, которым он нужен, и не очень бессрочным для остальных подписок и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0c46-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="d0c46-125">Ниже перечислены некоторые допустимые назначаемые области.</span><span class="sxs-lookup"><span data-stu-id="d0c46-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="d0c46-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": делает роль доступной для назначения в двух подписках.</span><span class="sxs-lookup"><span data-stu-id="d0c46-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="d0c46-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": роль становится доступной для назначения в одной подписке.</span><span class="sxs-lookup"><span data-stu-id="d0c46-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="d0c46-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": роль станет доступна для задания только в группе сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0c46-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="d0c46-129">Определение роли ввода может содержать следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="d0c46-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="d0c46-130">Неизмененные данные: набор операций, которые необходимо исключить из действий для определения действующих действий для настраиваемой роли.</span><span class="sxs-lookup"><span data-stu-id="d0c46-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="d0c46-131">Если вы не хотите предоставлять доступ в особой роли, вы можете использовать ненужные функции, чтобы исключить их, вместо того чтобы указывать все операции, отличные от той, которые выполняются в действиях.</span><span class="sxs-lookup"><span data-stu-id="d0c46-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="d0c46-132">Примечание. Если пользователю назначена роль, указывающая на операцию в состоянии "не отменять", а другая роль предоставляет доступ к одной и той же операции, пользователь сможет выполнить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="d0c46-132">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="d0c46-133">"Мои изменения" не является правилом запретов — это просто удобный способ создания набора разрешенных операций, если требуется исключить определенные операции.</span><span class="sxs-lookup"><span data-stu-id="d0c46-133">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="d0c46-134">Ниже приведен пример определения роли JSON, которое может быть предоставлено как input {"имя": "компания Contoso On-Call", "Описание": "может отслеживать вычисление, сеть и хранение, а также перезапускать виртуальные машины", "действия": "Microsoft. COMPUTE//Read", "Microsoft. Вычисление/virtualMachines/начало/действие", "Microsoft. COMPUTE/virtualMachines/downloadRemoteDesktopConnectionFile/действие", "Microsoft. COMPUTE/ \[ *virtualMachines/Restart Network/* /Read", "Microsoft. Storage//Read", "Microsoft *. Authorization* //Read", "Microsoft. Resources/Subscriptions/resourceGroups/Resources/READS/", "Microsoft. Insights/alertRules/", "Microsoft *. support/* ", " \] AssignableScopes": \[ " \]</span><span class="sxs-lookup"><span data-stu-id="d0c46-134">Following is a sample json role definition that can be provided as input { "Name": "Contoso On-call", "Description": "Can monitor compute, network and storage, and restart virtual machines", "Actions": \[ "Microsoft.Compute/ */read", "Microsoft.Compute/virtualMachines/start/action", "Microsoft.Compute/virtualMachines/restart/action", "Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action", "Microsoft.Network/* /read", "Microsoft.Storage/ */read", "Microsoft.Authorization/* /read", "Microsoft.Resources/subscriptions/resourceGroups/read", "Microsoft.Resources/subscriptions/resourceGroups/resources/read", "Microsoft.Insights/alertRules/ *", "Microsoft.Support/* " \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx","/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"\] }</span></span>

## <span data-ttu-id="d0c46-135">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0c46-135">EXAMPLES</span></span>

### <span data-ttu-id="d0c46-136">--------------------------Создание с помощью PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0c46-136">--------------------------  Create using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="d0c46-137">--------------------------Создание с помощью файла JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0c46-137">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="d0c46-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0c46-138">PARAMETERS</span></span>

### <span data-ttu-id="d0c46-139">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d0c46-139">-InputFile</span></span>
<span data-ttu-id="d0c46-140">Имя файла, в котором содержится одно определение роли JSON.</span><span class="sxs-lookup"><span data-stu-id="d0c46-140">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="d0c46-141">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="d0c46-141">-Role</span></span>
<span data-ttu-id="d0c46-142">Объект определения роли.</span><span class="sxs-lookup"><span data-stu-id="d0c46-142">Role definition object.</span></span>

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

### <span data-ttu-id="d0c46-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c46-143">-DefaultProfile</span></span>
<span data-ttu-id="d0c46-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c46-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0c46-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c46-145">CommonParameters</span></span>
<span data-ttu-id="d0c46-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0c46-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c46-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0c46-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c46-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0c46-148">INPUTS</span></span>

## <span data-ttu-id="d0c46-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0c46-149">OUTPUTS</span></span>

### <span data-ttu-id="d0c46-150">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d0c46-150">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="d0c46-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0c46-151">NOTES</span></span>
<span data-ttu-id="d0c46-152">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="d0c46-152">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d0c46-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0c46-153">RELATED LINKS</span></span>

[<span data-ttu-id="d0c46-154">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d0c46-154">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="d0c46-155">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d0c46-155">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="d0c46-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d0c46-156">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="d0c46-157">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d0c46-157">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

