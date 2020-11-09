---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317009"
---
# <span data-ttu-id="6018a-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6018a-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6018a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6018a-102">SYNOPSIS</span></span>
<span data-ttu-id="6018a-103">Создание нового сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="6018a-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="6018a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6018a-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6018a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6018a-105">DESCRIPTION</span></span>
<span data-ttu-id="6018a-106">Командлет **New-AzVpnClientRevokedCertificate** создает новый сертификат отзыва для клиента виртуальной частной сети (VPN) для использования на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6018a-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="6018a-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6018a-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="6018a-108">Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="6018a-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="6018a-109">Вместо этого сертификат, созданный с помощью **New-AzVpnClientRevokedCertificate** , используется вместе с командлетом New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="6018a-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="6018a-110">Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6018a-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="6018a-111">Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="6018a-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="6018a-112">Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="6018a-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="6018a-113">Дополнительные сведения можно найти в документации по командлету New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="6018a-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="6018a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6018a-114">EXAMPLES</span></span>

### <span data-ttu-id="6018a-115">Пример 1: создание нового сертификата, отозванного клиентом</span><span class="sxs-lookup"><span data-stu-id="6018a-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="6018a-116">Эта команда создает новый сертификат, отозванный клиентом, и сохраняет объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6018a-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="6018a-117">Эта переменная может затем использоваться командлетом **New-AzVirtualNetworkGateway** для добавления сертификата в новый шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6018a-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="6018a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6018a-118">PARAMETERS</span></span>

### <span data-ttu-id="6018a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6018a-119">-DefaultProfile</span></span>
<span data-ttu-id="6018a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6018a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6018a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6018a-121">-Name</span></span>
<span data-ttu-id="6018a-122">Указывает уникальное имя для нового сертификата отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="6018a-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="6018a-123">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="6018a-123">-Thumbprint</span></span>
<span data-ttu-id="6018a-124">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="6018a-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="6018a-125">Вы можете вернуть отпечаток для сертификатов с помощью команды Windows PowerShell, как показано ниже: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="6018a-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="6018a-126">Предыдущая команда возвращает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6018a-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="6018a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6018a-127">CommonParameters</span></span>
<span data-ttu-id="6018a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6018a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6018a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6018a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6018a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6018a-130">INPUTS</span></span>

### <span data-ttu-id="6018a-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="6018a-131">None</span></span>

## <span data-ttu-id="6018a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6018a-132">OUTPUTS</span></span>

### <span data-ttu-id="6018a-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6018a-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6018a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6018a-134">NOTES</span></span>

## <span data-ttu-id="6018a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6018a-135">RELATED LINKS</span></span>

[<span data-ttu-id="6018a-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6018a-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6018a-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6018a-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6018a-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6018a-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


