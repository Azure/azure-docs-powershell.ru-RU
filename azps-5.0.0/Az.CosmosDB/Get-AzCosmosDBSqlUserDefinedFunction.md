---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314975"
---
# <span data-ttu-id="40313-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="40313-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="40313-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40313-102">SYNOPSIS</span></span>
<span data-ttu-id="40313-103">Возвращает пользовательскую функцию SQL CosmosDB, определяемую пользователем.</span><span class="sxs-lookup"><span data-stu-id="40313-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="40313-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40313-104">SYNTAX</span></span>

### <span data-ttu-id="40313-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40313-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40313-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40313-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40313-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40313-107">DESCRIPTION</span></span>
<span data-ttu-id="40313-108">Командлет **Get-AzCosmosDBSqlUserDefinedFunction** получает список всех существующих CosmosDB SQL UserDefinedFunctions для указанных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName и возвращает один CosmosDB SQL UserDefinedFunction для данного ResourceGroupName, имя_учетной_записи, DatabaseName, ContainerName и UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="40313-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="40313-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40313-109">EXAMPLES</span></span>

### <span data-ttu-id="40313-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40313-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="40313-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40313-111">PARAMETERS</span></span>

### <span data-ttu-id="40313-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="40313-112">-AccountName</span></span>
<span data-ttu-id="40313-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="40313-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40313-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="40313-114">-ContainerName</span></span>
<span data-ttu-id="40313-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="40313-115">Container name.</span></span>

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

### <span data-ttu-id="40313-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40313-116">-DatabaseName</span></span>
<span data-ttu-id="40313-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="40313-117">Database name.</span></span>

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

### <span data-ttu-id="40313-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40313-118">-DefaultProfile</span></span>
<span data-ttu-id="40313-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40313-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40313-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40313-120">-Name</span></span>
<span data-ttu-id="40313-121">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="40313-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="40313-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40313-122">-ParentObject</span></span>
<span data-ttu-id="40313-123">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="40313-123">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40313-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40313-124">-ResourceGroupName</span></span>
<span data-ttu-id="40313-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40313-125">Name of resource group.</span></span>

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

### <span data-ttu-id="40313-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40313-126">CommonParameters</span></span>
<span data-ttu-id="40313-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40313-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40313-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40313-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40313-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40313-129">INPUTS</span></span>

### <span data-ttu-id="40313-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="40313-130">None</span></span>

## <span data-ttu-id="40313-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40313-131">OUTPUTS</span></span>

### <span data-ttu-id="40313-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="40313-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="40313-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="40313-133">NOTES</span></span>

## <span data-ttu-id="40313-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40313-134">RELATED LINKS</span></span>
