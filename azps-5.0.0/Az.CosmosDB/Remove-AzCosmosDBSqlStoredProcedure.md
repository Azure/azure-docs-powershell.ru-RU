---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314639"
---
# <span data-ttu-id="0781d-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="0781d-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="0781d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0781d-102">SYNOPSIS</span></span>
<span data-ttu-id="0781d-103">Удаляет CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="0781d-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="0781d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0781d-104">SYNTAX</span></span>

### <span data-ttu-id="0781d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0781d-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0781d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0781d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0781d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0781d-107">DESCRIPTION</span></span>
<span data-ttu-id="0781d-108">Командлет **Remove-AzCosmosDBSqlStoredProcedure** удаляет CosmosDB SQL StoredProcedure, соответствующие указанным ResourceGroupName, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0781d-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="0781d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0781d-109">EXAMPLES</span></span>

### <span data-ttu-id="0781d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0781d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="0781d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0781d-111">PARAMETERS</span></span>

### <span data-ttu-id="0781d-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0781d-112">-AccountName</span></span>
<span data-ttu-id="0781d-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0781d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0781d-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0781d-114">-Confirm</span></span>
<span data-ttu-id="0781d-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0781d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0781d-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0781d-116">-ContainerName</span></span>
<span data-ttu-id="0781d-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="0781d-117">Container name.</span></span>

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

### <span data-ttu-id="0781d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0781d-118">-DatabaseName</span></span>
<span data-ttu-id="0781d-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0781d-119">Database name.</span></span>

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

### <span data-ttu-id="0781d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0781d-120">-DefaultProfile</span></span>
<span data-ttu-id="0781d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0781d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0781d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0781d-122">-InputObject</span></span>
<span data-ttu-id="0781d-123">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="0781d-123">Sql Database object.</span></span>

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

### <span data-ttu-id="0781d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0781d-124">-Name</span></span>
<span data-ttu-id="0781d-125">Имя сохраненного Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="0781d-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="0781d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0781d-126">-PassThru</span></span>
<span data-ttu-id="0781d-127">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="0781d-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="0781d-128">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="0781d-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="0781d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0781d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0781d-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0781d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="0781d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0781d-131">-WhatIf</span></span>
<span data-ttu-id="0781d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0781d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0781d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0781d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0781d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0781d-134">CommonParameters</span></span>
<span data-ttu-id="0781d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0781d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0781d-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0781d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0781d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0781d-137">INPUTS</span></span>

### <span data-ttu-id="0781d-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="0781d-138">None</span></span>

## <span data-ttu-id="0781d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0781d-139">OUTPUTS</span></span>

### <span data-ttu-id="0781d-140">System. void</span><span class="sxs-lookup"><span data-stu-id="0781d-140">System.Void</span></span>

### <span data-ttu-id="0781d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0781d-141">System.Boolean</span></span>

## <span data-ttu-id="0781d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0781d-142">NOTES</span></span>

## <span data-ttu-id="0781d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0781d-143">RELATED LINKS</span></span>
