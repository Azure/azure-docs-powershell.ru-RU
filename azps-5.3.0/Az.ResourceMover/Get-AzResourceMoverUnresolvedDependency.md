---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506712"
---
# <span data-ttu-id="281cf-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="281cf-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="281cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="281cf-102">SYNOPSIS</span></span>
<span data-ttu-id="281cf-103">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="281cf-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="281cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="281cf-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="281cf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="281cf-105">DESCRIPTION</span></span>
<span data-ttu-id="281cf-106">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="281cf-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="281cf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="281cf-107">EXAMPLES</span></span>

### <span data-ttu-id="281cf-108">Пример 1. Получить список неурегулированных зависимых ресурсов</span><span class="sxs-lookup"><span data-stu-id="281cf-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="281cf-109">Получить список неоконченных зависимых ресурсов для коллекции "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="281cf-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="281cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="281cf-110">PARAMETERS</span></span>

### <span data-ttu-id="281cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281cf-111">-DefaultProfile</span></span>
<span data-ttu-id="281cf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="281cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="281cf-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="281cf-113">-MoveCollectionName</span></span>
<span data-ttu-id="281cf-114">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="281cf-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="281cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="281cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="281cf-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="281cf-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="281cf-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="281cf-117">-SubscriptionId</span></span>
<span data-ttu-id="281cf-118">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="281cf-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="281cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281cf-119">CommonParameters</span></span>
<span data-ttu-id="281cf-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="281cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281cf-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="281cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281cf-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="281cf-122">INPUTS</span></span>

## <span data-ttu-id="281cf-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="281cf-123">OUTPUTS</span></span>

### <span data-ttu-id="281cf-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="281cf-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="281cf-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="281cf-125">NOTES</span></span>

<span data-ttu-id="281cf-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="281cf-126">ALIASES</span></span>

## <span data-ttu-id="281cf-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="281cf-127">RELATED LINKS</span></span>

