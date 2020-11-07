---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913815"
---
# <span data-ttu-id="881c4-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="881c4-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="881c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="881c4-102">SYNOPSIS</span></span>
<span data-ttu-id="881c4-103">Получение сведений о сертификатах отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="881c4-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="881c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="881c4-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="881c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="881c4-105">DESCRIPTION</span></span>
<span data-ttu-id="881c4-106">Командлет **Get-AzureRmVpnClientRevokedCertificate** возвращает сведения о сертификатах отзыва клиента, назначенных шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="881c4-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="881c4-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="881c4-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="881c4-108">**Get-AzureRmVpnClientRevokedCertificate** позволяет вернуть сведения о всех сертификатах отзыва клиента на шлюзе или с помощью параметра *VpnClientRevokedCertificateName* , чтобы получить сведения об одном сертификате.</span><span class="sxs-lookup"><span data-stu-id="881c4-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="881c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="881c4-109">EXAMPLES</span></span>

### <span data-ttu-id="881c4-110">Пример 1: получение сведений обо всех сертификатах отзыва клиента</span><span class="sxs-lookup"><span data-stu-id="881c4-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="881c4-111">Эта команда получает сведения обо всех сертификатах отзыва клиента, связанных с виртуальным сетевым шлюзом с именем ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="881c4-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="881c4-112">Пример 2: получение сведений о конкретных сертификатах отзыва клиента</span><span class="sxs-lookup"><span data-stu-id="881c4-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="881c4-113">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="881c4-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="881c4-114">Тем не менее, в этом случае параметр *VpnClientRevokedCertificateName* используется для ограничения возвращенных данных на конкретный клиентский сертификат: сертификат с именем ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="881c4-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="881c4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="881c4-115">PARAMETERS</span></span>

### <span data-ttu-id="881c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881c4-116">-DefaultProfile</span></span>
<span data-ttu-id="881c4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="881c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="881c4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="881c4-118">-ResourceGroupName</span></span>
<span data-ttu-id="881c4-119">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="881c4-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="881c4-120">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="881c4-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="881c4-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="881c4-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="881c4-122">Указывает имя шлюза виртуальной сети, которому назначены отозванные сведения о сертификате.</span><span class="sxs-lookup"><span data-stu-id="881c4-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="881c4-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="881c4-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="881c4-124">Указывает имя сертификата VPN-клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="881c4-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="881c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881c4-125">CommonParameters</span></span>
<span data-ttu-id="881c4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="881c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881c4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="881c4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881c4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="881c4-128">INPUTS</span></span>

## <span data-ttu-id="881c4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="881c4-129">OUTPUTS</span></span>

###  
<span data-ttu-id="881c4-130">Функция **Get-AzureRmVpnClientRevokedCertificate** возвращает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="881c4-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="881c4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="881c4-131">NOTES</span></span>

## <span data-ttu-id="881c4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="881c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="881c4-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="881c4-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="881c4-134">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="881c4-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="881c4-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="881c4-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


