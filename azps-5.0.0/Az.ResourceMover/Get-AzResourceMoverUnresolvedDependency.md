---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317666"
---
# <span data-ttu-id="a98ee-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="a98ee-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="a98ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a98ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a98ee-103">Получает список неразрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="a98ee-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="a98ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a98ee-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a98ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a98ee-105">DESCRIPTION</span></span>
<span data-ttu-id="a98ee-106">Получает список неразрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="a98ee-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="a98ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a98ee-107">EXAMPLES</span></span>

### <span data-ttu-id="a98ee-108">Пример 1: получение списка неразрешенных зависимых ресурсов</span><span class="sxs-lookup"><span data-stu-id="a98ee-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="a98ee-109">Получение списка неразрешенных зависимых ресурсов для коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="a98ee-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="a98ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a98ee-110">PARAMETERS</span></span>

### <span data-ttu-id="a98ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98ee-111">-DefaultProfile</span></span>
<span data-ttu-id="a98ee-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a98ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a98ee-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="a98ee-113">-MoveCollectionName</span></span>
<span data-ttu-id="a98ee-114">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="a98ee-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a98ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="a98ee-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a98ee-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a98ee-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a98ee-117">-SubscriptionId</span></span>
<span data-ttu-id="a98ee-118">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a98ee-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="a98ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98ee-119">CommonParameters</span></span>
<span data-ttu-id="a98ee-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a98ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98ee-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a98ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98ee-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a98ee-122">INPUTS</span></span>

## <span data-ttu-id="a98ee-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a98ee-123">OUTPUTS</span></span>

### <span data-ttu-id="a98ee-124">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="a98ee-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="a98ee-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a98ee-125">NOTES</span></span>

<span data-ttu-id="a98ee-126">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a98ee-126">ALIASES</span></span>

## <span data-ttu-id="a98ee-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a98ee-127">RELATED LINKS</span></span>

