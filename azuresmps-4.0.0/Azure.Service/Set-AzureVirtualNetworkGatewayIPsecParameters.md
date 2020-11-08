---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076412"
---
# <span data-ttu-id="0ab25-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0ab25-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="0ab25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ab25-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab25-103">Задает параметры IPsec для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0ab25-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="0ab25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ab25-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ab25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab25-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab25-106">Командлет **Set-AzureVirtualNetworkGatewayIPsecParameters** задает параметры IPsec для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0ab25-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="0ab25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ab25-107">EXAMPLES</span></span>

## <span data-ttu-id="0ab25-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ab25-108">PARAMETERS</span></span>

### <span data-ttu-id="0ab25-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="0ab25-109">-ConnectedEntityId</span></span>
<span data-ttu-id="0ab25-110">Указывает идентификатор подключенной сущности.</span><span class="sxs-lookup"><span data-stu-id="0ab25-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="0ab25-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="0ab25-111">-EncryptionType</span></span>
<span data-ttu-id="0ab25-112">Указывает тип шифрования для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0ab25-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="0ab25-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ab25-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab25-114">Нешифрование</span><span class="sxs-lookup"><span data-stu-id="0ab25-114">NoEncryption</span></span>
- <span data-ttu-id="0ab25-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="0ab25-115">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab25-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0ab25-116">-GatewayId</span></span>
<span data-ttu-id="0ab25-117">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="0ab25-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0ab25-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="0ab25-118">-PfsGroup</span></span>
<span data-ttu-id="0ab25-119">Задает безопасную группу безопасной пересылки (PFS).</span><span class="sxs-lookup"><span data-stu-id="0ab25-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="0ab25-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ab25-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab25-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="0ab25-121">PFS1</span></span>
- <span data-ttu-id="0ab25-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="0ab25-122">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab25-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="0ab25-123">-Profile</span></span>
<span data-ttu-id="0ab25-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0ab25-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0ab25-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ab25-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ab25-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="0ab25-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="0ab25-127">Задает размер (в килобайтах) сопоставления безопасности (SA).</span><span class="sxs-lookup"><span data-stu-id="0ab25-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab25-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="0ab25-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="0ab25-129">Указывает период (в секундах) сопоставления безопасности.</span><span class="sxs-lookup"><span data-stu-id="0ab25-129">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab25-130">CommonParameters</span></span>
<span data-ttu-id="0ab25-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ab25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab25-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab25-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab25-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ab25-133">INPUTS</span></span>

## <span data-ttu-id="0ab25-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab25-134">OUTPUTS</span></span>

## <span data-ttu-id="0ab25-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ab25-135">NOTES</span></span>

## <span data-ttu-id="0ab25-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ab25-136">RELATED LINKS</span></span>

[<span data-ttu-id="0ab25-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0ab25-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


