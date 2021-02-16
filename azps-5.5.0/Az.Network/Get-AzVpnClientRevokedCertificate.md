---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221172"
---
# <span data-ttu-id="c8459-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8459-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c8459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8459-102">SYNOPSIS</span></span>
<span data-ttu-id="c8459-103">Сведения о сертификатах отзыва VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="c8459-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="c8459-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8459-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8459-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8459-105">DESCRIPTION</span></span>
<span data-ttu-id="c8459-106">Cmdlet **Get-AzVpnClientRevokedCertificate** возвращает сведения о сертификатах отзыва клиента, которые назначены виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="c8459-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="c8459-107">Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c8459-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="c8459-108">**Get-AzVpnClientRevokedCertificate** позволяет вернуть сведения обо всех сертификатах отзыва клиента на шлюзе или с помощью параметра *VpnClientRevokedCertificateName,* чтобы получить сведения об одном сертификате.</span><span class="sxs-lookup"><span data-stu-id="c8459-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="c8459-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8459-109">EXAMPLES</span></span>

### <span data-ttu-id="c8459-110">Пример 1. Просмотр сведений обо всех сертификатах отзыва клиента</span><span class="sxs-lookup"><span data-stu-id="c8459-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c8459-111">Эта команда получает сведения обо всех сертификатах отзыва клиента, связанных с виртуальным сетевым шлюзом ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c8459-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="c8459-112">Пример 2. Просмотр сведений о конкретных сертификатах отзыва клиента</span><span class="sxs-lookup"><span data-stu-id="c8459-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="c8459-113">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="c8459-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="c8459-114">Однако в этом случае параметр *VpnClientRevokedCertificateName* используется для ограничения возвращаемого данных на определенный сертификат, отозванный клиентом: сертификат с именем ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="c8459-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="c8459-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8459-115">PARAMETERS</span></span>

### <span data-ttu-id="c8459-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8459-116">-DefaultProfile</span></span>
<span data-ttu-id="c8459-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8459-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8459-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8459-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8459-119">Имя группы ресурсов, назначенной виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="c8459-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="c8459-120">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="c8459-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="c8459-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c8459-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c8459-122">Указывает имя виртуального сетевого шлюза, для которого назначены данные отозванного сертификата.</span><span class="sxs-lookup"><span data-stu-id="c8459-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="c8459-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="c8459-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="c8459-124">Указывает имя сертификата клиента VPN, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8459-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8459-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8459-125">CommonParameters</span></span>
<span data-ttu-id="c8459-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8459-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8459-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8459-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8459-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8459-128">INPUTS</span></span>

### <span data-ttu-id="c8459-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c8459-129">System.String</span></span>

## <span data-ttu-id="c8459-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8459-130">OUTPUTS</span></span>

### <span data-ttu-id="c8459-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8459-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c8459-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8459-132">NOTES</span></span>

## <span data-ttu-id="c8459-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8459-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8459-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8459-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c8459-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8459-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="c8459-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8459-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


