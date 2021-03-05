---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000008"
---
# <span data-ttu-id="e1f09-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="e1f09-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="e1f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f09-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f09-103">Список ресурсов для перемещения, для которых требуется ресурс на arm.</span><span class="sxs-lookup"><span data-stu-id="e1f09-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="e1f09-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1f09-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e1f09-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f09-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f09-106">Список ресурсов для перемещения, для которых требуется ресурс на arm.</span><span class="sxs-lookup"><span data-stu-id="e1f09-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="e1f09-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1f09-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f09-108">Пример 1. Получить список необходимых для добавления ресурса armID.</span><span class="sxs-lookup"><span data-stu-id="e1f09-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="e1f09-109">Получить список необходимых для добавления ресурса armID.</span><span class="sxs-lookup"><span data-stu-id="e1f09-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="e1f09-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f09-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f09-111">-DefaultProfile</span></span>
<span data-ttu-id="e1f09-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f09-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="e1f09-113">-MoveCollectionName</span></span>
<span data-ttu-id="e1f09-114">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="e1f09-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e1f09-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f09-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1f09-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1f09-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e1f09-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="e1f09-117">-SourceId</span></span>
<span data-ttu-id="e1f09-118">SourceId, для которого вызывается api.</span><span class="sxs-lookup"><span data-stu-id="e1f09-118">The sourceId for which the api is invoked.</span></span>

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

### <span data-ttu-id="e1f09-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1f09-119">-SubscriptionId</span></span>
<span data-ttu-id="e1f09-120">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="e1f09-120">The Subscription ID.</span></span>

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

### <span data-ttu-id="e1f09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f09-121">CommonParameters</span></span>
<span data-ttu-id="e1f09-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f09-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1f09-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f09-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1f09-124">INPUTS</span></span>

## <span data-ttu-id="e1f09-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1f09-125">OUTPUTS</span></span>

### <span data-ttu-id="e1f09-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e1f09-126">System.String</span></span>

## <span data-ttu-id="e1f09-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1f09-127">NOTES</span></span>

<span data-ttu-id="e1f09-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e1f09-128">ALIASES</span></span>

## <span data-ttu-id="e1f09-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1f09-129">RELATED LINKS</span></span>

