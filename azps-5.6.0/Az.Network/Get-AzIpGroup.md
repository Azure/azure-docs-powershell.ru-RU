---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 75a7afbb8997492e1b30ead7f745d2f5b6eb8b5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956899"
---
# <span data-ttu-id="0f990-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0f990-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="0f990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f990-102">SYNOPSIS</span></span>
<span data-ttu-id="0f990-103">Получить IpGroup для Azure</span><span class="sxs-lookup"><span data-stu-id="0f990-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="0f990-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f990-104">SYNTAX</span></span>

### <span data-ttu-id="0f990-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f990-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f990-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f990-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f990-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f990-107">DESCRIPTION</span></span>
<span data-ttu-id="0f990-108">**Cmdlet Get-AzIpGroup** получает ipGroup Azure</span><span class="sxs-lookup"><span data-stu-id="0f990-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="0f990-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f990-109">EXAMPLES</span></span>

### <span data-ttu-id="0f990-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f990-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="0f990-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f990-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="0f990-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f990-112">PARAMETERS</span></span>

### <span data-ttu-id="0f990-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f990-113">-DefaultProfile</span></span>
<span data-ttu-id="0f990-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f990-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f990-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f990-115">-Name</span></span>
<span data-ttu-id="0f990-116">Имя ipgroup.</span><span class="sxs-lookup"><span data-stu-id="0f990-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="0f990-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f990-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f990-118">Имя группы ресурсов ipgroup.</span><span class="sxs-lookup"><span data-stu-id="0f990-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="0f990-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f990-119">-ResourceId</span></span>
<span data-ttu-id="0f990-120">ResourceId ipgroup.</span><span class="sxs-lookup"><span data-stu-id="0f990-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="0f990-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f990-121">CommonParameters</span></span>
<span data-ttu-id="0f990-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f990-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f990-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f990-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f990-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f990-124">INPUTS</span></span>

### <span data-ttu-id="0f990-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0f990-125">System.String</span></span>

## <span data-ttu-id="0f990-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f990-126">OUTPUTS</span></span>

### <span data-ttu-id="0f990-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="0f990-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="0f990-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f990-128">NOTES</span></span>

## <span data-ttu-id="0f990-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f990-129">RELATED LINKS</span></span>
