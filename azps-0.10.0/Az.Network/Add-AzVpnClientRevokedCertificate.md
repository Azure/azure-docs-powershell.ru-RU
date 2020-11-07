---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 384d5b88ce9a52ad5f68c009c7b610610c695ce2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910111"
---
# <span data-ttu-id="bcca3-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcca3-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bcca3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcca3-102">SYNOPSIS</span></span>
<span data-ttu-id="bcca3-103">Добавление сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="bcca3-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="bcca3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcca3-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcca3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcca3-105">DESCRIPTION</span></span>
<span data-ttu-id="bcca3-106">Командлет **Add-AzVpnClientRevokedCertificate** назначает сертификат отзыва клиента шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bcca3-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="bcca3-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bcca3-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="bcca3-108">Для использования этого командлета необходимо указать как имя сертификата, так и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="bcca3-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="bcca3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcca3-109">EXAMPLES</span></span>

### <span data-ttu-id="bcca3-110">Пример 1: Добавление нового сертификата отзыва клиента в шлюз виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="bcca3-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="bcca3-111">Эта команда добавляет новый сертификат отзыва клиента на шлюз виртуальной сети с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="bcca3-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="bcca3-112">Чтобы добавить сертификат, необходимо указать имя сертификата и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="bcca3-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="bcca3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcca3-113">PARAMETERS</span></span>

### <span data-ttu-id="bcca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcca3-114">-DefaultProfile</span></span>
<span data-ttu-id="bcca3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcca3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcca3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcca3-116">-ResourceGroupName</span></span>
<span data-ttu-id="bcca3-117">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bcca3-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="bcca3-118">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="bcca3-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bcca3-119">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="bcca3-119">-Thumbprint</span></span>
<span data-ttu-id="bcca3-120">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="bcca3-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="bcca3-121">Например:</span><span class="sxs-lookup"><span data-stu-id="bcca3-121">For example:</span></span>

<span data-ttu-id="bcca3-122">-Отпечаток "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="bcca3-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="bcca3-123">Вы можете получить сведения об отпечатном сертификате с помощью команды Windows PowerShell, как показано `Get-ChildItem -Path Cert:\LocalMachine\Root` ниже.</span><span class="sxs-lookup"><span data-stu-id="bcca3-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="bcca3-124">Предыдущая команда получает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="bcca3-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcca3-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bcca3-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bcca3-126">Указывает имя шлюза виртуальной сети, на который нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="bcca3-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="bcca3-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="bcca3-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="bcca3-128">Указывает имя добавляемого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="bcca3-128">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcca3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcca3-129">CommonParameters</span></span>
<span data-ttu-id="bcca3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcca3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcca3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcca3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcca3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcca3-132">INPUTS</span></span>

## <span data-ttu-id="bcca3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcca3-133">OUTPUTS</span></span>

### <span data-ttu-id="bcca3-134">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcca3-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bcca3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcca3-135">NOTES</span></span>

## <span data-ttu-id="bcca3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcca3-136">RELATED LINKS</span></span>

[<span data-ttu-id="bcca3-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcca3-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bcca3-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcca3-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bcca3-139">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bcca3-139">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


