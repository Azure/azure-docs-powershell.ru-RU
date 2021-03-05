---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 6df8d425967133e50dc45e44b6d567aca58465a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004387"
---
# <span data-ttu-id="59b5a-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="59b5a-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="59b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="59b5a-103">Получить учетную запись Facebook.</span><span class="sxs-lookup"><span data-stu-id="59b5a-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="59b5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59b5a-104">SYNTAX</span></span>

### <span data-ttu-id="59b5a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59b5a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59b5a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b5a-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b5a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="59b5a-108">С его учетной записью **Get-AzCosmosDBAccount** можно получить список всех существующих учетных записей "Перезапись" для заданной базы ресурсов ResourceGroupName и AccountName.</span><span class="sxs-lookup"><span data-stu-id="59b5a-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="59b5a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="59b5a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59b5a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="59b5a-111">Получить учетную запись базы данных "Базе данных " с именем databaseAccountName в ResourceGroup ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="59b5a-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="59b5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="59b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="59b5a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59b5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b5a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="59b5a-115">-Name</span></span>
<span data-ttu-id="59b5a-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="59b5a-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="59b5a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59b5a-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b5a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b5a-119">-ResourceId</span></span>
<span data-ttu-id="59b5a-120">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="59b5a-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b5a-121">CommonParameters</span></span>
<span data-ttu-id="59b5a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b5a-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59b5a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b5a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59b5a-124">INPUTS</span></span>

### <span data-ttu-id="59b5a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="59b5a-125">None</span></span>

## <span data-ttu-id="59b5a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59b5a-126">OUTPUTS</span></span>

### <span data-ttu-id="59b5a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="59b5a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="59b5a-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59b5a-128">NOTES</span></span>

## <span data-ttu-id="59b5a-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59b5a-129">RELATED LINKS</span></span>
