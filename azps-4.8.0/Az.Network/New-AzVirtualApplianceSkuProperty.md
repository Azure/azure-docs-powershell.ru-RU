---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236022"
---
# <span data-ttu-id="ab97a-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="ab97a-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="ab97a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab97a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab97a-103">Определите конфигурацию сетевого управляющего виртуального устройства для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab97a-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="ab97a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab97a-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab97a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab97a-105">DESCRIPTION</span></span>
<span data-ttu-id="ab97a-106">Команда New-AzVirtualApplianceSkuProperties определяет ресурс SKU для сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="ab97a-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ab97a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab97a-107">EXAMPLES</span></span>

### <span data-ttu-id="ab97a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab97a-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="ab97a-109">Создание объекта свойств SKU виртуального устройства для использования с New-AzNetworkVirtualAppliance командой.</span><span class="sxs-lookup"><span data-stu-id="ab97a-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="ab97a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab97a-110">PARAMETERS</span></span>

### <span data-ttu-id="ab97a-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ab97a-111">-BundledScaleUnit</span></span>
<span data-ttu-id="ab97a-112">Единица измерения в объединенном наборе.</span><span class="sxs-lookup"><span data-stu-id="ab97a-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab97a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab97a-113">-DefaultProfile</span></span>
<span data-ttu-id="ab97a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab97a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab97a-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="ab97a-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="ab97a-116">Версия на своем рынке.</span><span class="sxs-lookup"><span data-stu-id="ab97a-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab97a-117">-ИмяПоставщика</span><span class="sxs-lookup"><span data-stu-id="ab97a-117">-VendorName</span></span>
<span data-ttu-id="ab97a-118">Название поставщика.</span><span class="sxs-lookup"><span data-stu-id="ab97a-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab97a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab97a-119">CommonParameters</span></span>
<span data-ttu-id="ab97a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab97a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab97a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab97a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab97a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab97a-122">INPUTS</span></span>

### <span data-ttu-id="ab97a-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="ab97a-123">None</span></span>

## <span data-ttu-id="ab97a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab97a-124">OUTPUTS</span></span>

### <span data-ttu-id="ab97a-125">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="ab97a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="ab97a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab97a-126">NOTES</span></span>

## <span data-ttu-id="ab97a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab97a-127">RELATED LINKS</span></span>
