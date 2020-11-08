---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076275"
---
# <span data-ttu-id="a93dc-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a93dc-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="a93dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a93dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a93dc-103">Возвращает предварительно предоставленный ключ для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a93dc-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="a93dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a93dc-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a93dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a93dc-105">DESCRIPTION</span></span>
<span data-ttu-id="a93dc-106">Командлет **Get-AzureVNetGatewayKey** получает предварительный ключ для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a93dc-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="a93dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a93dc-107">EXAMPLES</span></span>

## <span data-ttu-id="a93dc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a93dc-108">PARAMETERS</span></span>

### <span data-ttu-id="a93dc-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="a93dc-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="a93dc-110">Указывает имя сайта локальной сети, подключенного к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a93dc-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="a93dc-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="a93dc-111">-Profile</span></span>
<span data-ttu-id="a93dc-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a93dc-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a93dc-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a93dc-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a93dc-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a93dc-114">-VNetName</span></span>
<span data-ttu-id="a93dc-115">Указывает виртуальную сеть, для которой этот командлет получает общий ключ для подключений.</span><span class="sxs-lookup"><span data-stu-id="a93dc-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="a93dc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93dc-116">CommonParameters</span></span>
<span data-ttu-id="a93dc-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a93dc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93dc-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93dc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93dc-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a93dc-119">INPUTS</span></span>

## <span data-ttu-id="a93dc-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a93dc-120">OUTPUTS</span></span>

## <span data-ttu-id="a93dc-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="a93dc-121">NOTES</span></span>

## <span data-ttu-id="a93dc-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a93dc-122">RELATED LINKS</span></span>

[<span data-ttu-id="a93dc-123">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a93dc-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


