---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248820"
---
# <span data-ttu-id="efaf1-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="efaf1-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="efaf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="efaf1-103">Удаление сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="efaf1-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="efaf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efaf1-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efaf1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="efaf1-106">Командлет **Revocation-AzVpnClientRevokedCertificate** Удаляет сертификат отзыва клиента из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="efaf1-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="efaf1-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="efaf1-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="efaf1-108">Если вы удалите клиентские компьютеры сертификата отзыва клиента, вы можете использовать ранее заблокированный сертификат, чтобы сделать виртуальную частную сеть (VPN).</span><span class="sxs-lookup"><span data-stu-id="efaf1-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="efaf1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efaf1-109">EXAMPLES</span></span>

### <span data-ttu-id="efaf1-110">Пример 1: Удаление сертификата отзыва клиента из шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="efaf1-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="efaf1-111">Эта команда удаляет сертификат отзыва клиента из шлюза виртуальной сети с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="efaf1-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="efaf1-112">Для удаления сертификата отзыва клиента необходимо указать как имя сертификата, так и отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="efaf1-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="efaf1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efaf1-113">PARAMETERS</span></span>

### <span data-ttu-id="efaf1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efaf1-114">-DefaultProfile</span></span>
<span data-ttu-id="efaf1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efaf1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efaf1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efaf1-116">-ResourceGroupName</span></span>
<span data-ttu-id="efaf1-117">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="efaf1-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="efaf1-118">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="efaf1-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="efaf1-119">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="efaf1-119">-Thumbprint</span></span>
<span data-ttu-id="efaf1-120">Указывает уникальный идентификатор удаляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="efaf1-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="efaf1-121">Вы можете вернуть отпечаток для сертификатов с помощью команды Windows PowerShell, как показано ниже: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="efaf1-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="efaf1-122">Предыдущая команда возвращает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="efaf1-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="efaf1-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="efaf1-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="efaf1-124">Указывает имя шлюза виртуальной сети, которому назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="efaf1-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="efaf1-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="efaf1-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="efaf1-126">Указывает имя удаляемого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="efaf1-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="efaf1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efaf1-127">CommonParameters</span></span>
<span data-ttu-id="efaf1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efaf1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efaf1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efaf1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efaf1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efaf1-130">INPUTS</span></span>

### <span data-ttu-id="efaf1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="efaf1-131">System.String</span></span>

## <span data-ttu-id="efaf1-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efaf1-132">OUTPUTS</span></span>

### <span data-ttu-id="efaf1-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efaf1-133">System.Boolean</span></span>

## <span data-ttu-id="efaf1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="efaf1-134">NOTES</span></span>

## <span data-ttu-id="efaf1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efaf1-135">RELATED LINKS</span></span>

[<span data-ttu-id="efaf1-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="efaf1-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="efaf1-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="efaf1-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="efaf1-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="efaf1-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

