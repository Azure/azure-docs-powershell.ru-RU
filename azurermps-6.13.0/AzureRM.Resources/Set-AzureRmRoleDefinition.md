---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: f0c22f199d19e97f957bc86fbee8d649d30b622d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734295"
---
# <span data-ttu-id="98008-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="98008-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98008-102">SYNOPSIS</span></span>
<span data-ttu-id="98008-103">Изменяет настраиваемую роль в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="98008-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="98008-104">Укажите измененное определение роли либо в виде JSON-файла, либо в виде PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="98008-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="98008-105">Сначала используйте команду Get-AzureRmRoleDefinition, чтобы получить настраиваемую роль, которую вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="98008-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="98008-106">Затем измените свойства, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="98008-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="98008-107">Наконец, сохраните определение роли с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="98008-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98008-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98008-108">SYNTAX</span></span>

### <span data-ttu-id="98008-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="98008-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98008-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="98008-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98008-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98008-111">DESCRIPTION</span></span>
<span data-ttu-id="98008-112">Командлет Set-AzureRmRoleDefinition обновляет существующую настраиваемую роль в Azure Role-Based управления доступом.</span><span class="sxs-lookup"><span data-stu-id="98008-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="98008-113">Предоставьте обновленное определение роли в качестве входных данных для команды в виде JSON-файла или объекта PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="98008-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="98008-114">Определение роли для обновленной настраиваемой роли должно содержать идентификатор и все другие обязательные свойства роли, даже если они не были обновлены: DisplayName, описание, действия, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="98008-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="98008-115">Не все изменения, макрокоманды, NotDataActions являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="98008-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="98008-116">Ниже приведен пример обновленного определения роли JSON для Set-AzureRmRoleDefinition {"ИД": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "имя": "обновленная роль", "Описание": "может отслеживать все ресурсы, запускать и перезапускать виртуальные машины", "действия": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/перезапустить/действие", "Microsoft. ClassicCompute/virtualmachines/Start/Action", "незащищенные" \] : \[ "* /Write" \] , "Actions": " \[ Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/большие/двоичные \] объекты/BLOB/ \[ записи" \] , "NotDataActions": \[ "storageAccounts") \]</span><span class="sxs-lookup"><span data-stu-id="98008-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="98008-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98008-117">EXAMPLES</span></span>

### <span data-ttu-id="98008-118">Обновление с помощью PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="98008-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="98008-119">Создание с помощью JSON File</span><span class="sxs-lookup"><span data-stu-id="98008-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="98008-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98008-120">PARAMETERS</span></span>

### <span data-ttu-id="98008-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98008-121">-DefaultProfile</span></span>
<span data-ttu-id="98008-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98008-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98008-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="98008-123">-InputFile</span></span>
<span data-ttu-id="98008-124">Имя файла, содержащего одно определение роли JSON, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="98008-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="98008-125">Включайте только свойства, которые должны быть обновлены в JSON.</span><span class="sxs-lookup"><span data-stu-id="98008-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="98008-126">Требуется свойство ID.</span><span class="sxs-lookup"><span data-stu-id="98008-126">Id property is Required.</span></span>

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

### <span data-ttu-id="98008-127">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="98008-127">-Role</span></span>
<span data-ttu-id="98008-128">Обновляемый объект определения роли</span><span class="sxs-lookup"><span data-stu-id="98008-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="98008-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98008-129">CommonParameters</span></span>
<span data-ttu-id="98008-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98008-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98008-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98008-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98008-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98008-132">INPUTS</span></span>

### <span data-ttu-id="98008-133">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="98008-134">Параметры: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98008-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="98008-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98008-135">OUTPUTS</span></span>

### <span data-ttu-id="98008-136">Microsoft. Azure. Commands. Resources. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="98008-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="98008-137">NOTES</span></span>
<span data-ttu-id="98008-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="98008-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="98008-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98008-139">RELATED LINKS</span></span>

[<span data-ttu-id="98008-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="98008-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="98008-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="98008-142">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="98008-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="98008-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

