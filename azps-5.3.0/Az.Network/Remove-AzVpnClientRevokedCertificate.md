---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425172"
---
# <span data-ttu-id="3a4b8-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3a4b8-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="3a4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4b8-103">Удаляет сертификат отзыва клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="3a4b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a4b8-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a4b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4b8-106">При **этом из виртуального** сетевого шлюза удаляется сертификат отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="3a4b8-107">Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="3a4b8-108">После удаления клиентского сертификата отзыва клиента можно использовать ранее заблокированный сертификат для подключения к виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="3a4b8-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="3a4b8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a4b8-109">EXAMPLES</span></span>

### <span data-ttu-id="3a4b8-110">Пример 1. Удаление сертификата отзыва клиента из виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="3a4b8-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="3a4b8-111">Эта команда удаляет сертификат отзыва клиента для виртуального сетевого шлюза с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="3a4b8-112">Чтобы удалить сертификат отзыва клиента, необходимо указать как его имя, так и его эскиз.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="3a4b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-113">PARAMETERS</span></span>

### <span data-ttu-id="3a4b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4b8-114">-DefaultProfile</span></span>
<span data-ttu-id="3a4b8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a4b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="3a4b8-117">Указывает имя группы ресурсов, которая назначена виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="3a4b8-118">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3a4b8-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="3a4b8-119">-Thumbprint</span></span>
<span data-ttu-id="3a4b8-120">Указывает уникальный идентификатор удаляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="3a4b8-121">Получить данные от руки для сертификатов можно с помощью команды Windows PowerShell примерно так: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="3a4b8-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="3a4b8-122">Предшествуя команда возвращает сведения для всех сертификатов локального компьютера, найденных в хранилище корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="3a4b8-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3a4b8-124">Указывает имя виртуального сетевого шлюза, назначенного сертификату.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="3a4b8-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="3a4b8-126">Указывает имя удаляемого сертификата клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="3a4b8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4b8-127">CommonParameters</span></span>
<span data-ttu-id="3a4b8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4b8-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4b8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4b8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-130">INPUTS</span></span>

### <span data-ttu-id="3a4b8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3a4b8-131">System.String</span></span>

## <span data-ttu-id="3a4b8-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-132">OUTPUTS</span></span>

### <span data-ttu-id="3a4b8-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a4b8-133">System.Boolean</span></span>

## <span data-ttu-id="3a4b8-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a4b8-134">NOTES</span></span>

## <span data-ttu-id="3a4b8-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a4b8-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a4b8-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3a4b8-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="3a4b8-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3a4b8-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="3a4b8-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3a4b8-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


