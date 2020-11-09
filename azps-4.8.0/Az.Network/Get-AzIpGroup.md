---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244138"
---
# <span data-ttu-id="0ffe5-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0ffe5-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="0ffe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ffe5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffe5-103">Получить Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="0ffe5-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="0ffe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ffe5-104">SYNTAX</span></span>

### <span data-ttu-id="0ffe5-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffe5-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ffe5-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ffe5-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ffe5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ffe5-107">DESCRIPTION</span></span>
<span data-ttu-id="0ffe5-108">Командлет **Get-AzIpGroup** получает Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="0ffe5-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="0ffe5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ffe5-109">EXAMPLES</span></span>

### <span data-ttu-id="0ffe5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ffe5-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="0ffe5-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0ffe5-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="0ffe5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ffe5-112">PARAMETERS</span></span>

### <span data-ttu-id="0ffe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffe5-113">-DefaultProfile</span></span>
<span data-ttu-id="0ffe5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffe5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ffe5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ffe5-115">-Name</span></span>
<span data-ttu-id="0ffe5-116">Имя IPGroup.</span><span class="sxs-lookup"><span data-stu-id="0ffe5-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffe5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ffe5-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ffe5-118">Имя группы ресурсов для IPGroup.</span><span class="sxs-lookup"><span data-stu-id="0ffe5-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffe5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ffe5-119">-ResourceId</span></span>
<span data-ttu-id="0ffe5-120">ResourceId для IPGroup.</span><span class="sxs-lookup"><span data-stu-id="0ffe5-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ffe5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffe5-121">CommonParameters</span></span>
<span data-ttu-id="0ffe5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ffe5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffe5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ffe5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffe5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ffe5-124">INPUTS</span></span>

### <span data-ttu-id="0ffe5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffe5-125">System.String</span></span>

## <span data-ttu-id="0ffe5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ffe5-126">OUTPUTS</span></span>

### <span data-ttu-id="0ffe5-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="0ffe5-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="0ffe5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ffe5-128">NOTES</span></span>

## <span data-ttu-id="0ffe5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ffe5-129">RELATED LINKS</span></span>