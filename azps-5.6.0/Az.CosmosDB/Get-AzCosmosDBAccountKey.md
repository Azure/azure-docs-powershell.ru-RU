---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: c143fed64e99dd9f564b4375c4ef20e5b5ad4354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983731"
---
# <span data-ttu-id="6cac3-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="6cac3-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="6cac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cac3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cac3-103">Получите ключи {"ConnectionKeys", "PrimaryReadOnly" или "Keys"} для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6cac3-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="6cac3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cac3-104">SYNTAX</span></span>

### <span data-ttu-id="6cac3-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6cac3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cac3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cac3-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cac3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cac3-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cac3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cac3-108">DESCRIPTION</span></span>
<span data-ttu-id="6cac3-109">Получить список ключей подключения.</span><span class="sxs-lookup"><span data-stu-id="6cac3-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="6cac3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cac3-110">EXAMPLES</span></span>

### <span data-ttu-id="6cac3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cac3-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="6cac3-112">В этой области перечислены ключи для учетной записи ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="6cac3-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="6cac3-113">Тип ключа может быть значением из : ConnectionStrings, Keys и ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="6cac3-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="6cac3-114">Значение по умолчанию — "Ключи".</span><span class="sxs-lookup"><span data-stu-id="6cac3-114">Default is Keys.</span></span>

## <span data-ttu-id="6cac3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cac3-115">PARAMETERS</span></span>

### <span data-ttu-id="6cac3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cac3-116">-DefaultProfile</span></span>
<span data-ttu-id="6cac3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cac3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cac3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cac3-118">-InputObject</span></span>
<span data-ttu-id="6cac3-119">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="6cac3-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cac3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6cac3-120">-Name</span></span>
<span data-ttu-id="6cac3-121">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="6cac3-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6cac3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cac3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cac3-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cac3-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6cac3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cac3-124">-ResourceId</span></span>
<span data-ttu-id="6cac3-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="6cac3-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="6cac3-126">-Type</span><span class="sxs-lookup"><span data-stu-id="6cac3-126">-Type</span></span>
<span data-ttu-id="6cac3-127">Значение из: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="6cac3-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="6cac3-128">Значение по умолчанию — "Ключи".</span><span class="sxs-lookup"><span data-stu-id="6cac3-128">Default is Keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cac3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cac3-129">CommonParameters</span></span>
<span data-ttu-id="6cac3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cac3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cac3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cac3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cac3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cac3-132">INPUTS</span></span>

### <span data-ttu-id="6cac3-133">Нет</span><span class="sxs-lookup"><span data-stu-id="6cac3-133">None</span></span>

## <span data-ttu-id="6cac3-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cac3-134">OUTPUTS</span></span>

### <span data-ttu-id="6cac3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="6cac3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="6cac3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6cac3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="6cac3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="6cac3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="6cac3-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cac3-138">NOTES</span></span>

## <span data-ttu-id="6cac3-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cac3-139">RELATED LINKS</span></span>
