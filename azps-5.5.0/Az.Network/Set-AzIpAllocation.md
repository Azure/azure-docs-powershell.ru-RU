---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236500"
---
# <span data-ttu-id="b2ebe-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b2ebe-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="b2ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ebe-103">Сохранение измененного ipAllocation.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="b2ebe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2ebe-104">SYNTAX</span></span>

### <span data-ttu-id="b2ebe-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2ebe-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ebe-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2ebe-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ebe-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2ebe-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2ebe-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2ebe-108">DESCRIPTION</span></span>
<span data-ttu-id="b2ebe-109">**Cmdlet Set-AzIpAllocation** обновляет службу IpAllocation Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="b2ebe-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2ebe-110">EXAMPLES</span></span>

### <span data-ttu-id="b2ebe-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2ebe-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="b2ebe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2ebe-112">PARAMETERS</span></span>

### <span data-ttu-id="b2ebe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2ebe-113">-AsJob</span></span>
<span data-ttu-id="b2ebe-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b2ebe-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ebe-115">-DefaultProfile</span></span>
<span data-ttu-id="b2ebe-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2ebe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2ebe-117">-InputObject</span></span>
<span data-ttu-id="b2ebe-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b2ebe-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="b2ebe-119">-IpAllocationTag</span></span>
<span data-ttu-id="b2ebe-120">Теги выделения для выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b2ebe-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2ebe-121">-Name</span></span>
<span data-ttu-id="b2ebe-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ebe-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2ebe-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2ebe-125">-ResourceId</span></span>
<span data-ttu-id="b2ebe-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="b2ebe-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2ebe-127">-Tag</span></span>
<span data-ttu-id="b2ebe-128">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ebe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ebe-129">CommonParameters</span></span>
<span data-ttu-id="b2ebe-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ebe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ebe-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2ebe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ebe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2ebe-132">INPUTS</span></span>

### <span data-ttu-id="b2ebe-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b2ebe-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b2ebe-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2ebe-134">OUTPUTS</span></span>

### <span data-ttu-id="b2ebe-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b2ebe-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b2ebe-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2ebe-136">NOTES</span></span>

## <span data-ttu-id="b2ebe-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2ebe-137">RELATED LINKS</span></span>
