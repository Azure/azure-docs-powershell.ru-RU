---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 9f20b0540481c40326bc3656e3f65534c22f9b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562875"
---
# <span data-ttu-id="c8edc-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8edc-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c8edc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8edc-102">SYNOPSIS</span></span>
<span data-ttu-id="c8edc-103">Создание нового сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="c8edc-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8edc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8edc-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8edc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8edc-105">DESCRIPTION</span></span>
<span data-ttu-id="c8edc-106">Командлет **New-AzureRmVpnClientRevokedCertificate** создает новый сертификат отзыва для клиента виртуальной частной сети (VPN) для использования на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c8edc-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="c8edc-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c8edc-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="c8edc-108">Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="c8edc-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="c8edc-109">Вместо этого сертификат, созданный с помощью **New-AzureRmVpnClientRevokedCertificate** , используется вместе с командлетом New-AzureRmVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="c8edc-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="c8edc-110">Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c8edc-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="c8edc-111">Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="c8edc-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="c8edc-112">Например, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="c8edc-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="c8edc-113">Дополнительные сведения можно найти в документации по командлету New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c8edc-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="c8edc-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8edc-114">EXAMPLES</span></span>

### <span data-ttu-id="c8edc-115">Пример 1: создание нового сертификата, отозванного клиентом</span><span class="sxs-lookup"><span data-stu-id="c8edc-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="c8edc-116">Эта команда создает новый сертификат, отозванный клиентом, и сохраняет объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="c8edc-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="c8edc-117">Эта переменная может затем использоваться командлетом **New-AzureRmVirtualNetworkGateway** для добавления сертификата в новый шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c8edc-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="c8edc-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8edc-118">PARAMETERS</span></span>

### <span data-ttu-id="c8edc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8edc-119">-DefaultProfile</span></span>
<span data-ttu-id="c8edc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8edc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8edc-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8edc-121">-Name</span></span>
<span data-ttu-id="c8edc-122">Указывает уникальное имя для нового сертификата отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="c8edc-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="c8edc-123">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="c8edc-123">-Thumbprint</span></span>
<span data-ttu-id="c8edc-124">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="c8edc-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="c8edc-125">Вы можете вернуть отпечаток для сертификатов с помощью команды Windows PowerShell, как показано ниже: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="c8edc-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="c8edc-126">Предыдущая команда возвращает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c8edc-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="c8edc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8edc-127">CommonParameters</span></span>
<span data-ttu-id="c8edc-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8edc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8edc-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8edc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8edc-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8edc-130">INPUTS</span></span>

### <span data-ttu-id="c8edc-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="c8edc-131">None</span></span>

## <span data-ttu-id="c8edc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8edc-132">OUTPUTS</span></span>

### <span data-ttu-id="c8edc-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8edc-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="c8edc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8edc-134">NOTES</span></span>

## <span data-ttu-id="c8edc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8edc-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8edc-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8edc-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c8edc-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8edc-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="c8edc-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="c8edc-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


