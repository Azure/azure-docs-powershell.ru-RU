---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405788"
---
# <span data-ttu-id="28a3a-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="28a3a-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="28a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="28a3a-103">Получите ключи {"ConnectionKeys", "PrimaryReadOnly" или "Keys"} для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="28a3a-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="28a3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28a3a-104">SYNTAX</span></span>

### <span data-ttu-id="28a3a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28a3a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28a3a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a3a-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28a3a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28a3a-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a3a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a3a-108">DESCRIPTION</span></span>
<span data-ttu-id="28a3a-109">Получить список ключей подключения.</span><span class="sxs-lookup"><span data-stu-id="28a3a-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="28a3a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28a3a-110">EXAMPLES</span></span>

### <span data-ttu-id="28a3a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28a3a-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="28a3a-112">В этой области перечислены ключи для учетной записи ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="28a3a-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="28a3a-113">Тип ключа может быть значением из : ConnectionStrings, Keys и ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="28a3a-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="28a3a-114">Значение по умолчанию — "Ключи".</span><span class="sxs-lookup"><span data-stu-id="28a3a-114">Default is Keys.</span></span>

## <span data-ttu-id="28a3a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a3a-115">PARAMETERS</span></span>

### <span data-ttu-id="28a3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a3a-116">-DefaultProfile</span></span>
<span data-ttu-id="28a3a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28a3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a3a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a3a-118">-InputObject</span></span>
<span data-ttu-id="28a3a-119">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="28a3a-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="28a3a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="28a3a-120">-Name</span></span>
<span data-ttu-id="28a3a-121">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="28a3a-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="28a3a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a3a-122">-ResourceGroupName</span></span>
<span data-ttu-id="28a3a-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28a3a-123">Name of resource group.</span></span>

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

### <span data-ttu-id="28a3a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a3a-124">-ResourceId</span></span>
<span data-ttu-id="28a3a-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="28a3a-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="28a3a-126">-Type</span><span class="sxs-lookup"><span data-stu-id="28a3a-126">-Type</span></span>
<span data-ttu-id="28a3a-127">Значение из: {ConnectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="28a3a-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="28a3a-128">Значение по умолчанию — "Ключи".</span><span class="sxs-lookup"><span data-stu-id="28a3a-128">Default is Keys.</span></span>

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

### <span data-ttu-id="28a3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a3a-129">CommonParameters</span></span>
<span data-ttu-id="28a3a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a3a-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a3a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a3a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28a3a-132">INPUTS</span></span>

### <span data-ttu-id="28a3a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="28a3a-133">None</span></span>

## <span data-ttu-id="28a3a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28a3a-134">OUTPUTS</span></span>

### <span data-ttu-id="28a3a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="28a3a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="28a3a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="28a3a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="28a3a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="28a3a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="28a3a-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28a3a-138">NOTES</span></span>

## <span data-ttu-id="28a3a-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28a3a-139">RELATED LINKS</span></span>
