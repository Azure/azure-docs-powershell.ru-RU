---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c770bc2bb7c3fde9475ee844e12b8ed8c457dd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734346"
---
# <span data-ttu-id="fd28c-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fd28c-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="fd28c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd28c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd28c-103">Добавление сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="fd28c-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd28c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd28c-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd28c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd28c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd28c-106">Командлет **Add-AzureRmVpnClientRevokedCertificate** назначает сертификат отзыва клиента шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd28c-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="fd28c-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="fd28c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="fd28c-108">Для использования этого командлета необходимо указать как имя сертификата, так и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="fd28c-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="fd28c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd28c-109">EXAMPLES</span></span>

### <span data-ttu-id="fd28c-110">Пример 1: Добавление нового сертификата отзыва клиента в шлюз виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="fd28c-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="fd28c-111">Эта команда добавляет новый сертификат отзыва клиента на шлюз виртуальной сети с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="fd28c-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="fd28c-112">Чтобы добавить сертификат, необходимо указать имя сертификата и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="fd28c-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="fd28c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd28c-113">PARAMETERS</span></span>

### <span data-ttu-id="fd28c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd28c-114">-DefaultProfile</span></span>
<span data-ttu-id="fd28c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd28c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd28c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd28c-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd28c-117">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd28c-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="fd28c-118">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="fd28c-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="fd28c-119">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="fd28c-119">-Thumbprint</span></span>
<span data-ttu-id="fd28c-120">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="fd28c-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="fd28c-121">Например:-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" можно получить сведения об отпечатных сертификатах с помощью команды Windows PowerShell, как показано `Get-ChildItem -Path Cert:\LocalMachine\Root` ниже.</span><span class="sxs-lookup"><span data-stu-id="fd28c-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="fd28c-122">Предыдущая команда получает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fd28c-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="fd28c-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fd28c-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fd28c-124">Указывает имя шлюза виртуальной сети, на который нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="fd28c-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="fd28c-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="fd28c-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="fd28c-126">Указывает имя добавляемого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="fd28c-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd28c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd28c-127">CommonParameters</span></span>
<span data-ttu-id="fd28c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd28c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd28c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd28c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd28c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd28c-130">INPUTS</span></span>

### <span data-ttu-id="fd28c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fd28c-131">System.String</span></span>

## <span data-ttu-id="fd28c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd28c-132">OUTPUTS</span></span>

### <span data-ttu-id="fd28c-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fd28c-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="fd28c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd28c-134">NOTES</span></span>

## <span data-ttu-id="fd28c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd28c-135">RELATED LINKS</span></span>

[<span data-ttu-id="fd28c-136">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fd28c-136">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fd28c-137">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fd28c-137">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fd28c-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fd28c-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


