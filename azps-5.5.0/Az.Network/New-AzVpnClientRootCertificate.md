---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225900"
---
# <span data-ttu-id="5549d-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5549d-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="5549d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5549d-102">SYNOPSIS</span></span>
<span data-ttu-id="5549d-103">Создание корневого сертификата клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="5549d-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="5549d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5549d-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5549d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5549d-105">DESCRIPTION</span></span>
<span data-ttu-id="5549d-106">Новый корневой сертификат VPN для виртуального сетевого шлюза создается с помощью **cmdlet New-AzVpnClientRootCertificate.**</span><span class="sxs-lookup"><span data-stu-id="5549d-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="5549d-107">Корневые сертификаты — это сертификаты X.509, которые определяют корневой сертификат сертификации: все остальные сертификаты, используемые на шлюзе, доверять корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="5549d-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="5549d-108">Этот cmdlet создает автономный сертификат, который не назначен виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="5549d-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="5549d-109">Вместо этого сертификат, созданный **new-AzVpnClientRootCertificate,** используется в сочетании с New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="5549d-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="5549d-110">Предположим, например, что вы создали новый сертификат и храните его в переменной с $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5549d-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="5549d-111">Этот объект сертификата можно использовать при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="5549d-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="5549d-112">Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="5549d-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="5549d-113">Дополнительные сведения см. в документации New-AzVirtualNetworkGateway управления проектами.</span><span class="sxs-lookup"><span data-stu-id="5549d-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="5549d-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5549d-114">EXAMPLES</span></span>

### <span data-ttu-id="5549d-115">Пример 1. Создание корневого сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="5549d-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="5549d-116">В этом примере создается корневой сертификат клиента и объект сертификата сохраняется в переменной с $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5549d-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="5549d-117">Затем с помощью **командлета New-AzVirtualNetworkGateway** можно добавить корневой сертификат к новому виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="5549d-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="5549d-118">Первая команда использует **командлет Get-Content** для получения ранее экспортируемого текстового представления корневого сертификата. что текстовые данные хранятся в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="5549d-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="5549d-119">Затем с помощью циклов вторая команда извлекает весь текст, кроме первой и последней строк, с сохранением извлеченного текста в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="5549d-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="5549d-120">Третья команда использует командлет **New-AzVpnClientRootCertificate** для создания сертификата, храняного созданный объект в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="5549d-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="5549d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5549d-121">PARAMETERS</span></span>

### <span data-ttu-id="5549d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5549d-122">-DefaultProfile</span></span>
<span data-ttu-id="5549d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5549d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5549d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5549d-124">-Name</span></span>
<span data-ttu-id="5549d-125">Указывает имя нового корневого сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="5549d-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="5549d-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="5549d-126">-PublicCertData</span></span>
<span data-ttu-id="5549d-127">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="5549d-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="5549d-128">Чтобы получить текстовое представление, экспортировать сертификат в формате CER (с использованием кодиента Base64), а затем откройте получивающийся файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="5549d-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="5549d-129">Результаты должны быть примерно такие же (обратите внимание, что фактический результат будет содержать намного больше строк текста, чем показано в сокращенном примере): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo0 Конечный сертификат -----СVFAw8w ----- PublicCertData состоит из всех линий между первой строкой (----- BEGIN CERTIFICATE -----) и последней строкой (----- END CERTIFICATE -----) в файле.</span><span class="sxs-lookup"><span data-stu-id="5549d-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="5549d-130">Чтобы получить publicCertData, можно использовать команды Windows PowerShell примерно так: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="5549d-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="5549d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5549d-131">CommonParameters</span></span>
<span data-ttu-id="5549d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5549d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5549d-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5549d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5549d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5549d-134">INPUTS</span></span>

### <span data-ttu-id="5549d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5549d-135">System.String</span></span>

## <span data-ttu-id="5549d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5549d-136">OUTPUTS</span></span>

### <span data-ttu-id="5549d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5549d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="5549d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5549d-138">NOTES</span></span>

## <span data-ttu-id="5549d-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5549d-139">RELATED LINKS</span></span>

[<span data-ttu-id="5549d-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5549d-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="5549d-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5549d-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="5549d-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5549d-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


