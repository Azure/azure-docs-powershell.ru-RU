---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236846"
---
# <span data-ttu-id="b2def-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="b2def-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="b2def-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2def-102">SYNOPSIS</span></span>
<span data-ttu-id="b2def-103">Удаляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b2def-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="b2def-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2def-104">SYNTAX</span></span>

### <span data-ttu-id="b2def-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2def-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2def-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2def-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2def-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2def-107">DESCRIPTION</span></span>
<span data-ttu-id="b2def-108">Командлет **Remove-AzCosmosDBTable** удаляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b2def-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="b2def-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2def-109">EXAMPLES</span></span>

### <span data-ttu-id="b2def-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2def-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="b2def-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="b2def-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="b2def-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2def-112">PARAMETERS</span></span>

### <span data-ttu-id="b2def-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b2def-113">-AccountName</span></span>
<span data-ttu-id="b2def-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b2def-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b2def-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2def-115">-Confirm</span></span>
<span data-ttu-id="b2def-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2def-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2def-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2def-117">-DefaultProfile</span></span>
<span data-ttu-id="b2def-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2def-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2def-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2def-119">-InputObject</span></span>
<span data-ttu-id="b2def-120">Объект базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b2def-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2def-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2def-121">-Name</span></span>
<span data-ttu-id="b2def-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="b2def-122">Name of the Table.</span></span>

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

### <span data-ttu-id="b2def-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2def-123">-PassThru</span></span>
<span data-ttu-id="b2def-124">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="b2def-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b2def-125">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b2def-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b2def-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2def-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2def-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2def-127">Name of resource group.</span></span>

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

### <span data-ttu-id="b2def-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2def-128">-WhatIf</span></span>
<span data-ttu-id="b2def-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2def-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2def-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2def-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2def-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2def-131">CommonParameters</span></span>
<span data-ttu-id="b2def-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2def-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2def-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2def-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2def-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2def-134">INPUTS</span></span>

### <span data-ttu-id="b2def-135">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b2def-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="b2def-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2def-136">OUTPUTS</span></span>

### <span data-ttu-id="b2def-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b2def-137">System.Void</span></span>

### <span data-ttu-id="b2def-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2def-138">System.Boolean</span></span>

## <span data-ttu-id="b2def-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2def-139">NOTES</span></span>

## <span data-ttu-id="b2def-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2def-140">RELATED LINKS</span></span>
