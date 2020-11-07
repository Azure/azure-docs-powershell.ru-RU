---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: f9dbdaf531f4ccc35543dc542dc0637b9795360e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909589"
---
# <span data-ttu-id="9ac79-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9ac79-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9ac79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ac79-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac79-103">Создание нового сертификата отзыва VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="9ac79-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="9ac79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ac79-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac79-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac79-106">Командлет **New-AzVpnClientRevokedCertificate** создает новый сертификат отзыва для клиента виртуальной частной сети (VPN) для использования на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9ac79-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="9ac79-107">Сертификаты отзыва клиента не позволяют клиентским компьютерам использовать указанный сертификат для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9ac79-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="9ac79-108">Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="9ac79-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="9ac79-109">Вместо этого сертификат, созданный с помощью **New-AzVpnClientRevokedCertificate** , используется вместе с командлетом New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ac79-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="9ac79-110">Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="9ac79-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="9ac79-111">Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ac79-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="9ac79-112">Например,</span><span class="sxs-lookup"><span data-stu-id="9ac79-112">For instance,</span></span>

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="9ac79-113">Дополнительные сведения можно найти в документации по командлету New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="9ac79-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="9ac79-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ac79-114">EXAMPLES</span></span>

### <span data-ttu-id="9ac79-115">Пример 1: создание нового сертификата, отозванного клиентом</span><span class="sxs-lookup"><span data-stu-id="9ac79-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9ac79-116">Эта команда создает новый сертификат, отозванный клиентом, и сохраняет объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="9ac79-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="9ac79-117">Эта переменная может затем использоваться командлетом **New-AzVirtualNetworkGateway** для добавления сертификата в новый шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9ac79-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="9ac79-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ac79-118">PARAMETERS</span></span>

### <span data-ttu-id="9ac79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac79-119">-DefaultProfile</span></span>
<span data-ttu-id="9ac79-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac79-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac79-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ac79-121">-Name</span></span>
<span data-ttu-id="9ac79-122">Указывает уникальное имя для нового сертификата отзыва клиента.</span><span class="sxs-lookup"><span data-stu-id="9ac79-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="9ac79-123">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="9ac79-123">-Thumbprint</span></span>
<span data-ttu-id="9ac79-124">Указывает уникальный идентификатор добавляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="9ac79-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="9ac79-125">Вы можете вернуть отпечаток для сертификатов с помощью команды Windows PowerShell, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="9ac79-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="9ac79-126">Предыдущая команда возвращает сведения обо всех сертификатах локального компьютера, которые находятся в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9ac79-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="9ac79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac79-127">CommonParameters</span></span>
<span data-ttu-id="9ac79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ac79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac79-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac79-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ac79-130">INPUTS</span></span>

###  
<span data-ttu-id="9ac79-131">Этот командлет не поддерживает конвейерный вход.</span><span class="sxs-lookup"><span data-stu-id="9ac79-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="9ac79-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac79-132">OUTPUTS</span></span>

###  
<span data-ttu-id="9ac79-133">Этот командлет создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="9ac79-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="9ac79-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ac79-134">NOTES</span></span>

## <span data-ttu-id="9ac79-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ac79-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ac79-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9ac79-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9ac79-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9ac79-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9ac79-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9ac79-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


