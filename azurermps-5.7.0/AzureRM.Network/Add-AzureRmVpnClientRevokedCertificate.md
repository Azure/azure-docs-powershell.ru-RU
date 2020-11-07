---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8f1c81dbfb3d8c42b359464ce33a0053fdc25143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734440"
---
# <span data-ttu-id="d7cd0-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d7cd0-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d7cd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cd0-103">Добавление сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7cd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7cd0-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7cd0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="d7cd0-106">Командлет **Add-AzureRmVpnClientRevokedCertificate** назначает сертификат отзыва клиента шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="d7cd0-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="d7cd0-108">Для использования этого командлета необходимо указать как имя сертификата, так и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="d7cd0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="d7cd0-110">Пример 1: Добавление нового сертификата отзыва клиента в шлюз виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d7cd0-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="d7cd0-111">Эта команда добавляет новый сертификат отзыва клиента на шлюз виртуальной сети с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="d7cd0-112">Чтобы добавить сертификат, необходимо указать имя сертификата и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="d7cd0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7cd0-113">PARAMETERS</span></span>

### <span data-ttu-id="d7cd0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cd0-114">-DefaultProfile</span></span>
<span data-ttu-id="d7cd0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7cd0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cd0-116">-ResourceGroupName</span></span>
<span data-ttu-id="d7cd0-117">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="d7cd0-118">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="d7cd0-119">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="d7cd0-119">-Thumbprint</span></span>
<span data-ttu-id="d7cd0-120">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="d7cd0-121">Например:</span><span class="sxs-lookup"><span data-stu-id="d7cd0-121">For example:</span></span>

<span data-ttu-id="d7cd0-122">-Отпечаток "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="d7cd0-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="d7cd0-123">Вы можете получить сведения об отпечатном сертификате с помощью команды Windows PowerShell, как показано `Get-ChildItem -Path Cert:\LocalMachine\Root` ниже.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="d7cd0-124">Предыдущая команда получает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="d7cd0-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d7cd0-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d7cd0-126">Указывает имя шлюза виртуальной сети, на который нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="d7cd0-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="d7cd0-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="d7cd0-128">Указывает имя добавляемого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="d7cd0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cd0-129">CommonParameters</span></span>
<span data-ttu-id="d7cd0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cd0-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7cd0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cd0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7cd0-132">INPUTS</span></span>

### <span data-ttu-id="d7cd0-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="d7cd0-133">None</span></span>
<span data-ttu-id="d7cd0-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d7cd0-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7cd0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7cd0-135">OUTPUTS</span></span>

### <span data-ttu-id="d7cd0-136">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d7cd0-136">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d7cd0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7cd0-137">NOTES</span></span>

## <span data-ttu-id="d7cd0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7cd0-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7cd0-139">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d7cd0-139">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="d7cd0-140">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d7cd0-140">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="d7cd0-141">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d7cd0-141">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


