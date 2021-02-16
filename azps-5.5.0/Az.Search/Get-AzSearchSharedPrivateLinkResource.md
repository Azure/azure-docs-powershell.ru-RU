---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226777"
---
# <span data-ttu-id="c2eed-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c2eed-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="c2eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2eed-102">SYNOPSIS</span></span>
<span data-ttu-id="c2eed-103">Получает общие ресурсы по закрытым ссылкам службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c2eed-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c2eed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2eed-104">SYNTAX</span></span>

### <span data-ttu-id="c2eed-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2eed-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eed-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2eed-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2eed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2eed-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2eed-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2eed-108">DESCRIPTION</span></span>
<span data-ttu-id="c2eed-109">Для получения общих ресурсов по личным ссылкам службы интеллектуального поиска Azure возвращается **cmdlet Get-AzSearchSharedPrivateLinkResource.**</span><span class="sxs-lookup"><span data-stu-id="c2eed-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c2eed-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2eed-110">EXAMPLES</span></span>

### <span data-ttu-id="c2eed-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2eed-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="c2eed-112">В этом примере перечислены все общие ресурсы по закрытым ссылкам службы Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c2eed-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="c2eed-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2eed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="c2eed-114">В этом примере перечислены определенные ресурсы общей частной ссылки по имени службы Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c2eed-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c2eed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2eed-115">PARAMETERS</span></span>

### <span data-ttu-id="c2eed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2eed-116">-DefaultProfile</span></span>
<span data-ttu-id="c2eed-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2eed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2eed-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2eed-118">-Name</span></span>
<span data-ttu-id="c2eed-119">Ресурс личной ссылки "Общий поиск" в Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="c2eed-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2eed-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2eed-120">-ParentObject</span></span>
<span data-ttu-id="c2eed-121">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="c2eed-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2eed-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2eed-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2eed-123">Resource Group name.</span></span>

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

### <span data-ttu-id="c2eed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2eed-124">-ResourceId</span></span>
<span data-ttu-id="c2eed-125">ИД ресурса общей личной ссылки</span><span class="sxs-lookup"><span data-stu-id="c2eed-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2eed-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c2eed-126">-ServiceName</span></span>
<span data-ttu-id="c2eed-127">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c2eed-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="c2eed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2eed-128">-Confirm</span></span>
<span data-ttu-id="c2eed-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c2eed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2eed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2eed-130">-WhatIf</span></span>
<span data-ttu-id="c2eed-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2eed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2eed-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2eed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2eed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2eed-133">CommonParameters</span></span>
<span data-ttu-id="c2eed-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2eed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2eed-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2eed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2eed-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2eed-136">INPUTS</span></span>

### <span data-ttu-id="c2eed-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c2eed-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c2eed-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c2eed-138">System.String</span></span>

## <span data-ttu-id="c2eed-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2eed-139">OUTPUTS</span></span>

### <span data-ttu-id="c2eed-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="c2eed-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="c2eed-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2eed-141">NOTES</span></span>

## <span data-ttu-id="c2eed-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2eed-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2eed-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="c2eed-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="c2eed-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="c2eed-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="c2eed-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="c2eed-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
