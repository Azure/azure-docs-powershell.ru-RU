---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406231"
---
# <span data-ttu-id="9b0e8-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9b0e8-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9b0e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0e8-103">Создание нового сертификата vpn-отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="9b0e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b0e8-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b0e8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="9b0e8-106">Для использования виртуального сетевого шлюза с помощью нового сертификата отзыва клиента в **AzVpnClientRevokedCertificate** создается новый сертификат отзыва клиента виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="9b0e8-107">Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="9b0e8-108">Этот cmdlet создает автономный сертификат, который не назначен виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="9b0e8-109">Вместо этого сертификат, созданный **new-AzVpnClientRevokedCertificate,** используется в сочетании с New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="9b0e8-110">Предположим, например, что вы создали новый сертификат и храните его в переменной с $Certificate.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="9b0e8-111">Этот объект сертификата можно использовать при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="9b0e8-112">Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="9b0e8-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="9b0e8-113">Дополнительные сведения см. в документации New-AzVirtualNetworkGateway управления проектами.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="9b0e8-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-114">EXAMPLES</span></span>

### <span data-ttu-id="9b0e8-115">Пример 1. Создание отозванного сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="9b0e8-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9b0e8-116">Эта команда создает новый отозванный клиентом сертификат и сохраняет объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="9b0e8-117">Затем с помощью **командлета New-AzVirtualNetworkGateway** можно добавить сертификат к новому виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="9b0e8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b0e8-118">PARAMETERS</span></span>

### <span data-ttu-id="9b0e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0e8-119">-DefaultProfile</span></span>
<span data-ttu-id="9b0e8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b0e8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b0e8-121">-Name</span></span>
<span data-ttu-id="9b0e8-122">Указывает уникальное имя для нового сертификата отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="9b0e8-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="9b0e8-123">-Thumbprint</span></span>
<span data-ttu-id="9b0e8-124">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="9b0e8-125">Получить сведения о эскизах для сертификатов можно с помощью команды Windows PowerShell примерно так: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="9b0e8-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="9b0e8-126">Предшествуя команда возвращает сведения для всех сертификатов локального компьютера, найденных в хранилище корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="9b0e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0e8-127">CommonParameters</span></span>
<span data-ttu-id="9b0e8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0e8-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b0e8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0e8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b0e8-130">INPUTS</span></span>

### <span data-ttu-id="9b0e8-131">Нет</span><span class="sxs-lookup"><span data-stu-id="9b0e8-131">None</span></span>

## <span data-ttu-id="9b0e8-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b0e8-132">OUTPUTS</span></span>

### <span data-ttu-id="9b0e8-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9b0e8-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9b0e8-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-134">NOTES</span></span>

## <span data-ttu-id="9b0e8-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b0e8-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9b0e8-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9b0e8-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9b0e8-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9b0e8-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9b0e8-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


