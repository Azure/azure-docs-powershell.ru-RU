---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408316"
---
# <span data-ttu-id="11571-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="11571-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="11571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11571-102">SYNOPSIS</span></span>
<span data-ttu-id="11571-103">Подробные сведения о внедренной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="11571-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="11571-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11571-104">SYNTAX</span></span>

### <span data-ttu-id="11571-105">ByCapacityOrResourceGroupOrSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11571-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11571-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="11571-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11571-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11571-107">DESCRIPTION</span></span>
<span data-ttu-id="11571-108">С Get-AzPowerBIEmbeddedCapacity управления получают сведения о внедренной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="11571-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="11571-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11571-109">EXAMPLES</span></span>

### <span data-ttu-id="11571-110">Пример 1. Группировка ресурсов</span><span class="sxs-lookup"><span data-stu-id="11571-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="11571-111">Эта команда получает все внедренные мощности Azure PowerBI в группе ресурсов TestRG</span><span class="sxs-lookup"><span data-stu-id="11571-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="11571-112">Пример 2. Получить емкость</span><span class="sxs-lookup"><span data-stu-id="11571-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="11571-113">Эта команда получает встроенную мощность Azure PowerBI Testcapacity в группе ресурсов TestRG.</span><span class="sxs-lookup"><span data-stu-id="11571-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="11571-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11571-114">PARAMETERS</span></span>

### <span data-ttu-id="11571-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11571-115">-DefaultProfile</span></span>
<span data-ttu-id="11571-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11571-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11571-117">-Name</span><span class="sxs-lookup"><span data-stu-id="11571-117">-Name</span></span>
<span data-ttu-id="11571-118">Имя внедренной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="11571-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11571-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11571-119">-ResourceGroupName</span></span>
<span data-ttu-id="11571-120">Имя группы ресурсов Azure, к которой относится пропускная способность</span><span class="sxs-lookup"><span data-stu-id="11571-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11571-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11571-121">-ResourceId</span></span>
<span data-ttu-id="11571-122">ИД ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="11571-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11571-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11571-123">CommonParameters</span></span>
<span data-ttu-id="11571-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11571-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11571-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11571-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11571-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11571-126">INPUTS</span></span>

### <span data-ttu-id="11571-127">System.String</span><span class="sxs-lookup"><span data-stu-id="11571-127">System.String</span></span>

## <span data-ttu-id="11571-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11571-128">OUTPUTS</span></span>

### <span data-ttu-id="11571-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="11571-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="11571-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11571-130">NOTES</span></span>

## <span data-ttu-id="11571-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11571-131">RELATED LINKS</span></span>

[<span data-ttu-id="11571-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="11571-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="11571-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="11571-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
