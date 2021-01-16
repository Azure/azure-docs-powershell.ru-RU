---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397380"
---
# <span data-ttu-id="9c4ec-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c4ec-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="9c4ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4ec-103">Сведения о корневых сертификатах VPN.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="9c4ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c4ec-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c4ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c4ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9c4ec-106">Cmdlet **Get-AzVpnClientRootCertificate** возвращает сведения о корневых сертификатах, которые назначены виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="9c4ec-107">Корневые сертификаты — это сертификаты X.509, которые определяют корневой сертификат сертификации: все остальные сертификаты, используемые на шлюзе, доверять корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="9c4ec-108">По умолчанию **Get-AzVpnClientRootCertificate** возвращает сведения обо всех корневых сертификатах, которые назначены шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="9c4ec-109">(Шлюзы могут иметь несколько корневых сертификатов.) Однако включив параметр **VpnClientRootCertificateName,** вы можете ограничить возвращаемую информацию определенным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="9c4ec-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c4ec-110">EXAMPLES</span></span>

### <span data-ttu-id="9c4ec-111">Пример 1. Сведения обо всех корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="9c4ec-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="9c4ec-112">Эта команда получает сведения обо всех корневых сертификатах, которые назначены виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="9c4ec-113">Пример 2. Просмотр сведений о конкретных корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="9c4ec-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="9c4ec-114">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="9c4ec-115">Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемую информацию определенным корневым сертификатом: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="9c4ec-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c4ec-116">PARAMETERS</span></span>

### <span data-ttu-id="9c4ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4ec-117">-DefaultProfile</span></span>
<span data-ttu-id="9c4ec-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4ec-119">-ResourceGroupName</span></span>
<span data-ttu-id="9c4ec-120">Имя группы ресурсов, назначенной виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="9c4ec-121">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ec-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9c4ec-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9c4ec-123">Указывает имя виртуального сетевого шлюза, корневого сертификата которого назначен.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ec-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="9c4ec-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="9c4ec-125">Указывает имя корневого сертификата клиента, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4ec-126">CommonParameters</span></span>
<span data-ttu-id="9c4ec-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4ec-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c4ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4ec-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c4ec-129">INPUTS</span></span>

### <span data-ttu-id="9c4ec-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9c4ec-130">System.String</span></span>

## <span data-ttu-id="9c4ec-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c4ec-131">OUTPUTS</span></span>

### <span data-ttu-id="9c4ec-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c4ec-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="9c4ec-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c4ec-133">NOTES</span></span>

## <span data-ttu-id="9c4ec-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c4ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="9c4ec-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c4ec-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="9c4ec-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c4ec-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="9c4ec-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9c4ec-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


