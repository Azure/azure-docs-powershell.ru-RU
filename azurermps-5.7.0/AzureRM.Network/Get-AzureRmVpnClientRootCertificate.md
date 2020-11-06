---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 3215d80d006d3a2dd1a7e4575c7033ba7d85c0ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564764"
---
# <span data-ttu-id="08728-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="08728-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="08728-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08728-102">SYNOPSIS</span></span>
<span data-ttu-id="08728-103">Получение сведений о корневых сертификатах VPN.</span><span class="sxs-lookup"><span data-stu-id="08728-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08728-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08728-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08728-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08728-105">DESCRIPTION</span></span>
<span data-ttu-id="08728-106">Командлет **Get-AzureRmVpnClientRootCertificate** возвращает сведения о корневых сертификатах, назначенных шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="08728-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="08728-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="08728-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="08728-108">По умолчанию **Get-AzureRmVpnClientRootCertificate** возвращает сведения о всех корневых сертификатах, назначенных шлюзу.</span><span class="sxs-lookup"><span data-stu-id="08728-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="08728-109">(Шлюзы могут иметь более одного корневого сертификата.) Однако, включив параметр **VpnClientRootCertificateName** , вы можете ограничить возвращаемые данные определенным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="08728-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="08728-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08728-110">EXAMPLES</span></span>

### <span data-ttu-id="08728-111">Пример 1: получение сведений обо всех корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="08728-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="08728-112">Эта команда получает сведения обо всех корневых сертификатах, назначенных виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="08728-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="08728-113">Пример 2: получение сведений о конкретных корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="08728-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="08728-114">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="08728-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="08728-115">Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемые данные определенным корневым сертификатом: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="08728-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="08728-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08728-116">PARAMETERS</span></span>

### <span data-ttu-id="08728-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08728-117">-DefaultProfile</span></span>
<span data-ttu-id="08728-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08728-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08728-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08728-119">-ResourceGroupName</span></span>
<span data-ttu-id="08728-120">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="08728-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="08728-121">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="08728-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="08728-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="08728-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="08728-123">Указывает имя шлюза виртуальной сети, на котором назначен корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="08728-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="08728-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="08728-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="08728-125">Указывает имя корневого сертификата клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="08728-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08728-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08728-126">CommonParameters</span></span>
<span data-ttu-id="08728-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08728-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08728-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08728-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08728-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08728-129">INPUTS</span></span>

### <span data-ttu-id="08728-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="08728-130">None</span></span>
<span data-ttu-id="08728-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="08728-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08728-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08728-132">OUTPUTS</span></span>

###  
<span data-ttu-id="08728-133">**Get-AzureRmVpnClientRootCertificate** получает экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="08728-133">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="08728-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="08728-134">NOTES</span></span>

## <span data-ttu-id="08728-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08728-135">RELATED LINKS</span></span>

[<span data-ttu-id="08728-136">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="08728-136">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="08728-137">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="08728-137">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="08728-138">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="08728-138">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


