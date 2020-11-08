---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075626"
---
# <span data-ttu-id="f49f8-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="f49f8-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="f49f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f49f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f49f8-103">Получение сведений об устройстве VPN.</span><span class="sxs-lookup"><span data-stu-id="f49f8-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="f49f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f49f8-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f49f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f49f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f49f8-106">Командлет **Get-AzureRemoteAppVpnDevice** извлекает сведения об устройстве виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="f49f8-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="f49f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f49f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f49f8-108">Пример 1: возврат доступных конфигураций VPN-устройств для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f49f8-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="f49f8-109">Эта команда возвращает доступные конфигурации VPN-устройств для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f49f8-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="f49f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f49f8-110">PARAMETERS</span></span>

### <span data-ttu-id="f49f8-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="f49f8-111">-Profile</span></span>
<span data-ttu-id="f49f8-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f49f8-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f49f8-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f49f8-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f49f8-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f49f8-114">-VNetName</span></span>
<span data-ttu-id="f49f8-115">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="f49f8-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49f8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49f8-116">CommonParameters</span></span>
<span data-ttu-id="f49f8-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f49f8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49f8-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49f8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49f8-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f49f8-119">INPUTS</span></span>

## <span data-ttu-id="f49f8-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f49f8-120">OUTPUTS</span></span>

### <span data-ttu-id="f49f8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f49f8-121">System.String</span></span>

## <span data-ttu-id="f49f8-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="f49f8-122">NOTES</span></span>

## <span data-ttu-id="f49f8-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f49f8-123">RELATED LINKS</span></span>

[<span data-ttu-id="f49f8-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="f49f8-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="f49f8-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="f49f8-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


