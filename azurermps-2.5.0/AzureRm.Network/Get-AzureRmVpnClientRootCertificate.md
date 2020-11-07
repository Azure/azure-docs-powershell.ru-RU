---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913813"
---
# <span data-ttu-id="9cdf5-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9cdf5-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="9cdf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdf5-103">Получение сведений о корневых сертификатах VPN.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cdf5-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cdf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cdf5-105">DESCRIPTION</span></span>
<span data-ttu-id="9cdf5-106">Командлет **Get-AzureRmVpnClientRootCertificate** возвращает сведения о корневых сертификатах, назначенных шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="9cdf5-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="9cdf5-108">По умолчанию **Get-AzureRmVpnClientRootCertificate** возвращает сведения о всех корневых сертификатах, назначенных шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="9cdf5-109">(Шлюзы могут иметь более одного корневого сертификата.) Однако, включив параметр **VpnClientRootCertificateName** , вы можете ограничить возвращаемые данные определенным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="9cdf5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cdf5-110">EXAMPLES</span></span>

### <span data-ttu-id="9cdf5-111">Пример 1: получение сведений обо всех корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="9cdf5-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="9cdf5-112">Эта команда получает сведения обо всех корневых сертификатах, назначенных виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="9cdf5-113">Пример 2: получение сведений о конкретных корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="9cdf5-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="9cdf5-114">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="9cdf5-115">Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемые данные определенным корневым сертификатом: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="9cdf5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cdf5-116">PARAMETERS</span></span>

### <span data-ttu-id="9cdf5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdf5-117">-DefaultProfile</span></span>
<span data-ttu-id="9cdf5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cdf5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdf5-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cdf5-120">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="9cdf5-121">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9cdf5-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9cdf5-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9cdf5-123">Указывает имя шлюза виртуальной сети, на котором назначен корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="9cdf5-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="9cdf5-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="9cdf5-125">Указывает имя корневого сертификата клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9cdf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdf5-126">CommonParameters</span></span>
<span data-ttu-id="9cdf5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cdf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdf5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdf5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdf5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cdf5-129">INPUTS</span></span>

## <span data-ttu-id="9cdf5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cdf5-130">OUTPUTS</span></span>

###  
<span data-ttu-id="9cdf5-131">**Get-AzureRmVpnClientRootCertificate** получает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="9cdf5-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="9cdf5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cdf5-132">NOTES</span></span>

## <span data-ttu-id="9cdf5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cdf5-133">RELATED LINKS</span></span>

[<span data-ttu-id="9cdf5-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9cdf5-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="9cdf5-135">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9cdf5-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="9cdf5-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9cdf5-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


