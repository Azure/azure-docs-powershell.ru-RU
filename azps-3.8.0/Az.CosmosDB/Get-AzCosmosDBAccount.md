---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912052"
---
# <span data-ttu-id="9675f-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9675f-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9675f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9675f-102">SYNOPSIS</span></span>
<span data-ttu-id="9675f-103">Получить учетную запись CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9675f-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="9675f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9675f-104">SYNTAX</span></span>

### <span data-ttu-id="9675f-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9675f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9675f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9675f-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9675f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9675f-107">DESCRIPTION</span></span>
<span data-ttu-id="9675f-108">Командлет **Get-AzCosmosDBAccount** получает список всех существующих учетных записей CosmosDB для данного ResourceGroupName и возвращает одну CosmosDBную учетную запись для указанных ResourceGroupName и AccountName.</span><span class="sxs-lookup"><span data-stu-id="9675f-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="9675f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9675f-109">EXAMPLES</span></span>

### <span data-ttu-id="9675f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9675f-110">Example 1</span></span>
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
```

<span data-ttu-id="9675f-111">Получение учетной записи базы данных CosmosDB с именем databaseAccountName в группе ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="9675f-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9675f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9675f-112">PARAMETERS</span></span>

### <span data-ttu-id="9675f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9675f-113">-DefaultProfile</span></span>
<span data-ttu-id="9675f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9675f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9675f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9675f-115">-Name</span></span>
<span data-ttu-id="9675f-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9675f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9675f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9675f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9675f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9675f-118">Name of resource group.</span></span>

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

### <span data-ttu-id="9675f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9675f-119">-ResourceId</span></span>
<span data-ttu-id="9675f-120">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="9675f-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="9675f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9675f-121">CommonParameters</span></span>
<span data-ttu-id="9675f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9675f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9675f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9675f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9675f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9675f-124">INPUTS</span></span>

### <span data-ttu-id="9675f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="9675f-125">None</span></span>

## <span data-ttu-id="9675f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9675f-126">OUTPUTS</span></span>

### <span data-ttu-id="9675f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9675f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9675f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="9675f-128">NOTES</span></span>

## <span data-ttu-id="9675f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9675f-129">RELATED LINKS</span></span>
