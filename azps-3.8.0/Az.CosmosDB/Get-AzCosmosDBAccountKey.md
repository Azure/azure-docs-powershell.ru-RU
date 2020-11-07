---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: 6c0fb28010aff759c406ddd04db281dc05ce1f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912049"
---
# <span data-ttu-id="59fb7-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="59fb7-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="59fb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="59fb7-103">Получение ключей {"ConnectionKeys", "PrimaryReadOnly" или "Keys"} для указанной учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="59fb7-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="59fb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59fb7-104">SYNTAX</span></span>

### <span data-ttu-id="59fb7-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59fb7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59fb7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fb7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59fb7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fb7-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fb7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="59fb7-109">Получение списка ключей подключения.</span><span class="sxs-lookup"><span data-stu-id="59fb7-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="59fb7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="59fb7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59fb7-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="59fb7-112">Список клавиш для учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="59fb7-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="59fb7-113">Тип ключа может принимать значения от: ConnectionString, Keys и ReadOnlyKeys.</span><span class="sxs-lookup"><span data-stu-id="59fb7-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="59fb7-114">По умолчанию — ключи.</span><span class="sxs-lookup"><span data-stu-id="59fb7-114">Default is Keys.</span></span>

## <span data-ttu-id="59fb7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59fb7-115">PARAMETERS</span></span>

### <span data-ttu-id="59fb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fb7-116">-DefaultProfile</span></span>
<span data-ttu-id="59fb7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59fb7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59fb7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59fb7-118">-InputObject</span></span>
<span data-ttu-id="59fb7-119">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="59fb7-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fb7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59fb7-120">-Name</span></span>
<span data-ttu-id="59fb7-121">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="59fb7-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59fb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="59fb7-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59fb7-123">Name of resource group.</span></span>

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

### <span data-ttu-id="59fb7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59fb7-124">-ResourceId</span></span>
<span data-ttu-id="59fb7-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="59fb7-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="59fb7-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="59fb7-126">-Type</span></span>
<span data-ttu-id="59fb7-127">Значение от: {connectionStrings, Keys, ReadOnlyKeys}.</span><span class="sxs-lookup"><span data-stu-id="59fb7-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="59fb7-128">По умолчанию — ключи.</span><span class="sxs-lookup"><span data-stu-id="59fb7-128">Default is Keys.</span></span>

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

### <span data-ttu-id="59fb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fb7-129">CommonParameters</span></span>
<span data-ttu-id="59fb7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59fb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fb7-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59fb7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fb7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59fb7-132">INPUTS</span></span>

### <span data-ttu-id="59fb7-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="59fb7-133">None</span></span>

## <span data-ttu-id="59fb7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59fb7-134">OUTPUTS</span></span>

### <span data-ttu-id="59fb7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="59fb7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="59fb7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="59fb7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="59fb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="59fb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="59fb7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="59fb7-138">NOTES</span></span>

## <span data-ttu-id="59fb7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59fb7-139">RELATED LINKS</span></span>
