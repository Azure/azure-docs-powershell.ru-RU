---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314693"
---
# <span data-ttu-id="486fb-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="486fb-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="486fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="486fb-102">SYNOPSIS</span></span>
<span data-ttu-id="486fb-103">Удаление учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="486fb-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="486fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="486fb-104">SYNTAX</span></span>

### <span data-ttu-id="486fb-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="486fb-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486fb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="486fb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486fb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="486fb-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="486fb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="486fb-108">DESCRIPTION</span></span>
<span data-ttu-id="486fb-109">Удаление учетной записи CosmosDB с указанным именем в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="486fb-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="486fb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="486fb-110">EXAMPLES</span></span>

### <span data-ttu-id="486fb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="486fb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="486fb-112">Учетная запись с именем учетной записи dbname в группе ResourceGroup RG удаляется.</span><span class="sxs-lookup"><span data-stu-id="486fb-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="486fb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="486fb-113">PARAMETERS</span></span>

### <span data-ttu-id="486fb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="486fb-114">-AsJob</span></span>
<span data-ttu-id="486fb-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="486fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="486fb-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="486fb-116">-Confirm</span></span>
<span data-ttu-id="486fb-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="486fb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486fb-118">-DefaultProfile</span></span>
<span data-ttu-id="486fb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="486fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="486fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="486fb-120">-InputObject</span></span>
<span data-ttu-id="486fb-121">Объект учетной записи базы данных</span><span class="sxs-lookup"><span data-stu-id="486fb-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486fb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="486fb-122">-Name</span></span>
<span data-ttu-id="486fb-123">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="486fb-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="486fb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="486fb-124">-PassThru</span></span>
<span data-ttu-id="486fb-125">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="486fb-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="486fb-126">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="486fb-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="486fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="486fb-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="486fb-128">Name of resource group.</span></span>

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

### <span data-ttu-id="486fb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="486fb-129">-ResourceId</span></span>
<span data-ttu-id="486fb-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="486fb-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="486fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486fb-131">-WhatIf</span></span>
<span data-ttu-id="486fb-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="486fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="486fb-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="486fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="486fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486fb-134">CommonParameters</span></span>
<span data-ttu-id="486fb-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="486fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486fb-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="486fb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486fb-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="486fb-137">INPUTS</span></span>

### <span data-ttu-id="486fb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="486fb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="486fb-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="486fb-139">OUTPUTS</span></span>

### <span data-ttu-id="486fb-140">System. void</span><span class="sxs-lookup"><span data-stu-id="486fb-140">System.Void</span></span>

## <span data-ttu-id="486fb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="486fb-141">NOTES</span></span>

## <span data-ttu-id="486fb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="486fb-142">RELATED LINKS</span></span>