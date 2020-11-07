---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 847f1c06975e9bef570c5ab3fdaf5f6f3e4a99d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902266"
---
# <span data-ttu-id="727f2-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="727f2-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="727f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="727f2-102">SYNOPSIS</span></span>
<span data-ttu-id="727f2-103">Получение сведений о корневых сертификатах VPN.</span><span class="sxs-lookup"><span data-stu-id="727f2-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="727f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="727f2-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="727f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="727f2-105">DESCRIPTION</span></span>
<span data-ttu-id="727f2-106">Командлет **Get-AzVpnClientRootCertificate** возвращает сведения о корневых сертификатах, назначенных шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="727f2-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="727f2-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="727f2-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="727f2-108">По умолчанию **Get-AzVpnClientRootCertificate** возвращает сведения о всех корневых сертификатах, назначенных шлюзу.</span><span class="sxs-lookup"><span data-stu-id="727f2-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="727f2-109">(Шлюзы могут иметь более одного корневого сертификата.) Однако, включив параметр **VpnClientRootCertificateName** , вы можете ограничить возвращаемые данные определенным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="727f2-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="727f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="727f2-110">EXAMPLES</span></span>

### <span data-ttu-id="727f2-111">Пример 1: получение сведений обо всех корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="727f2-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="727f2-112">Эта команда получает сведения обо всех корневых сертификатах, назначенных виртуальному сетевому шлюзу с именем ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="727f2-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="727f2-113">Пример 2: получение сведений о конкретных корневых сертификатах</span><span class="sxs-lookup"><span data-stu-id="727f2-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="727f2-114">Эта команда является вариантом команды, показанной в примере 1.</span><span class="sxs-lookup"><span data-stu-id="727f2-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="727f2-115">Однако в этом случае параметр *VpnClientRootCertificateName* включается, чтобы ограничить возвращаемые данные определенным корневым сертификатом: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="727f2-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="727f2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="727f2-116">PARAMETERS</span></span>

### <span data-ttu-id="727f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="727f2-117">-DefaultProfile</span></span>
<span data-ttu-id="727f2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="727f2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="727f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="727f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="727f2-120">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="727f2-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="727f2-121">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="727f2-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="727f2-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="727f2-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="727f2-123">Указывает имя шлюза виртуальной сети, на котором назначен корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="727f2-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="727f2-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="727f2-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="727f2-125">Указывает имя корневого сертификата клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="727f2-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="727f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="727f2-126">CommonParameters</span></span>
<span data-ttu-id="727f2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="727f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="727f2-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="727f2-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="727f2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="727f2-129">INPUTS</span></span>

### <span data-ttu-id="727f2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="727f2-130">System.String</span></span>

## <span data-ttu-id="727f2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="727f2-131">OUTPUTS</span></span>

### <span data-ttu-id="727f2-132">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="727f2-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="727f2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="727f2-133">NOTES</span></span>

## <span data-ttu-id="727f2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="727f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="727f2-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="727f2-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="727f2-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="727f2-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="727f2-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="727f2-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


