---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 985c501f93f2d37900b8ad62acc16f8508e51023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966680"
---
# <span data-ttu-id="dbbb7-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="dbbb7-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="dbbb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbb7-103">Удаляет Sql StoredProcedure вБDB.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dbbb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbbb7-104">SYNTAX</span></span>

### <span data-ttu-id="dbbb7-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbb7-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbbb7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbbb7-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbbb7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbbb7-107">DESCRIPTION</span></span>
<span data-ttu-id="dbbb7-108">Для удаления из данных ResourceGroupName, AccountName и DatabaseName с его учетной записью удаляется **cmdDB-AzCosmosDBSqlStoredProcedure.**</span><span class="sxs-lookup"><span data-stu-id="dbbb7-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="dbbb7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbbb7-109">EXAMPLES</span></span>

### <span data-ttu-id="dbbb7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbbb7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="dbbb7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbbb7-111">PARAMETERS</span></span>

### <span data-ttu-id="dbbb7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbbb7-112">-AccountName</span></span>
<span data-ttu-id="dbbb7-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="dbbb7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dbbb7-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbbb7-114">-Confirm</span></span>
<span data-ttu-id="dbbb7-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbbb7-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dbbb7-116">-ContainerName</span></span>
<span data-ttu-id="dbbb7-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-117">Container name.</span></span>

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

### <span data-ttu-id="dbbb7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dbbb7-118">-DatabaseName</span></span>
<span data-ttu-id="dbbb7-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-119">Database name.</span></span>

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

### <span data-ttu-id="dbbb7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbb7-120">-DefaultProfile</span></span>
<span data-ttu-id="dbbb7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbbb7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbbb7-122">-InputObject</span></span>
<span data-ttu-id="dbbb7-123">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbbb7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dbbb7-124">-Name</span></span>
<span data-ttu-id="dbbb7-125">Имя хранимой prcodecure.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="dbbb7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbbb7-126">-PassThru</span></span>
<span data-ttu-id="dbbb7-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dbbb7-128">Результат является истинным, если операция прошла успешно и если она не произошла, вы ошибку.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dbbb7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbbb7-129">-ResourceGroupName</span></span>
<span data-ttu-id="dbbb7-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dbbb7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbbb7-131">-WhatIf</span></span>
<span data-ttu-id="dbbb7-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbbb7-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbbb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbb7-134">CommonParameters</span></span>
<span data-ttu-id="dbbb7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbb7-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbbb7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbb7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbbb7-137">INPUTS</span></span>

### <span data-ttu-id="dbbb7-138">Нет</span><span class="sxs-lookup"><span data-stu-id="dbbb7-138">None</span></span>

## <span data-ttu-id="dbbb7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbbb7-139">OUTPUTS</span></span>

### <span data-ttu-id="dbbb7-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="dbbb7-140">System.Void</span></span>

### <span data-ttu-id="dbbb7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbbb7-141">System.Boolean</span></span>

## <span data-ttu-id="dbbb7-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbbb7-142">NOTES</span></span>

## <span data-ttu-id="dbbb7-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbbb7-143">RELATED LINKS</span></span>
