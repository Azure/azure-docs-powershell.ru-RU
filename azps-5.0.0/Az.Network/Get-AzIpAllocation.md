---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248129"
---
# <span data-ttu-id="b1621-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b1621-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="b1621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1621-102">SYNOPSIS</span></span>
<span data-ttu-id="b1621-103">Получает Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="b1621-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="b1621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1621-104">SYNTAX</span></span>

### <span data-ttu-id="b1621-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1621-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1621-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1621-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1621-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1621-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1621-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1621-108">DESCRIPTION</span></span>
<span data-ttu-id="b1621-109">Командлет **Get-AzIpAllocation** получает Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b1621-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="b1621-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1621-110">EXAMPLES</span></span>

### <span data-ttu-id="b1621-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1621-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="b1621-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1621-112">PARAMETERS</span></span>

### <span data-ttu-id="b1621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1621-113">-DefaultProfile</span></span>
<span data-ttu-id="b1621-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1621-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1621-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1621-115">-Name</span></span>
<span data-ttu-id="b1621-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1621-116">The resource name.</span></span>

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

### <span data-ttu-id="b1621-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1621-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1621-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1621-118">The resource group name.</span></span>

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

### <span data-ttu-id="b1621-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1621-119">-ResourceId</span></span>
<span data-ttu-id="b1621-120">Идентификатор IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b1621-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="b1621-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1621-121">CommonParameters</span></span>
<span data-ttu-id="b1621-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1621-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1621-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1621-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1621-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1621-124">INPUTS</span></span>

### <span data-ttu-id="b1621-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b1621-125">System.String</span></span>

## <span data-ttu-id="b1621-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1621-126">OUTPUTS</span></span>

### <span data-ttu-id="b1621-127">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b1621-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b1621-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1621-128">NOTES</span></span>

## <span data-ttu-id="b1621-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1621-129">RELATED LINKS</span></span>
