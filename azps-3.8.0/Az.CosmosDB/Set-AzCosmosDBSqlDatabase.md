---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065024"
---
# <span data-ttu-id="07d44-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07d44-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="07d44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07d44-102">SYNOPSIS</span></span>
<span data-ttu-id="07d44-103">Создает новую или обновляет существующую базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="07d44-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="07d44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07d44-104">SYNTAX</span></span>

### <span data-ttu-id="07d44-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07d44-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07d44-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07d44-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07d44-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07d44-107">DESCRIPTION</span></span>
<span data-ttu-id="07d44-108">Командлет **Set-AzCosmosDBSqlDatabase** создает новую или обновляет существующую базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="07d44-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="07d44-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07d44-109">EXAMPLES</span></span>

### <span data-ttu-id="07d44-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07d44-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="07d44-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07d44-111">PARAMETERS</span></span>

### <span data-ttu-id="07d44-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="07d44-112">-AccountName</span></span>
<span data-ttu-id="07d44-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="07d44-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="07d44-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07d44-114">-Confirm</span></span>
<span data-ttu-id="07d44-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07d44-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d44-116">-DefaultProfile</span></span>
<span data-ttu-id="07d44-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07d44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07d44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d44-118">-InputObject</span></span>
<span data-ttu-id="07d44-119">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="07d44-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07d44-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07d44-120">-Name</span></span>
<span data-ttu-id="07d44-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="07d44-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d44-122">-ResourceGroupName</span></span>
<span data-ttu-id="07d44-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07d44-123">Name of resource group.</span></span>

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

### <span data-ttu-id="07d44-124">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="07d44-124">-Throughput</span></span>
<span data-ttu-id="07d44-125">Пропускная способность базы данных SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="07d44-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="07d44-126">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="07d44-126">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d44-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d44-127">-WhatIf</span></span>
<span data-ttu-id="07d44-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07d44-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d44-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07d44-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d44-130">CommonParameters</span></span>
<span data-ttu-id="07d44-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07d44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d44-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07d44-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d44-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07d44-133">INPUTS</span></span>

### <span data-ttu-id="07d44-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="07d44-134">None</span></span>

## <span data-ttu-id="07d44-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07d44-135">OUTPUTS</span></span>

### <span data-ttu-id="07d44-136">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="07d44-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="07d44-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="07d44-137">NOTES</span></span>

## <span data-ttu-id="07d44-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07d44-138">RELATED LINKS</span></span>
