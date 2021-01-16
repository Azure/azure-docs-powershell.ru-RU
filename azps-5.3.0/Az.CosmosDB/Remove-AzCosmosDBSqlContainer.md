---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508754"
---
# <span data-ttu-id="12339-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="12339-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="12339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12339-102">SYNOPSIS</span></span>
<span data-ttu-id="12339-103">Удаляет контейнер SQLDb.</span><span class="sxs-lookup"><span data-stu-id="12339-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="12339-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12339-104">SYNTAX</span></span>

### <span data-ttu-id="12339-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12339-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12339-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12339-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12339-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12339-107">DESCRIPTION</span></span>
<span data-ttu-id="12339-108">При **этом** удаляется контейнер Sql ,соответствующий заданным ресурсам ResourceGroupName, AccountName, DatabaseName и ContainerName, с его учетной записью.</span><span class="sxs-lookup"><span data-stu-id="12339-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="12339-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12339-109">EXAMPLES</span></span>

### <span data-ttu-id="12339-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12339-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="12339-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12339-111">PARAMETERS</span></span>

### <span data-ttu-id="12339-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12339-112">-AccountName</span></span>
<span data-ttu-id="12339-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="12339-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="12339-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12339-114">-Confirm</span></span>
<span data-ttu-id="12339-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12339-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12339-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12339-116">-DatabaseName</span></span>
<span data-ttu-id="12339-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="12339-117">Database name.</span></span>

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

### <span data-ttu-id="12339-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12339-118">-DefaultProfile</span></span>
<span data-ttu-id="12339-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12339-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12339-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12339-120">-InputObject</span></span>
<span data-ttu-id="12339-121">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="12339-121">Sql Container object.</span></span>

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

### <span data-ttu-id="12339-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12339-122">-Name</span></span>
<span data-ttu-id="12339-123">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="12339-123">Container name.</span></span>

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

### <span data-ttu-id="12339-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12339-124">-PassThru</span></span>
<span data-ttu-id="12339-125">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="12339-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="12339-126">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="12339-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="12339-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12339-127">-ResourceGroupName</span></span>
<span data-ttu-id="12339-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12339-128">Name of resource group.</span></span>

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

### <span data-ttu-id="12339-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12339-129">-WhatIf</span></span>
<span data-ttu-id="12339-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12339-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12339-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12339-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12339-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12339-132">CommonParameters</span></span>
<span data-ttu-id="12339-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12339-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12339-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12339-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12339-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12339-135">INPUTS</span></span>

### <span data-ttu-id="12339-136">Нет</span><span class="sxs-lookup"><span data-stu-id="12339-136">None</span></span>

## <span data-ttu-id="12339-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12339-137">OUTPUTS</span></span>

### <span data-ttu-id="12339-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="12339-138">System.Void</span></span>

### <span data-ttu-id="12339-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12339-139">System.Boolean</span></span>

## <span data-ttu-id="12339-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12339-140">NOTES</span></span>

## <span data-ttu-id="12339-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12339-141">RELATED LINKS</span></span>
