---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076036"
---
# <span data-ttu-id="136f7-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="136f7-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="136f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="136f7-102">SYNOPSIS</span></span>
<span data-ttu-id="136f7-103">Задает параметры IPsec для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="136f7-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="136f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="136f7-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="136f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="136f7-105">DESCRIPTION</span></span>
<span data-ttu-id="136f7-106">Командлет **Set-AzureVNetGatewayIPsecParameters** задает параметры безопасности IP (IPSec) и IKE (Internet Key Exchange) для подключения между шлюзом виртуальной сети и сайтом локальной сети.</span><span class="sxs-lookup"><span data-stu-id="136f7-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="136f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="136f7-107">EXAMPLES</span></span>

## <span data-ttu-id="136f7-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="136f7-108">PARAMETERS</span></span>

### <span data-ttu-id="136f7-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="136f7-109">-EncryptionType</span></span>
<span data-ttu-id="136f7-110">Указывает тип шифрования для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="136f7-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="136f7-111">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="136f7-111">Valid values are:</span></span> 

- <span data-ttu-id="136f7-112">Нешифрование</span><span class="sxs-lookup"><span data-stu-id="136f7-112">NoEncryption</span></span> 
- <span data-ttu-id="136f7-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="136f7-113">RequireEncryption</span></span>

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

### <span data-ttu-id="136f7-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="136f7-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="136f7-115">Указывает имя подключения к сайту локальной сети, на котором этот командлет настраивает параметры IPsec и IKE.</span><span class="sxs-lookup"><span data-stu-id="136f7-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="136f7-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="136f7-116">-PfsGroup</span></span>
<span data-ttu-id="136f7-117">Задает безопасную группу безопасной пересылки (PFS).</span><span class="sxs-lookup"><span data-stu-id="136f7-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="136f7-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="136f7-118">Valid values are:</span></span> 

- <span data-ttu-id="136f7-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="136f7-119">PFS1</span></span> 
- <span data-ttu-id="136f7-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="136f7-120">None</span></span>

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

### <span data-ttu-id="136f7-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="136f7-121">-Profile</span></span>
<span data-ttu-id="136f7-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="136f7-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="136f7-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="136f7-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="136f7-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="136f7-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="136f7-125">Задает размер (в килобайтах) сопоставления безопасности (SA).</span><span class="sxs-lookup"><span data-stu-id="136f7-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="136f7-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="136f7-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="136f7-127">Указывает период (в секундах) сопоставления безопасности.</span><span class="sxs-lookup"><span data-stu-id="136f7-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="136f7-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="136f7-128">-VNetName</span></span>
<span data-ttu-id="136f7-129">Указывает виртуальную сеть, для которой этот командлет задает параметры IPsec для подключения.</span><span class="sxs-lookup"><span data-stu-id="136f7-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="136f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136f7-130">CommonParameters</span></span>
<span data-ttu-id="136f7-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="136f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136f7-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136f7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136f7-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="136f7-133">INPUTS</span></span>

## <span data-ttu-id="136f7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="136f7-134">OUTPUTS</span></span>

## <span data-ttu-id="136f7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="136f7-135">NOTES</span></span>

## <span data-ttu-id="136f7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="136f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="136f7-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="136f7-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


