---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075465"
---
# <span data-ttu-id="cf94d-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf94d-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="cf94d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf94d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf94d-103">Сброс VPN-шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cf94d-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="cf94d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf94d-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf94d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf94d-105">DESCRIPTION</span></span>
<span data-ttu-id="cf94d-106">Командлет **Reset-AzureVNetGateway** сбрасывает и перезапускает шлюз виртуальной сети виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="cf94d-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="cf94d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf94d-107">EXAMPLES</span></span>

### <span data-ttu-id="cf94d-108">Пример 1: сброс шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cf94d-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="cf94d-109">Эта команда сбрасывает шлюз виртуальной сети из виртуальной сети с именем ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="cf94d-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="cf94d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf94d-110">PARAMETERS</span></span>

### <span data-ttu-id="cf94d-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf94d-111">-Profile</span></span>
<span data-ttu-id="cf94d-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf94d-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cf94d-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf94d-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf94d-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="cf94d-114">-VNetName</span></span>
<span data-ttu-id="cf94d-115">Указывает виртуальную сеть, которая содержит шлюз виртуальной сети, который сбрасывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cf94d-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="cf94d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf94d-116">CommonParameters</span></span>
<span data-ttu-id="cf94d-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf94d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf94d-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf94d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf94d-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf94d-119">INPUTS</span></span>

## <span data-ttu-id="cf94d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf94d-120">OUTPUTS</span></span>

## <span data-ttu-id="cf94d-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf94d-121">NOTES</span></span>

## <span data-ttu-id="cf94d-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf94d-122">RELATED LINKS</span></span>

[<span data-ttu-id="cf94d-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf94d-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="cf94d-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf94d-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="cf94d-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf94d-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="cf94d-126">Изменить размер — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="cf94d-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="cf94d-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="cf94d-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


