---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 0ea0c0345bc57a7b1bd5c0c4cf67d6bd400542be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729302"
---
# <span data-ttu-id="89e5f-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="89e5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="89e5f-103">Изменяет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="89e5f-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="89e5f-104">Укажите измененное определение роли либо в виде JSON-файла, либо в виде PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="89e5f-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="89e5f-105">Сначала используйте команду Get-AzRoleDefinition, чтобы получить настраиваемую роль, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="89e5f-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="89e5f-106">Затем измените свойства, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="89e5f-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="89e5f-107">Наконец, сохраните определение роли с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="89e5f-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="89e5f-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89e5f-108">SYNTAX</span></span>

### <span data-ttu-id="89e5f-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="89e5f-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89e5f-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="89e5f-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89e5f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e5f-111">DESCRIPTION</span></span>
<span data-ttu-id="89e5f-112">Командлет Set-AzRoleDefinition обновляет существующую настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="89e5f-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="89e5f-113">Предоставьте обновленное определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="89e5f-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="89e5f-114">Определение роли для обновленной настраиваемой роли должно содержать идентификатор и все другие обязательные свойства роли, даже если они не были обновлены: DisplayName, описание, действия, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="89e5f-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="89e5f-115">Не все изменения, макрокоманды, NotDataActions являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="89e5f-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="89e5f-116">Ниже приведен пример обновленного определения роли JSON для Set-AzRoleDefinition {"ИД": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "имя": "обновленная роль", "Описание": "может отслеживать все ресурсы, запускать и перезапускать виртуальные машины", "действия": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/перезапустить/действие", "Microsoft. ClassicCompute/virtualmachines/Start/Action", "незащищенные" \] : \[ "* /Write" \] , "Actions": " \[ Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/большие/двоичные \] объекты/BLOB/ \[ записи" \] , "NotDataActions": \[ "storageAccounts") \]</span><span class="sxs-lookup"><span data-stu-id="89e5f-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="89e5f-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89e5f-117">EXAMPLES</span></span>

### <span data-ttu-id="89e5f-118">Обновление с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="89e5f-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="89e5f-119">Создание с помощью JSON File</span><span class="sxs-lookup"><span data-stu-id="89e5f-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="89e5f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89e5f-120">PARAMETERS</span></span>

### <span data-ttu-id="89e5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e5f-121">-DefaultProfile</span></span>
<span data-ttu-id="89e5f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89e5f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89e5f-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="89e5f-123">-InputFile</span></span>
<span data-ttu-id="89e5f-124">Имя файла, содержащего одно определение роли JSON, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="89e5f-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="89e5f-125">Включайте только свойства, которые должны быть обновлены в JSON.</span><span class="sxs-lookup"><span data-stu-id="89e5f-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="89e5f-126">Требуется свойство ID.</span><span class="sxs-lookup"><span data-stu-id="89e5f-126">Id property is Required.</span></span>

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

### <span data-ttu-id="89e5f-127">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="89e5f-127">-Role</span></span>
<span data-ttu-id="89e5f-128">Обновляемый объект определения роли</span><span class="sxs-lookup"><span data-stu-id="89e5f-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="89e5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e5f-129">CommonParameters</span></span>
<span data-ttu-id="89e5f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89e5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e5f-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e5f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e5f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89e5f-132">INPUTS</span></span>

### <span data-ttu-id="89e5f-133">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="89e5f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e5f-134">OUTPUTS</span></span>

### <span data-ttu-id="89e5f-135">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="89e5f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="89e5f-136">NOTES</span></span>
<span data-ttu-id="89e5f-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="89e5f-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="89e5f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89e5f-138">RELATED LINKS</span></span>

[<span data-ttu-id="89e5f-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="89e5f-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="89e5f-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="89e5f-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="89e5f-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="89e5f-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

