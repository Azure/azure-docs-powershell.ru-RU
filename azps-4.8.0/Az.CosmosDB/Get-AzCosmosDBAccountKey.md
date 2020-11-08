---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242878"
---
# <span data-ttu-id="6f057-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f057-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="6f057-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f057-102">SYNOPSIS</span></span>
<span data-ttu-id="6f057-103">Получение ключей {"ConnectionKeys", "PrimaryReadOnly" или "Keys"} для указанной учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6f057-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="6f057-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f057-104">SYNTAX</span></span>

### <span data-ttu-id="6f057-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f057-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f057-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f057-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f057-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f057-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f057-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f057-108">DESCRIPTION</span></span>
<span data-ttu-id="6f057-109">Получение списка ключей подключения.</span><span class="sxs-lookup"><span data-stu-id="6f057-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="6f057-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f057-110">EXAMPLES</span></span>

### <span data-ttu-id="6f057-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f057-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="6f057-112">Список клавиш для учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6f057-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="6f057-113">Тип ключа может принимать значения от: ConnectionString, Keys и ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="6f057-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="6f057-114">По умолчанию — ключи.</span><span class="sxs-lookup"><span data-stu-id="6f057-114">Default is Keys.</span></span>

## <span data-ttu-id="6f057-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f057-115">PARAMETERS</span></span>

### <span data-ttu-id="6f057-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f057-116">-DefaultProfile</span></span>
<span data-ttu-id="6f057-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f057-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f057-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f057-118">-InputObject</span></span>
<span data-ttu-id="6f057-119">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6f057-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6f057-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f057-120">-Name</span></span>
<span data-ttu-id="6f057-121">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6f057-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6f057-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f057-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f057-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f057-123">Name of resource group.</span></span>

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

### <span data-ttu-id="6f057-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f057-124">-ResourceId</span></span>
<span data-ttu-id="6f057-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="6f057-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="6f057-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="6f057-126">-Type</span></span>
<span data-ttu-id="6f057-127">Значение от: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="6f057-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="6f057-128">По умолчанию — ключи.</span><span class="sxs-lookup"><span data-stu-id="6f057-128">Default is Keys.</span></span>

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

### <span data-ttu-id="6f057-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f057-129">CommonParameters</span></span>
<span data-ttu-id="6f057-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f057-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f057-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f057-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f057-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f057-132">INPUTS</span></span>

### <span data-ttu-id="6f057-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f057-133">None</span></span>

## <span data-ttu-id="6f057-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f057-134">OUTPUTS</span></span>

### <span data-ttu-id="6f057-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="6f057-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="6f057-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6f057-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="6f057-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="6f057-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="6f057-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f057-138">NOTES</span></span>

## <span data-ttu-id="6f057-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f057-139">RELATED LINKS</span></span>