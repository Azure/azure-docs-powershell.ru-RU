---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425279"
---
# <span data-ttu-id="2c77f-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="2c77f-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="2c77f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c77f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c77f-103">Определите SKU сетевого виртуального устройства для ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c77f-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="2c77f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c77f-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c77f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c77f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c77f-106">Команда New-AzVirtualApplianceSkuProperties определяет SKU для ресурса сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="2c77f-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2c77f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c77f-107">EXAMPLES</span></span>

### <span data-ttu-id="2c77f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c77f-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="2c77f-109">Создайте объект "Свойства виртуальной устройства", который будет использоваться с командой New-AzNetworkVirtualAppliance устройств.</span><span class="sxs-lookup"><span data-stu-id="2c77f-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="2c77f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c77f-110">PARAMETERS</span></span>

### <span data-ttu-id="2c77f-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2c77f-111">-BundledScaleUnit</span></span>
<span data-ttu-id="2c77f-112">Единица в пакетном масштабе.</span><span class="sxs-lookup"><span data-stu-id="2c77f-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="2c77f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c77f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c77f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c77f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c77f-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="2c77f-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="2c77f-116">Версия для рынка.</span><span class="sxs-lookup"><span data-stu-id="2c77f-116">The market place version.</span></span>

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

### <span data-ttu-id="2c77f-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="2c77f-117">-VendorName</span></span>
<span data-ttu-id="2c77f-118">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="2c77f-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="2c77f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c77f-119">CommonParameters</span></span>
<span data-ttu-id="2c77f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c77f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c77f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c77f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c77f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c77f-122">INPUTS</span></span>

### <span data-ttu-id="2c77f-123">Нет</span><span class="sxs-lookup"><span data-stu-id="2c77f-123">None</span></span>

## <span data-ttu-id="2c77f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c77f-124">OUTPUTS</span></span>

### <span data-ttu-id="2c77f-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="2c77f-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="2c77f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c77f-126">NOTES</span></span>

## <span data-ttu-id="2c77f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c77f-127">RELATED LINKS</span></span>
