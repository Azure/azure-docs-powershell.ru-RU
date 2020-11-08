---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075810"
---
# <span data-ttu-id="d5ef4-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d5ef4-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="d5ef4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ef4-103">Задает предварительный ключ для подключения между шлюзом Azure VPN и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="d5ef4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5ef4-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5ef4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5ef4-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ef4-106">Командлет **Set-AzureVNetGatewayKey** задает предварительный ключ для подключения между шлюзом виртуальной частной сети Azure и локальным сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="d5ef4-107">Ключ должен совпадать с ключом, настроенным на шлюзе на сайте локальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="d5ef4-108">Если клавиши не совпадают, соединение не устанавливается.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="d5ef4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5ef4-109">EXAMPLES</span></span>

## <span data-ttu-id="d5ef4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5ef4-110">PARAMETERS</span></span>

### <span data-ttu-id="d5ef4-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="d5ef4-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="d5ef4-112">Указывает имя сайта локальной сети, подключенного к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="d5ef4-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5ef4-113">-Profile</span></span>
<span data-ttu-id="d5ef4-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d5ef4-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5ef4-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d5ef4-116">-SharedKey</span></span>
<span data-ttu-id="d5ef4-117">Задает общий ключ, назначаемый VPN-шлюзу.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="d5ef4-118">Значение должно быть буквенно-цифровой строкой длиной не более 128 знаков.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="d5ef4-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d5ef4-119">-VNetName</span></span>
<span data-ttu-id="d5ef4-120">Указывает виртуальную сеть, для которой этот командлет задает общий ключ для подключения.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="d5ef4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ef4-121">CommonParameters</span></span>
<span data-ttu-id="d5ef4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5ef4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ef4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ef4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ef4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5ef4-124">INPUTS</span></span>

## <span data-ttu-id="d5ef4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5ef4-125">OUTPUTS</span></span>

## <span data-ttu-id="d5ef4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5ef4-126">NOTES</span></span>

## <span data-ttu-id="d5ef4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5ef4-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5ef4-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d5ef4-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


