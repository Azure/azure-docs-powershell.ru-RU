---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238473"
---
# <span data-ttu-id="ad7e3-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad7e3-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ad7e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7e3-103">Удаляет базу данных SQLDb.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ad7e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad7e3-104">SYNTAX</span></span>

### <span data-ttu-id="ad7e3-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad7e3-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad7e3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad7e3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad7e3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad7e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ad7e3-108">При этом удаляется база данных Sql " **ВадимБазыБ.AZCosmosDBSqlDatabase,** соответствующая заданной базе данных ResourceGroupName, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ad7e3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad7e3-109">EXAMPLES</span></span>

### <span data-ttu-id="ad7e3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad7e3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="ad7e3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad7e3-111">PARAMETERS</span></span>

### <span data-ttu-id="ad7e3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad7e3-112">-AccountName</span></span>
<span data-ttu-id="ad7e3-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="ad7e3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad7e3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad7e3-114">-Confirm</span></span>
<span data-ttu-id="ad7e3-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7e3-116">-DefaultProfile</span></span>
<span data-ttu-id="ad7e3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad7e3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad7e3-118">-InputObject</span></span>
<span data-ttu-id="ad7e3-119">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7e3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ad7e3-120">-Name</span></span>
<span data-ttu-id="ad7e3-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-121">Database name.</span></span>

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

### <span data-ttu-id="ad7e3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad7e3-122">-PassThru</span></span>
<span data-ttu-id="ad7e3-123">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ad7e3-124">Результат является истинным, если операция прошла успешно и если она не произошла, вы ошибку.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ad7e3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7e3-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad7e3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-126">Name of resource group.</span></span>

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

### <span data-ttu-id="ad7e3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7e3-127">-WhatIf</span></span>
<span data-ttu-id="ad7e3-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad7e3-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7e3-130">CommonParameters</span></span>
<span data-ttu-id="ad7e3-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7e3-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad7e3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7e3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad7e3-133">INPUTS</span></span>

### <span data-ttu-id="ad7e3-134">Нет</span><span class="sxs-lookup"><span data-stu-id="ad7e3-134">None</span></span>

## <span data-ttu-id="ad7e3-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad7e3-135">OUTPUTS</span></span>

### <span data-ttu-id="ad7e3-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="ad7e3-136">System.Void</span></span>

### <span data-ttu-id="ad7e3-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad7e3-137">System.Boolean</span></span>

## <span data-ttu-id="ad7e3-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad7e3-138">NOTES</span></span>

## <span data-ttu-id="ad7e3-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad7e3-139">RELATED LINKS</span></span>
