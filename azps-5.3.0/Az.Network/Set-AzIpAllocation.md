---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519917"
---
# <span data-ttu-id="b24a1-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b24a1-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="b24a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b24a1-103">Сохранение измененного ipAllocation.</span><span class="sxs-lookup"><span data-stu-id="b24a1-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="b24a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b24a1-104">SYNTAX</span></span>

### <span data-ttu-id="b24a1-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24a1-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b24a1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24a1-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b24a1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24a1-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24a1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b24a1-108">DESCRIPTION</span></span>
<span data-ttu-id="b24a1-109">**Cmdlet Set-AzIpAllocation** обновляет службу IpAllocation Azure.</span><span class="sxs-lookup"><span data-stu-id="b24a1-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="b24a1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b24a1-110">EXAMPLES</span></span>

### <span data-ttu-id="b24a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b24a1-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="b24a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24a1-112">PARAMETERS</span></span>

### <span data-ttu-id="b24a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b24a1-113">-AsJob</span></span>
<span data-ttu-id="b24a1-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b24a1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b24a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24a1-115">-DefaultProfile</span></span>
<span data-ttu-id="b24a1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b24a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24a1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b24a1-117">-InputObject</span></span>
<span data-ttu-id="b24a1-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b24a1-118">The IpAllocation</span></span>

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

### <span data-ttu-id="b24a1-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="b24a1-119">-IpAllocationTag</span></span>
<span data-ttu-id="b24a1-120">Теги выделения для выделения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b24a1-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="b24a1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b24a1-121">-Name</span></span>
<span data-ttu-id="b24a1-122">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b24a1-122">The resource name.</span></span>

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

### <span data-ttu-id="b24a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="b24a1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b24a1-124">The resource group name.</span></span>

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

### <span data-ttu-id="b24a1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24a1-125">-ResourceId</span></span>
<span data-ttu-id="b24a1-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="b24a1-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="b24a1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b24a1-127">-Tag</span></span>
<span data-ttu-id="b24a1-128">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="b24a1-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b24a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24a1-129">CommonParameters</span></span>
<span data-ttu-id="b24a1-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24a1-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b24a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24a1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b24a1-132">INPUTS</span></span>

### <span data-ttu-id="b24a1-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b24a1-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b24a1-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b24a1-134">OUTPUTS</span></span>

### <span data-ttu-id="b24a1-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b24a1-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b24a1-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b24a1-136">NOTES</span></span>

## <span data-ttu-id="b24a1-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b24a1-137">RELATED LINKS</span></span>