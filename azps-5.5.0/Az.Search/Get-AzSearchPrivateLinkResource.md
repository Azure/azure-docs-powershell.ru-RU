---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: 24941a301d0ffcc4e7219dc923fefcf1e007de99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210409"
---
# <span data-ttu-id="caca0-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="caca0-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="caca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caca0-102">SYNOPSIS</span></span>
<span data-ttu-id="caca0-103">Возвращает сведения о ресурсах личной ссылки для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="caca0-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="caca0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="caca0-104">SYNTAX</span></span>

### <span data-ttu-id="caca0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="caca0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caca0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caca0-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caca0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="caca0-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caca0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caca0-108">DESCRIPTION</span></span>
<span data-ttu-id="caca0-109">Cmdlet **Get-AzSearchPrivateLinkResource** получает сведения о ресурсах личной ссылки для службы Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="caca0-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="caca0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="caca0-110">EXAMPLES</span></span>

### <span data-ttu-id="caca0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="caca0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="caca0-112">В этом примере показано, как получить сведения о ресурсах закрытой ссылки (в форме JSON для удобства) для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="caca0-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="caca0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caca0-113">PARAMETERS</span></span>

### <span data-ttu-id="caca0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caca0-114">-DefaultProfile</span></span>
<span data-ttu-id="caca0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caca0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caca0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caca0-116">-InputObject</span></span>
<span data-ttu-id="caca0-117">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="caca0-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caca0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="caca0-118">-Name</span></span>
<span data-ttu-id="caca0-119">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="caca0-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="caca0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caca0-120">-ResourceGroupName</span></span>
<span data-ttu-id="caca0-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caca0-121">Resource Group name.</span></span>

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

### <span data-ttu-id="caca0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caca0-122">-ResourceId</span></span>
<span data-ttu-id="caca0-123">ИД ресурса службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="caca0-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="caca0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caca0-124">-Confirm</span></span>
<span data-ttu-id="caca0-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="caca0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caca0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caca0-126">-WhatIf</span></span>
<span data-ttu-id="caca0-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caca0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caca0-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="caca0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caca0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caca0-129">CommonParameters</span></span>
<span data-ttu-id="caca0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caca0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caca0-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="caca0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caca0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caca0-132">INPUTS</span></span>

### <span data-ttu-id="caca0-133">Нет</span><span class="sxs-lookup"><span data-stu-id="caca0-133">None</span></span>

## <span data-ttu-id="caca0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="caca0-134">OUTPUTS</span></span>

### <span data-ttu-id="caca0-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="caca0-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="caca0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="caca0-136">NOTES</span></span>

## <span data-ttu-id="caca0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caca0-137">RELATED LINKS</span></span>

[<span data-ttu-id="caca0-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="caca0-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="caca0-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="caca0-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="caca0-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="caca0-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="caca0-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="caca0-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)