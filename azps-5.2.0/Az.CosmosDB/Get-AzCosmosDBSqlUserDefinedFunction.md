---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401468"
---
# <span data-ttu-id="55a69-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="55a69-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="55a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a69-102">SYNOPSIS</span></span>
<span data-ttu-id="55a69-103">Возвращает функцию Sql Sql SQL.</span><span class="sxs-lookup"><span data-stu-id="55a69-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="55a69-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55a69-104">SYNTAX</span></span>

### <span data-ttu-id="55a69-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a69-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a69-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a69-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55a69-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a69-107">DESCRIPTION</span></span>
<span data-ttu-id="55a69-108">Cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** возвращает список всех существующих буклетов Sql UserDefinedFunctions Для данного названия ResourceGroupName, AccountName, DatabaseName и ContainerName, которая получает одну надстройку "КодПродажа UserDefinedFunction" для данного имени resourceGroupName, AccountName, DatabaseName, ContainerName и UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="55a69-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="55a69-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55a69-109">EXAMPLES</span></span>

### <span data-ttu-id="55a69-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55a69-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="55a69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55a69-111">PARAMETERS</span></span>

### <span data-ttu-id="55a69-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55a69-112">-AccountName</span></span>
<span data-ttu-id="55a69-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="55a69-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55a69-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="55a69-114">-ContainerName</span></span>
<span data-ttu-id="55a69-115">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="55a69-115">Container name.</span></span>

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

### <span data-ttu-id="55a69-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55a69-116">-DatabaseName</span></span>
<span data-ttu-id="55a69-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="55a69-117">Database name.</span></span>

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

### <span data-ttu-id="55a69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a69-118">-DefaultProfile</span></span>
<span data-ttu-id="55a69-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55a69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a69-120">-Name</span><span class="sxs-lookup"><span data-stu-id="55a69-120">-Name</span></span>
<span data-ttu-id="55a69-121">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="55a69-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="55a69-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55a69-122">-ParentObject</span></span>
<span data-ttu-id="55a69-123">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="55a69-123">Sql Container object.</span></span>

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

### <span data-ttu-id="55a69-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a69-124">-ResourceGroupName</span></span>
<span data-ttu-id="55a69-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55a69-125">Name of resource group.</span></span>

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

### <span data-ttu-id="55a69-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a69-126">CommonParameters</span></span>
<span data-ttu-id="55a69-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a69-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a69-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55a69-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a69-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55a69-129">INPUTS</span></span>

### <span data-ttu-id="55a69-130">Нет</span><span class="sxs-lookup"><span data-stu-id="55a69-130">None</span></span>

## <span data-ttu-id="55a69-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55a69-131">OUTPUTS</span></span>

### <span data-ttu-id="55a69-132">Microsoft.Azure.Commands.GetsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="55a69-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="55a69-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55a69-133">NOTES</span></span>

## <span data-ttu-id="55a69-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55a69-134">RELATED LINKS</span></span>
