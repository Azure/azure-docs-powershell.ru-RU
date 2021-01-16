---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410564"
---
# <span data-ttu-id="1ab8f-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8f-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1ab8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab8f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab8f-103">Добавляет сертификат отзыва клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="1ab8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ab8f-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ab8f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ab8f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ab8f-106">Cmdlet **Add-AzVpnClientRevokedCertificate** назначает сертификат отзыва клиента виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="1ab8f-107">Сертификаты отзыва клиента не могут использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="1ab8f-108">Для использования этого cmdlet необходимо указать как имя сертификата, так и его отпечаток.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="1ab8f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ab8f-109">EXAMPLES</span></span>

### <span data-ttu-id="1ab8f-110">Пример 1. Добавление нового сертификата отзыва клиента к виртуальному сетевому шлюзу</span><span class="sxs-lookup"><span data-stu-id="1ab8f-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1ab8f-111">Эта команда добавляет новый сертификат отзыва клиента к виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="1ab8f-112">Чтобы добавить сертификат, необходимо указать как его имя, так и его эскиз.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="1ab8f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ab8f-113">PARAMETERS</span></span>

### <span data-ttu-id="1ab8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab8f-114">-DefaultProfile</span></span>
<span data-ttu-id="1ab8f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ab8f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab8f-116">-ResourceGroupName</span></span>
<span data-ttu-id="1ab8f-117">Имя группы ресурсов, назначенной виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="1ab8f-118">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1ab8f-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="1ab8f-119">-Thumbprint</span></span>
<span data-ttu-id="1ab8f-120">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="1ab8f-121">Например: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Вы можете получить данные эскизов для сертификатов, используя команду Windows PowerShell примерно так: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="1ab8f-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="1ab8f-122">Перед этой командой выдается информация о всех сертификатах локального компьютера, найденных в корневом хранилище.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="1ab8f-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1ab8f-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1ab8f-124">Указывает имя виртуального сетевого шлюза, в который нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="1ab8f-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="1ab8f-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="1ab8f-126">Указывает имя добавляемого сертификата клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="1ab8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab8f-127">CommonParameters</span></span>
<span data-ttu-id="1ab8f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab8f-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab8f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab8f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ab8f-130">INPUTS</span></span>

### <span data-ttu-id="1ab8f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1ab8f-131">System.String</span></span>

## <span data-ttu-id="1ab8f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ab8f-132">OUTPUTS</span></span>

### <span data-ttu-id="1ab8f-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8f-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1ab8f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ab8f-134">NOTES</span></span>

## <span data-ttu-id="1ab8f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ab8f-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ab8f-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8f-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="1ab8f-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8f-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="1ab8f-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8f-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


