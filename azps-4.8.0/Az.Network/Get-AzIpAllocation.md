---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244141"
---
# <span data-ttu-id="444f5-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="444f5-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="444f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="444f5-102">SYNOPSIS</span></span>
<span data-ttu-id="444f5-103">Получает Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="444f5-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="444f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="444f5-104">SYNTAX</span></span>

### <span data-ttu-id="444f5-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="444f5-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="444f5-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="444f5-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="444f5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="444f5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="444f5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="444f5-108">DESCRIPTION</span></span>
<span data-ttu-id="444f5-109">Командлет **Get-AzIpAllocation** получает Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="444f5-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="444f5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="444f5-110">EXAMPLES</span></span>

### <span data-ttu-id="444f5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="444f5-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="444f5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="444f5-112">PARAMETERS</span></span>

### <span data-ttu-id="444f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="444f5-113">-DefaultProfile</span></span>
<span data-ttu-id="444f5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="444f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="444f5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="444f5-115">-Name</span></span>
<span data-ttu-id="444f5-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="444f5-116">The resource name.</span></span>

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

### <span data-ttu-id="444f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="444f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="444f5-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="444f5-118">The resource group name.</span></span>

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

### <span data-ttu-id="444f5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="444f5-119">-ResourceId</span></span>
<span data-ttu-id="444f5-120">Идентификатор IpAllocation</span><span class="sxs-lookup"><span data-stu-id="444f5-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="444f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="444f5-121">CommonParameters</span></span>
<span data-ttu-id="444f5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="444f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="444f5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="444f5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="444f5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="444f5-124">INPUTS</span></span>

### <span data-ttu-id="444f5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="444f5-125">System.String</span></span>

## <span data-ttu-id="444f5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="444f5-126">OUTPUTS</span></span>

### <span data-ttu-id="444f5-127">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="444f5-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="444f5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="444f5-128">NOTES</span></span>

## <span data-ttu-id="444f5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="444f5-129">RELATED LINKS</span></span>
