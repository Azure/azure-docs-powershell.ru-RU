---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964099"
---
# <span data-ttu-id="7d68b-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7d68b-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7d68b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d68b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d68b-103">Создание нового сертификата vpn-отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="7d68b-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="7d68b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d68b-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d68b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d68b-105">DESCRIPTION</span></span>
<span data-ttu-id="7d68b-106">Для использования виртуального сетевого шлюза с помощью нового сертификата отзыва клиента в **AzVpnClientRevokedCertificate** создается новый сертификат отзыва клиента виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="7d68b-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="7d68b-107">Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7d68b-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="7d68b-108">Этот cmdlet создает автономный сертификат, который не назначен виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="7d68b-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="7d68b-109">Вместо этого сертификат, созданный **new-AzVpnClientRevokedCertificate,** используется в сочетании с New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="7d68b-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="7d68b-110">Предположим, например, что вы создали новый сертификат и сохраняете его в переменной с $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7d68b-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="7d68b-111">Этот объект сертификата можно использовать при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="7d68b-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="7d68b-112">Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="7d68b-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="7d68b-113">Дополнительные сведения см. в документации New-AzVirtualNetworkGateway управления проектами.</span><span class="sxs-lookup"><span data-stu-id="7d68b-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="7d68b-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d68b-114">EXAMPLES</span></span>

### <span data-ttu-id="7d68b-115">Пример 1. Создание отозванного сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="7d68b-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="7d68b-116">Эта команда создает новый отозванный клиентом сертификат и сохраняет объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7d68b-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="7d68b-117">Затем эту переменную можно использовать **командлетом New-AzVirtualNetworkGateway** для добавления сертификата к новому виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="7d68b-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="7d68b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d68b-118">PARAMETERS</span></span>

### <span data-ttu-id="7d68b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d68b-119">-DefaultProfile</span></span>
<span data-ttu-id="7d68b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d68b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d68b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d68b-121">-Name</span></span>
<span data-ttu-id="7d68b-122">Указывает уникальное имя для нового сертификата отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="7d68b-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d68b-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="7d68b-123">-Thumbprint</span></span>
<span data-ttu-id="7d68b-124">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="7d68b-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="7d68b-125">Получить сведения о эскизах для сертификатов можно с помощью команды Windows PowerShell примерно так: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="7d68b-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="7d68b-126">Предшествуя команда возвращает сведения для всех сертификатов локального компьютера, найденных в хранилище корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7d68b-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d68b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d68b-127">CommonParameters</span></span>
<span data-ttu-id="7d68b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d68b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d68b-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d68b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d68b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d68b-130">INPUTS</span></span>

### <span data-ttu-id="7d68b-131">Нет</span><span class="sxs-lookup"><span data-stu-id="7d68b-131">None</span></span>

## <span data-ttu-id="7d68b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d68b-132">OUTPUTS</span></span>

### <span data-ttu-id="7d68b-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7d68b-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7d68b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d68b-134">NOTES</span></span>

## <span data-ttu-id="7d68b-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d68b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d68b-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7d68b-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="7d68b-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7d68b-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="7d68b-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7d68b-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


