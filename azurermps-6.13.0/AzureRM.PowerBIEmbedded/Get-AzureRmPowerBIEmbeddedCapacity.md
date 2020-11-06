---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560783"
---
# <span data-ttu-id="13ffe-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="13ffe-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="13ffe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="13ffe-103">Получает сведения о емкости встроенных данных PowerBI.</span><span class="sxs-lookup"><span data-stu-id="13ffe-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ffe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13ffe-104">SYNTAX</span></span>

### <span data-ttu-id="13ffe-105">ByCapacityOrResourceGroupOrSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13ffe-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ffe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13ffe-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ffe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="13ffe-108">Командлет Get-AzureRmPowerBIEmbeddedCapacity получает сведения о емкости встроенных данных PowerBI.</span><span class="sxs-lookup"><span data-stu-id="13ffe-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="13ffe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13ffe-109">EXAMPLES</span></span>

### <span data-ttu-id="13ffe-110">Пример 1: получение производственных мощностей групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="13ffe-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="13ffe-111">Эта команда получает все внедренную емкость Azure PowerBI в группе ресурсов с именем testRG</span><span class="sxs-lookup"><span data-stu-id="13ffe-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="13ffe-112">Пример 2: получение емкости</span><span class="sxs-lookup"><span data-stu-id="13ffe-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="13ffe-113">Эта команда возвращает емкость встроенной емкости Azure PowerBI с именем testcapacity в группе ресурсов с именем testRG.</span><span class="sxs-lookup"><span data-stu-id="13ffe-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="13ffe-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13ffe-114">PARAMETERS</span></span>

### <span data-ttu-id="13ffe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ffe-115">-DefaultProfile</span></span>
<span data-ttu-id="13ffe-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13ffe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ffe-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13ffe-117">-Name</span></span>
<span data-ttu-id="13ffe-118">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="13ffe-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="13ffe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ffe-119">-ResourceGroupName</span></span>
<span data-ttu-id="13ffe-120">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="13ffe-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="13ffe-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ffe-121">-ResourceId</span></span>
<span data-ttu-id="13ffe-122">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="13ffe-122">Azure resource ID</span></span>

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

### <span data-ttu-id="13ffe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ffe-123">CommonParameters</span></span>
<span data-ttu-id="13ffe-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13ffe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ffe-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ffe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ffe-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13ffe-126">INPUTS</span></span>

### <span data-ttu-id="13ffe-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13ffe-127">System.String</span></span>

## <span data-ttu-id="13ffe-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13ffe-128">OUTPUTS</span></span>

### <span data-ttu-id="13ffe-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="13ffe-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="13ffe-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="13ffe-130">NOTES</span></span>

## <span data-ttu-id="13ffe-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13ffe-131">RELATED LINKS</span></span>

[<span data-ttu-id="13ffe-132">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="13ffe-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="13ffe-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="13ffe-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
