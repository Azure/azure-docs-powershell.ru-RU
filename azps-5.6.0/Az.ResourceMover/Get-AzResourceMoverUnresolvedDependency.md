---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999992"
---
# <span data-ttu-id="18fd7-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="18fd7-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="18fd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="18fd7-103">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="18fd7-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="18fd7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18fd7-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="18fd7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="18fd7-106">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="18fd7-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="18fd7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="18fd7-108">Пример 1. Получить список неурегулированных зависимых ресурсов для коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="18fd7-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="18fd7-109">Получить список неоконченных зависимых ресурсов для перемещаемого сбора.</span><span class="sxs-lookup"><span data-stu-id="18fd7-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="18fd7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18fd7-110">PARAMETERS</span></span>

### <span data-ttu-id="18fd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fd7-111">-DefaultProfile</span></span>
<span data-ttu-id="18fd7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18fd7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="18fd7-113">-DependencyLevel</span></span>
<span data-ttu-id="18fd7-114">Определяет уровень зависимости.</span><span class="sxs-lookup"><span data-stu-id="18fd7-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="18fd7-115">-Filter</span></span>
<span data-ttu-id="18fd7-116">Фильтр, который нужно применить к операции.</span><span class="sxs-lookup"><span data-stu-id="18fd7-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="18fd7-117">Например, $apply=filter(count eq 2).</span><span class="sxs-lookup"><span data-stu-id="18fd7-117">For example, $apply=filter(count eq 2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="18fd7-118">-MoveCollectionName</span></span>
<span data-ttu-id="18fd7-119">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="18fd7-119">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="18fd7-120">-Orderby</span></span>
<span data-ttu-id="18fd7-121">Параметр "Порядок OData по запросу".</span><span class="sxs-lookup"><span data-stu-id="18fd7-121">OData order by query option.</span></span>
<span data-ttu-id="18fd7-122">Например, можно использовать $orderby=Количество desc.</span><span class="sxs-lookup"><span data-stu-id="18fd7-122">For example, you can use $orderby=Count desc.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fd7-123">-ResourceGroupName</span></span>
<span data-ttu-id="18fd7-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18fd7-124">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18fd7-125">-SubscriptionId</span></span>
<span data-ttu-id="18fd7-126">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="18fd7-126">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18fd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fd7-127">CommonParameters</span></span>
<span data-ttu-id="18fd7-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fd7-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18fd7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fd7-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18fd7-130">INPUTS</span></span>

## <span data-ttu-id="18fd7-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18fd7-131">OUTPUTS</span></span>

### <span data-ttu-id="18fd7-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="18fd7-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="18fd7-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18fd7-133">NOTES</span></span>

<span data-ttu-id="18fd7-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18fd7-134">ALIASES</span></span>

## <span data-ttu-id="18fd7-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18fd7-135">RELATED LINKS</span></span>

