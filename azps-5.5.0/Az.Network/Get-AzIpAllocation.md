---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223841"
---
# <span data-ttu-id="5bd84-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5bd84-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="5bd84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd84-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd84-103">Получает Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="5bd84-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="5bd84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bd84-104">SYNTAX</span></span>

### <span data-ttu-id="5bd84-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bd84-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bd84-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bd84-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bd84-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bd84-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bd84-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bd84-108">DESCRIPTION</span></span>
<span data-ttu-id="5bd84-109">Для **получения службы IpAllocation** в Azure возвращается cmdlet Get-AzIpAllocation.</span><span class="sxs-lookup"><span data-stu-id="5bd84-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="5bd84-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bd84-110">EXAMPLES</span></span>

### <span data-ttu-id="5bd84-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5bd84-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="5bd84-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd84-112">PARAMETERS</span></span>

### <span data-ttu-id="5bd84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd84-113">-DefaultProfile</span></span>
<span data-ttu-id="5bd84-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5bd84-115">-Name</span></span>
<span data-ttu-id="5bd84-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5bd84-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd84-117">-ResourceGroupName</span></span>
<span data-ttu-id="5bd84-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bd84-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bd84-119">-ResourceId</span></span>
<span data-ttu-id="5bd84-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="5bd84-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd84-121">CommonParameters</span></span>
<span data-ttu-id="5bd84-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd84-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bd84-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd84-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd84-124">INPUTS</span></span>

### <span data-ttu-id="5bd84-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5bd84-125">System.String</span></span>

## <span data-ttu-id="5bd84-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bd84-126">OUTPUTS</span></span>

### <span data-ttu-id="5bd84-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="5bd84-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="5bd84-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bd84-128">NOTES</span></span>

## <span data-ttu-id="5bd84-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bd84-129">RELATED LINKS</span></span>
