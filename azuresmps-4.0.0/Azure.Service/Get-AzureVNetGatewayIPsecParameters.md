---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076276"
---
# <span data-ttu-id="d247e-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d247e-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="d247e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d247e-102">SYNOPSIS</span></span>
<span data-ttu-id="d247e-103">Получает параметры IPsec для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d247e-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d247e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d247e-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d247e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d247e-105">DESCRIPTION</span></span>
<span data-ttu-id="d247e-106">Командлет **Get-AzureVNetGatewayIPsecParameters** получает протоколы IP-безопасности (IPSec) и IKE (Internet Key Exchange) для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d247e-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="d247e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d247e-107">EXAMPLES</span></span>

## <span data-ttu-id="d247e-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d247e-108">PARAMETERS</span></span>

### <span data-ttu-id="d247e-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d247e-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d247e-110">Указывает имя сайта локальной сети, подключенного к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d247e-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="d247e-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="d247e-111">-Profile</span></span>
<span data-ttu-id="d247e-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d247e-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d247e-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d247e-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d247e-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d247e-114">-VNetName</span></span>
<span data-ttu-id="d247e-115">Указывает виртуальную сеть, для которой этот командлет получает параметры IPsec для подключения.</span><span class="sxs-lookup"><span data-stu-id="d247e-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="d247e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d247e-116">CommonParameters</span></span>
<span data-ttu-id="d247e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d247e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d247e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d247e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d247e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d247e-119">INPUTS</span></span>

## <span data-ttu-id="d247e-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d247e-120">OUTPUTS</span></span>

## <span data-ttu-id="d247e-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="d247e-121">NOTES</span></span>

## <span data-ttu-id="d247e-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d247e-122">RELATED LINKS</span></span>

[<span data-ttu-id="d247e-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d247e-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


