---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732251"
---
# <span data-ttu-id="8443f-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8443f-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8443f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8443f-102">SYNOPSIS</span></span>
<span data-ttu-id="8443f-103">Получает сведения о емкости встроенных данных PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8443f-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8443f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8443f-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="8443f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8443f-105">DESCRIPTION</span></span>
<span data-ttu-id="8443f-106">Командлет Get-AzureRmPowerBIEmbeddedCapacity получает сведения о емкости встроенных данных PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8443f-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="8443f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8443f-107">EXAMPLES</span></span>

### <span data-ttu-id="8443f-108">Пример 1: получение производственных мощностей групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="8443f-108">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="8443f-109">Эта команда получает все внедренную емкость Azure PowerBI в группе ресурсов с именем testRG</span><span class="sxs-lookup"><span data-stu-id="8443f-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="8443f-110">Пример 2: получение емкости</span><span class="sxs-lookup"><span data-stu-id="8443f-110">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="8443f-111">Эта команда возвращает емкость встроенной емкости Azure PowerBI с именем testcapacity в группе ресурсов с именем testRG.</span><span class="sxs-lookup"><span data-stu-id="8443f-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="8443f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8443f-112">PARAMETERS</span></span>

### <span data-ttu-id="8443f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8443f-113">-ResourceGroupName</span></span>
<span data-ttu-id="8443f-114">Имя группы ресурсов Azure, к которой относится емкость</span><span class="sxs-lookup"><span data-stu-id="8443f-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8443f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8443f-115">-Name</span></span>
<span data-ttu-id="8443f-116">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="8443f-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="8443f-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8443f-117">-ResourceId</span></span>
<span data-ttu-id="8443f-118">Идентификатор ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="8443f-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8443f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8443f-119">CommonParameters</span></span>
<span data-ttu-id="8443f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8443f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8443f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8443f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8443f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8443f-122">INPUTS</span></span>

### <span data-ttu-id="8443f-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="8443f-123">None</span></span>
<span data-ttu-id="8443f-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8443f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8443f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8443f-125">OUTPUTS</span></span>

### <span data-ttu-id="8443f-126">List<Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="8443f-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="8443f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8443f-127">NOTES</span></span>

## <span data-ttu-id="8443f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8443f-128">RELATED LINKS</span></span>

[<span data-ttu-id="8443f-129">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8443f-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8443f-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8443f-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
