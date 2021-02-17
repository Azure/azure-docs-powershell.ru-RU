---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212737"
---
# <span data-ttu-id="49741-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="49741-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="49741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49741-102">SYNOPSIS</span></span>
<span data-ttu-id="49741-103">Обновив ресурс общей частной ссылки для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="49741-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="49741-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49741-104">SYNTAX</span></span>

### <span data-ttu-id="49741-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49741-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49741-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49741-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49741-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49741-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49741-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49741-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49741-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49741-109">DESCRIPTION</span></span>
<span data-ttu-id="49741-110">Этот **ресурс Set-AzSearchSharedPrivateLinkResource** обновляет ресурс общей частной ссылки для службы Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="49741-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="49741-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49741-111">EXAMPLES</span></span>

### <span data-ttu-id="49741-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49741-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="49741-113">В этом примере обновляется сообщение запроса для ожидающих ожидания ресурсов общей личной ссылки для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="49741-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="49741-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49741-114">PARAMETERS</span></span>

### <span data-ttu-id="49741-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49741-115">-AsJob</span></span>
<span data-ttu-id="49741-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="49741-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49741-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49741-117">-DefaultProfile</span></span>
<span data-ttu-id="49741-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49741-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49741-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49741-119">-InputObject</span></span>
<span data-ttu-id="49741-120">Объект ввода ресурсов общей частной ссылки</span><span class="sxs-lookup"><span data-stu-id="49741-120">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49741-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49741-121">-Name</span></span>
<span data-ttu-id="49741-122">Ресурс личной ссылки "Общий поиск" в Azure</span><span class="sxs-lookup"><span data-stu-id="49741-122">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49741-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49741-123">-ParentObject</span></span>
<span data-ttu-id="49741-124">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="49741-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49741-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="49741-125">-RequestMessage</span></span>
<span data-ttu-id="49741-126">Сообщение с запросом ресурсов на доступную личную ссылку</span><span class="sxs-lookup"><span data-stu-id="49741-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49741-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49741-127">-ResourceGroupName</span></span>
<span data-ttu-id="49741-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49741-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49741-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49741-129">-ResourceId</span></span>
<span data-ttu-id="49741-130">ИД ресурса общей личной ссылки</span><span class="sxs-lookup"><span data-stu-id="49741-130">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49741-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49741-131">-ServiceName</span></span>
<span data-ttu-id="49741-132">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="49741-132">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49741-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49741-133">-Confirm</span></span>
<span data-ttu-id="49741-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49741-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49741-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49741-135">-WhatIf</span></span>
<span data-ttu-id="49741-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49741-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49741-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49741-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49741-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49741-138">CommonParameters</span></span>
<span data-ttu-id="49741-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49741-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49741-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49741-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49741-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49741-141">INPUTS</span></span>

### <span data-ttu-id="49741-142">Нет</span><span class="sxs-lookup"><span data-stu-id="49741-142">None</span></span>

## <span data-ttu-id="49741-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49741-143">OUTPUTS</span></span>

### <span data-ttu-id="49741-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="49741-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="49741-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49741-145">NOTES</span></span>

## <span data-ttu-id="49741-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49741-146">RELATED LINKS</span></span>

[<span data-ttu-id="49741-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="49741-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="49741-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="49741-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="49741-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="49741-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)