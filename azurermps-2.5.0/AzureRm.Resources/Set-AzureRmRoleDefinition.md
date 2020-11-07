---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913967"
---
# <span data-ttu-id="d86c9-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="d86c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d86c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d86c9-103">Изменяет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="d86c9-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="d86c9-104">Укажите измененное определение роли либо в виде JSON-файла, либо в виде PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="d86c9-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="d86c9-105">Сначала используйте команду Get-AzureRmRoleDefinition, чтобы получить настраиваемую роль, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="d86c9-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="d86c9-106">Затем измените свойства, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="d86c9-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="d86c9-107">Наконец, сохраните определение роли с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="d86c9-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d86c9-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d86c9-108">SYNTAX</span></span>

### <span data-ttu-id="d86c9-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d86c9-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d86c9-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d86c9-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d86c9-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d86c9-111">DESCRIPTION</span></span>
<span data-ttu-id="d86c9-112">Командлет Set-AzureRmRoleDefinition обновляет существующую настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="d86c9-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="d86c9-113">Предоставьте обновленное определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="d86c9-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="d86c9-114">Определение роли для обновленной настраиваемой роли должно содержать идентификатор и все другие обязательные свойства роли, даже если они не были обновлены: DisplayName, описание, действия, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="d86c9-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="d86c9-115">Не все изменения, макрокоманды, NotDataActions являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="d86c9-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="d86c9-116">Ниже приведен пример обновленного определения роли JSON для Set-AzureRmRoleDefinition {"ИД": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "имя": "обновленная роль", "Описание": "может отслеживать все ресурсы, запускать и перезапускать виртуальные машины", "действия": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/перезапустить/действие", "Microsoft. ClassicCompute/virtualmachines/Start/Action", "незащищенные" \] : \[ "* /Write" \] , "Actions": " \[ Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/большие/двоичные \] объекты/BLOB/ \[ записи" \] , "NotDataActions": \[ "storageAccounts") \]</span><span class="sxs-lookup"><span data-stu-id="d86c9-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="d86c9-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d86c9-117">EXAMPLES</span></span>

### <span data-ttu-id="d86c9-118">Обновление с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="d86c9-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="d86c9-119">Создание с помощью JSON File</span><span class="sxs-lookup"><span data-stu-id="d86c9-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="d86c9-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d86c9-120">PARAMETERS</span></span>

### <span data-ttu-id="d86c9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86c9-121">-DefaultProfile</span></span>
<span data-ttu-id="d86c9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d86c9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d86c9-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d86c9-123">-InputFile</span></span>
<span data-ttu-id="d86c9-124">Имя файла, содержащего одно определение роли JSON, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="d86c9-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="d86c9-125">Включайте только свойства, которые должны быть обновлены в JSON.</span><span class="sxs-lookup"><span data-stu-id="d86c9-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="d86c9-126">Требуется свойство ID.</span><span class="sxs-lookup"><span data-stu-id="d86c9-126">Id property is Required.</span></span>

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

### <span data-ttu-id="d86c9-127">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="d86c9-127">-Role</span></span>
<span data-ttu-id="d86c9-128">Обновляемый объект определения роли</span><span class="sxs-lookup"><span data-stu-id="d86c9-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="d86c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86c9-129">CommonParameters</span></span>
<span data-ttu-id="d86c9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d86c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86c9-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86c9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86c9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d86c9-132">INPUTS</span></span>

### <span data-ttu-id="d86c9-133">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="d86c9-134">Параметры: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d86c9-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="d86c9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d86c9-135">OUTPUTS</span></span>

### <span data-ttu-id="d86c9-136">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="d86c9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d86c9-137">NOTES</span></span>
<span data-ttu-id="d86c9-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="d86c9-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d86c9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d86c9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d86c9-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d86c9-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="d86c9-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="d86c9-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="d86c9-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d86c9-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

