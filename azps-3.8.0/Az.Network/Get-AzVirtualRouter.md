---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065834"
---
# <span data-ttu-id="d76b8-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d76b8-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="d76b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d76b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d76b8-103">Получить Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d76b8-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="d76b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d76b8-104">SYNTAX</span></span>

### <span data-ttu-id="d76b8-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d76b8-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d76b8-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76b8-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d76b8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76b8-107">DESCRIPTION</span></span>
<span data-ttu-id="d76b8-108">Командлет **Get-AzVirtualRouter** получает Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d76b8-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="d76b8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d76b8-109">EXAMPLES</span></span>

### <span data-ttu-id="d76b8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d76b8-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="d76b8-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d76b8-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="d76b8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d76b8-112">PARAMETERS</span></span>

### <span data-ttu-id="d76b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76b8-113">-DefaultProfile</span></span>
<span data-ttu-id="d76b8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d76b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76b8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76b8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d76b8-116">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d76b8-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76b8-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d76b8-117">-ResourceId</span></span>
<span data-ttu-id="d76b8-118">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d76b8-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76b8-119">-RouterName</span><span class="sxs-lookup"><span data-stu-id="d76b8-119">-RouterName</span></span>
<span data-ttu-id="d76b8-120">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d76b8-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76b8-121">CommonParameters</span></span>
<span data-ttu-id="d76b8-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d76b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76b8-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d76b8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76b8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d76b8-124">INPUTS</span></span>

### <span data-ttu-id="d76b8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d76b8-125">System.String</span></span>

## <span data-ttu-id="d76b8-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76b8-126">OUTPUTS</span></span>

### <span data-ttu-id="d76b8-127">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d76b8-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="d76b8-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d76b8-128">NOTES</span></span>

## <span data-ttu-id="d76b8-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d76b8-129">RELATED LINKS</span></span>
