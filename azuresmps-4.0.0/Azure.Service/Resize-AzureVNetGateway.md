---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076087"
---
# <span data-ttu-id="18622-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="18622-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="18622-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18622-102">SYNOPSIS</span></span>
<span data-ttu-id="18622-103">Изменение размера шлюза VPN.</span><span class="sxs-lookup"><span data-stu-id="18622-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="18622-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18622-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="18622-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18622-105">DESCRIPTION</span></span>
<span data-ttu-id="18622-106">Командлет **resize-AzureVNetGateway** изменяет размер шлюза виртуальной частной сети виртуальной сети (VPN) на другой SKU.</span><span class="sxs-lookup"><span data-stu-id="18622-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="18622-107">Допустимые SKU для шлюза виртуальной сети: Default, Standard и HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="18622-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="18622-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18622-108">EXAMPLES</span></span>

### <span data-ttu-id="18622-109">Пример 1: изменение номера SKU для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="18622-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="18622-110">Эта команда изменяет конфигурацию шлюза виртуальной сети для виртуальной сети с именем ContosoVN07 на HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="18622-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="18622-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18622-111">PARAMETERS</span></span>

### <span data-ttu-id="18622-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="18622-112">-GatewaySKU</span></span>
<span data-ttu-id="18622-113">Указывает SKU, для которого этот командлет изменяет размер виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="18622-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="18622-114">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="18622-114">Valid values are:</span></span> 

- <span data-ttu-id="18622-115">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="18622-115">Default</span></span> 
- <span data-ttu-id="18622-116">Стандартная</span><span class="sxs-lookup"><span data-stu-id="18622-116">Standard</span></span> 
- <span data-ttu-id="18622-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="18622-117">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18622-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="18622-118">-Profile</span></span>
<span data-ttu-id="18622-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18622-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="18622-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18622-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18622-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="18622-121">-VNetName</span></span>
<span data-ttu-id="18622-122">Указывает виртуальную сеть, в которой этот командлет изменяет размер шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="18622-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18622-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18622-123">CommonParameters</span></span>
<span data-ttu-id="18622-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18622-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18622-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18622-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18622-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18622-126">INPUTS</span></span>

## <span data-ttu-id="18622-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18622-127">OUTPUTS</span></span>

## <span data-ttu-id="18622-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="18622-128">NOTES</span></span>

## <span data-ttu-id="18622-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18622-129">RELATED LINKS</span></span>

[<span data-ttu-id="18622-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="18622-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="18622-131">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="18622-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="18622-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="18622-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="18622-133">Сброс — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="18622-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="18622-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="18622-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


