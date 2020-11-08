---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244615"
---
# <span data-ttu-id="ebeb3-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ebeb3-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ebeb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="ebeb3-103">Удаляет CosmosDB контейнер SQL.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ebeb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebeb3-104">SYNTAX</span></span>

### <span data-ttu-id="ebeb3-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebeb3-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebeb3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebeb3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebeb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebeb3-107">DESCRIPTION</span></span>
<span data-ttu-id="ebeb3-108">Командлет **Remove-AzCosmosDBSqlContainer** удаляет контейнер SQL CosmosDB, соответствующий данному ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ebeb3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebeb3-109">EXAMPLES</span></span>

### <span data-ttu-id="ebeb3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebeb3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="ebeb3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebeb3-111">PARAMETERS</span></span>

### <span data-ttu-id="ebeb3-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ebeb3-112">-AccountName</span></span>
<span data-ttu-id="ebeb3-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ebeb3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebeb3-114">-Confirm</span></span>
<span data-ttu-id="ebeb3-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebeb3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebeb3-116">-DatabaseName</span></span>
<span data-ttu-id="ebeb3-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-117">Database name.</span></span>

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

### <span data-ttu-id="ebeb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebeb3-118">-DefaultProfile</span></span>
<span data-ttu-id="ebeb3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebeb3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebeb3-120">-InputObject</span></span>
<span data-ttu-id="ebeb3-121">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-121">Sql Container object.</span></span>

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

### <span data-ttu-id="ebeb3-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebeb3-122">-Name</span></span>
<span data-ttu-id="ebeb3-123">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-123">Container name.</span></span>

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

### <span data-ttu-id="ebeb3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebeb3-124">-PassThru</span></span>
<span data-ttu-id="ebeb3-125">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ebeb3-126">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ebeb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebeb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebeb3-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ebeb3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebeb3-129">-WhatIf</span></span>
<span data-ttu-id="ebeb3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebeb3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebeb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebeb3-132">CommonParameters</span></span>
<span data-ttu-id="ebeb3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebeb3-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebeb3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebeb3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebeb3-135">INPUTS</span></span>

### <span data-ttu-id="ebeb3-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="ebeb3-136">None</span></span>

## <span data-ttu-id="ebeb3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebeb3-137">OUTPUTS</span></span>

### <span data-ttu-id="ebeb3-138">System. void</span><span class="sxs-lookup"><span data-stu-id="ebeb3-138">System.Void</span></span>

### <span data-ttu-id="ebeb3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebeb3-139">System.Boolean</span></span>

## <span data-ttu-id="ebeb3-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebeb3-140">NOTES</span></span>

## <span data-ttu-id="ebeb3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebeb3-141">RELATED LINKS</span></span>
