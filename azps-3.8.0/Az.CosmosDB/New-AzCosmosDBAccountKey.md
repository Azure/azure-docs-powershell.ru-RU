---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066387"
---
# <span data-ttu-id="ea939-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea939-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="ea939-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea939-102">SYNOPSIS</span></span>
<span data-ttu-id="ea939-103">Повторное создание указанного ключа учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ea939-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="ea939-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea939-104">SYNTAX</span></span>

### <span data-ttu-id="ea939-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea939-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea939-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea939-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea939-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea939-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea939-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea939-108">DESCRIPTION</span></span>
<span data-ttu-id="ea939-109">Создание новой учетной записи CosmosDB в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea939-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="ea939-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea939-110">EXAMPLES</span></span>

### <span data-ttu-id="ea939-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea939-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="ea939-112">Новые ключи создаются для учетной записи с именем учетной записи dbname в группе ResourceGroup RG.</span><span class="sxs-lookup"><span data-stu-id="ea939-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="ea939-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea939-113">PARAMETERS</span></span>

### <span data-ttu-id="ea939-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea939-114">-AsJob</span></span>
<span data-ttu-id="ea939-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ea939-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea939-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea939-116">-Confirm</span></span>
<span data-ttu-id="ea939-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea939-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea939-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea939-118">-DefaultProfile</span></span>
<span data-ttu-id="ea939-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea939-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea939-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea939-120">-InputObject</span></span>
<span data-ttu-id="ea939-121">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ea939-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ea939-122">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="ea939-122">-KeyKind</span></span>
<span data-ttu-id="ea939-123">Клавиша доступа для повторного создания.</span><span class="sxs-lookup"><span data-stu-id="ea939-123">The access key to regenerate.</span></span>
<span data-ttu-id="ea939-124">Допустимые значения: Primary, primaryReadonly, Secondary, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="ea939-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea939-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea939-125">-Name</span></span>
<span data-ttu-id="ea939-126">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ea939-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ea939-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea939-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea939-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea939-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ea939-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea939-129">-ResourceId</span></span>
<span data-ttu-id="ea939-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="ea939-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="ea939-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea939-131">-WhatIf</span></span>
<span data-ttu-id="ea939-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea939-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea939-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea939-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea939-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea939-134">CommonParameters</span></span>
<span data-ttu-id="ea939-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea939-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea939-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea939-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea939-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea939-137">INPUTS</span></span>

### <span data-ttu-id="ea939-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea939-138">None</span></span>

## <span data-ttu-id="ea939-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea939-139">OUTPUTS</span></span>

### <span data-ttu-id="ea939-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ea939-140">System.Void</span></span>

## <span data-ttu-id="ea939-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea939-141">NOTES</span></span>

## <span data-ttu-id="ea939-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea939-142">RELATED LINKS</span></span>
