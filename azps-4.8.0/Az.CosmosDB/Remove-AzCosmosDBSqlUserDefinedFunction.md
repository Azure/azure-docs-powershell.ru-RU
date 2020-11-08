---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245078"
---
# <span data-ttu-id="2f7f3-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="2f7f3-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="2f7f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7f3-103">Удаляет CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2f7f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f7f3-104">SYNTAX</span></span>

### <span data-ttu-id="2f7f3-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f7f3-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f7f3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f7f3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f7f3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f7f3-107">DESCRIPTION</span></span>
<span data-ttu-id="2f7f3-108">Командлет **Remove-AzCosmosDBSqlUserDefinedFunction** удаляет CosmosDB SQL UserDefinedFunction, соответствующие данному ResourceGroupName, имя_учетной_записи и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="2f7f3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f7f3-109">EXAMPLES</span></span>

### <span data-ttu-id="2f7f3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f7f3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="2f7f3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f7f3-111">PARAMETERS</span></span>

### <span data-ttu-id="2f7f3-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="2f7f3-112">-AccountName</span></span>
<span data-ttu-id="2f7f3-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2f7f3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f7f3-114">-Confirm</span></span>
<span data-ttu-id="2f7f3-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f7f3-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2f7f3-116">-ContainerName</span></span>
<span data-ttu-id="2f7f3-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-117">Container name.</span></span>

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

### <span data-ttu-id="2f7f3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f7f3-118">-DatabaseName</span></span>
<span data-ttu-id="2f7f3-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-119">Database name.</span></span>

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

### <span data-ttu-id="2f7f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7f3-120">-DefaultProfile</span></span>
<span data-ttu-id="2f7f3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f7f3-122">-InputObject</span></span>
<span data-ttu-id="2f7f3-123">Объект пользовательской функции SQL</span><span class="sxs-lookup"><span data-stu-id="2f7f3-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7f3-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f7f3-124">-Name</span></span>
<span data-ttu-id="2f7f3-125">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="2f7f3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f7f3-126">-PassThru</span></span>
<span data-ttu-id="2f7f3-127">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2f7f3-128">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2f7f3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7f3-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f7f3-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="2f7f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f7f3-131">-WhatIf</span></span>
<span data-ttu-id="2f7f3-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f7f3-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f7f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7f3-134">CommonParameters</span></span>
<span data-ttu-id="2f7f3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f7f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7f3-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f7f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7f3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f7f3-137">INPUTS</span></span>

### <span data-ttu-id="2f7f3-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f7f3-138">None</span></span>

## <span data-ttu-id="2f7f3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f7f3-139">OUTPUTS</span></span>

### <span data-ttu-id="2f7f3-140">System. void</span><span class="sxs-lookup"><span data-stu-id="2f7f3-140">System.Void</span></span>

### <span data-ttu-id="2f7f3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f7f3-141">System.Boolean</span></span>

## <span data-ttu-id="2f7f3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f7f3-142">NOTES</span></span>

## <span data-ttu-id="2f7f3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f7f3-143">RELATED LINKS</span></span>
