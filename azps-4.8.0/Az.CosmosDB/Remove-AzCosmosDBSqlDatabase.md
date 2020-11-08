---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244612"
---
# <span data-ttu-id="f148e-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f148e-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f148e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f148e-102">SYNOPSIS</span></span>
<span data-ttu-id="f148e-103">Удаляет базу данных SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f148e-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f148e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f148e-104">SYNTAX</span></span>

### <span data-ttu-id="f148e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f148e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f148e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f148e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f148e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f148e-107">DESCRIPTION</span></span>
<span data-ttu-id="f148e-108">Командлет **Remove-AzCosmosDBSqlDatabase** удаляет базу данных SQL CosmosDB, соответствующую данному ResourceGroupName, имя_учетной_записи и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f148e-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="f148e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f148e-109">EXAMPLES</span></span>

### <span data-ttu-id="f148e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f148e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="f148e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f148e-111">PARAMETERS</span></span>

### <span data-ttu-id="f148e-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f148e-112">-AccountName</span></span>
<span data-ttu-id="f148e-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f148e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f148e-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f148e-114">-Confirm</span></span>
<span data-ttu-id="f148e-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f148e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f148e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f148e-116">-DefaultProfile</span></span>
<span data-ttu-id="f148e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f148e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f148e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f148e-118">-InputObject</span></span>
<span data-ttu-id="f148e-119">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f148e-119">Sql Database object.</span></span>

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

### <span data-ttu-id="f148e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f148e-120">-Name</span></span>
<span data-ttu-id="f148e-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f148e-121">Database name.</span></span>

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

### <span data-ttu-id="f148e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f148e-122">-PassThru</span></span>
<span data-ttu-id="f148e-123">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="f148e-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f148e-124">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f148e-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f148e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f148e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f148e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f148e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f148e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f148e-127">-WhatIf</span></span>
<span data-ttu-id="f148e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f148e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f148e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f148e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f148e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f148e-130">CommonParameters</span></span>
<span data-ttu-id="f148e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f148e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f148e-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f148e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f148e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f148e-133">INPUTS</span></span>

### <span data-ttu-id="f148e-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="f148e-134">None</span></span>

## <span data-ttu-id="f148e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f148e-135">OUTPUTS</span></span>

### <span data-ttu-id="f148e-136">System. void</span><span class="sxs-lookup"><span data-stu-id="f148e-136">System.Void</span></span>

### <span data-ttu-id="f148e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f148e-137">System.Boolean</span></span>

## <span data-ttu-id="f148e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f148e-138">NOTES</span></span>

## <span data-ttu-id="f148e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f148e-139">RELATED LINKS</span></span>
