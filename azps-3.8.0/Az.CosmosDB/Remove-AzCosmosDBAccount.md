---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: e9ec1f1626a1fb4335c6e5df43a96727692538c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073715"
---
# <span data-ttu-id="52892-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="52892-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="52892-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52892-102">SYNOPSIS</span></span>
<span data-ttu-id="52892-103">Удаление учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="52892-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="52892-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52892-104">SYNTAX</span></span>

### <span data-ttu-id="52892-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52892-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52892-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52892-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52892-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52892-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52892-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52892-108">DESCRIPTION</span></span>
<span data-ttu-id="52892-109">Удаление учетной записи CosmosDB с указанным именем в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52892-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="52892-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52892-110">EXAMPLES</span></span>

### <span data-ttu-id="52892-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52892-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="52892-112">Учетная запись с именем учетной записи dbname в группе ResourceGroup RG удаляется.</span><span class="sxs-lookup"><span data-stu-id="52892-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="52892-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52892-113">PARAMETERS</span></span>

### <span data-ttu-id="52892-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52892-114">-AsJob</span></span>
<span data-ttu-id="52892-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52892-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52892-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52892-116">-Confirm</span></span>
<span data-ttu-id="52892-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52892-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52892-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52892-118">-DefaultProfile</span></span>
<span data-ttu-id="52892-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52892-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52892-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52892-120">-InputObject</span></span>
<span data-ttu-id="52892-121">Объект учетной записи базы данных</span><span class="sxs-lookup"><span data-stu-id="52892-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52892-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52892-122">-Name</span></span>
<span data-ttu-id="52892-123">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="52892-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52892-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52892-124">-PassThru</span></span>
<span data-ttu-id="52892-125">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="52892-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="52892-126">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="52892-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="52892-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52892-127">-ResourceGroupName</span></span>
<span data-ttu-id="52892-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52892-128">Name of resource group.</span></span>

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

### <span data-ttu-id="52892-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52892-129">-ResourceId</span></span>
<span data-ttu-id="52892-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="52892-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52892-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52892-131">-WhatIf</span></span>
<span data-ttu-id="52892-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52892-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52892-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52892-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52892-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52892-134">CommonParameters</span></span>
<span data-ttu-id="52892-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52892-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52892-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52892-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52892-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52892-137">INPUTS</span></span>

### <span data-ttu-id="52892-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="52892-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="52892-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52892-139">OUTPUTS</span></span>

### <span data-ttu-id="52892-140">System. void</span><span class="sxs-lookup"><span data-stu-id="52892-140">System.Void</span></span>

## <span data-ttu-id="52892-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="52892-141">NOTES</span></span>

## <span data-ttu-id="52892-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52892-142">RELATED LINKS</span></span>
