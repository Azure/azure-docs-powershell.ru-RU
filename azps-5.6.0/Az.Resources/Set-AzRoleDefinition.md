---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971763"
---
# <span data-ttu-id="1a422-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="1a422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a422-102">SYNOPSIS</span></span>
<span data-ttu-id="1a422-103">Изменяет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="1a422-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="1a422-104">Предопределять измененное определение роли в файле JSON или в psRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="1a422-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="1a422-105">Сначала используйте команду Get-AzRoleDefinition для получения настраиваемой роли, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="1a422-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="1a422-106">Затем измените свойства, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="1a422-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="1a422-107">Наконец, сохраните определение роли с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="1a422-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="1a422-108">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a422-108">SYNTAX</span></span>

### <span data-ttu-id="1a422-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a422-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a422-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a422-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a422-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a422-111">DESCRIPTION</span></span>
<span data-ttu-id="1a422-112">Этот Set-AzRoleDefinition обновляет существующую пользовательскую роль в Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="1a422-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="1a422-113">Предопределять обновленное определение роли в качестве входных данных для команды в качестве файла JSON или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="1a422-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="1a422-114">Определение роли для обновленной настраиваемой роли должно содержать код и все остальные необходимые свойства роли, даже если они не были обновлены: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="1a422-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="1a422-115">Функции NotActions, DataActions и NotDataActions необязательны.</span><span class="sxs-lookup"><span data-stu-id="1a422-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="1a422-116">Ниже приводится пример обновленного json определения роли для Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmaservicees/restart/action", "Microsoft.ClassicCompute/virtualmaоиes/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/read" \] , "NotDataActions": \[ "Microsoft.Storage"/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="1a422-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="1a422-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a422-117">EXAMPLES</span></span>

### <span data-ttu-id="1a422-118">Пример 1. Обновление с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="1a422-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="1a422-119">Пример 2. Создание с помощью файла JSON</span><span class="sxs-lookup"><span data-stu-id="1a422-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="1a422-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a422-120">PARAMETERS</span></span>

### <span data-ttu-id="1a422-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a422-121">-DefaultProfile</span></span>
<span data-ttu-id="1a422-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a422-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a422-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1a422-123">-InputFile</span></span>
<span data-ttu-id="1a422-124">Имя файла, содержащего одно определение роли json, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="1a422-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="1a422-125">Включаем только свойства, которые нужно обновить в JSON.</span><span class="sxs-lookup"><span data-stu-id="1a422-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="1a422-126">Свойство Id является required (ИД).</span><span class="sxs-lookup"><span data-stu-id="1a422-126">Id property is Required.</span></span>

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

### <span data-ttu-id="1a422-127">-Роль</span><span class="sxs-lookup"><span data-stu-id="1a422-127">-Role</span></span>
<span data-ttu-id="1a422-128">Обновляемый объект определения роли</span><span class="sxs-lookup"><span data-stu-id="1a422-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a422-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a422-129">CommonParameters</span></span>
<span data-ttu-id="1a422-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a422-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a422-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a422-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a422-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a422-132">INPUTS</span></span>

### <span data-ttu-id="1a422-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1a422-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a422-134">OUTPUTS</span></span>

### <span data-ttu-id="1a422-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1a422-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a422-136">NOTES</span></span>
<span data-ttu-id="1a422-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="1a422-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1a422-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a422-138">RELATED LINKS</span></span>

[<span data-ttu-id="1a422-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="1a422-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="1a422-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="1a422-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="1a422-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1a422-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

