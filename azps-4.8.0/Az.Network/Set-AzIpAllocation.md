---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078838"
---
# <span data-ttu-id="f750b-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="f750b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f750b-102">SYNOPSIS</span></span>
<span data-ttu-id="f750b-103">Сохранение измененного IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="f750b-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="f750b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f750b-104">SYNTAX</span></span>

### <span data-ttu-id="f750b-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f750b-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f750b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f750b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f750b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f750b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f750b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f750b-108">DESCRIPTION</span></span>
<span data-ttu-id="f750b-109">Командлет **Set-AzIpAllocation** обновляет Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="f750b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f750b-110">EXAMPLES</span></span>

### <span data-ttu-id="f750b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f750b-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="f750b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f750b-112">PARAMETERS</span></span>

### <span data-ttu-id="f750b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f750b-113">-AsJob</span></span>
<span data-ttu-id="f750b-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f750b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f750b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f750b-115">-DefaultProfile</span></span>
<span data-ttu-id="f750b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f750b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f750b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f750b-117">-InputObject</span></span>
<span data-ttu-id="f750b-118">IpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-118">The IpAllocation</span></span>

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

### <span data-ttu-id="f750b-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="f750b-119">-IpAllocationTag</span></span>
<span data-ttu-id="f750b-120">Теги выделения для IP-адреса</span><span class="sxs-lookup"><span data-stu-id="f750b-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="f750b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f750b-121">-Name</span></span>
<span data-ttu-id="f750b-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f750b-122">The resource name.</span></span>

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

### <span data-ttu-id="f750b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f750b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f750b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f750b-124">The resource group name.</span></span>

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

### <span data-ttu-id="f750b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f750b-125">-ResourceId</span></span>
<span data-ttu-id="f750b-126">Идентификатор IpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="f750b-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="f750b-127">-Tag</span></span>
<span data-ttu-id="f750b-128">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f750b-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f750b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f750b-129">CommonParameters</span></span>
<span data-ttu-id="f750b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f750b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f750b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f750b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f750b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f750b-132">INPUTS</span></span>

### <span data-ttu-id="f750b-133">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="f750b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f750b-134">OUTPUTS</span></span>

### <span data-ttu-id="f750b-135">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="f750b-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="f750b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f750b-136">NOTES</span></span>

## <span data-ttu-id="f750b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f750b-137">RELATED LINKS</span></span>
