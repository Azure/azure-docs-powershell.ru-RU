---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405495"
---
# <span data-ttu-id="ba859-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ba859-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ba859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba859-102">SYNOPSIS</span></span>
<span data-ttu-id="ba859-103">Удаляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="ba859-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ba859-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba859-104">SYNTAX</span></span>

### <span data-ttu-id="ba859-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba859-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba859-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba859-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba859-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba859-107">DESCRIPTION</span></span>
<span data-ttu-id="ba859-108">Для удаления контейнера Sql **AzCosmosDBSqlContainer** удаляется контейнер Sql, соответствующий заданным названиям группы ресурсов, AccountName, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="ba859-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ba859-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba859-109">EXAMPLES</span></span>

### <span data-ttu-id="ba859-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba859-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="ba859-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba859-111">PARAMETERS</span></span>

### <span data-ttu-id="ba859-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba859-112">-AccountName</span></span>
<span data-ttu-id="ba859-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="ba859-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba859-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba859-114">-Confirm</span></span>
<span data-ttu-id="ba859-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba859-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba859-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba859-116">-DatabaseName</span></span>
<span data-ttu-id="ba859-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ba859-117">Database name.</span></span>

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

### <span data-ttu-id="ba859-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba859-118">-DefaultProfile</span></span>
<span data-ttu-id="ba859-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba859-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba859-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba859-120">-InputObject</span></span>
<span data-ttu-id="ba859-121">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="ba859-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba859-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ba859-122">-Name</span></span>
<span data-ttu-id="ba859-123">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ba859-123">Container name.</span></span>

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

### <span data-ttu-id="ba859-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba859-124">-PassThru</span></span>
<span data-ttu-id="ba859-125">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="ba859-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ba859-126">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="ba859-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba859-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba859-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba859-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba859-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ba859-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba859-129">-WhatIf</span></span>
<span data-ttu-id="ba859-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba859-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba859-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba859-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba859-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba859-132">CommonParameters</span></span>
<span data-ttu-id="ba859-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba859-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba859-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba859-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba859-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba859-135">INPUTS</span></span>

### <span data-ttu-id="ba859-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ba859-136">None</span></span>

## <span data-ttu-id="ba859-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba859-137">OUTPUTS</span></span>

### <span data-ttu-id="ba859-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba859-138">System.Void</span></span>

### <span data-ttu-id="ba859-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba859-139">System.Boolean</span></span>

## <span data-ttu-id="ba859-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba859-140">NOTES</span></span>

## <span data-ttu-id="ba859-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba859-141">RELATED LINKS</span></span>
