---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248247"
---
# <span data-ttu-id="da303-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="da303-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="da303-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da303-102">SYNOPSIS</span></span>
<span data-ttu-id="da303-103">Создание нового корневого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="da303-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="da303-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da303-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da303-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da303-105">DESCRIPTION</span></span>
<span data-ttu-id="da303-106">Командлет **New-AzVpnClientRootCertificate** создает новый корневой сертификат VPN для использования на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="da303-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="da303-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="da303-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="da303-108">Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="da303-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="da303-109">Вместо этого сертификат, созданный с помощью **New-AzVpnClientRootCertificate** , используется вместе с командлетом New-AzVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="da303-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="da303-110">Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="da303-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="da303-111">Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="da303-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="da303-112">Например, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="da303-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="da303-113">Дополнительные сведения можно найти в документации по командлету New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="da303-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="da303-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da303-114">EXAMPLES</span></span>

### <span data-ttu-id="da303-115">Пример 1: создание корневого сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="da303-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="da303-116">В этом примере создается корневой сертификат клиента и сохраняется объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="da303-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="da303-117">Эта переменная может затем использоваться командлетом **New-AzVirtualNetworkGateway** для добавления корневого сертификата в новый шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="da303-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="da303-118">Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления корневого сертификата; текстовые данные хранятся в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="da303-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="da303-119">Вторая команда использует цикл for, чтобы извлечь весь текст, кроме первой строки и последней строки, сохранив извлеченный текст в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="da303-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="da303-120">Третья команда использует командлет **New-AzVpnClientRootCertificate** , чтобы создать сертификат, сохранив созданный объект в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="da303-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="da303-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da303-121">PARAMETERS</span></span>

### <span data-ttu-id="da303-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da303-122">-DefaultProfile</span></span>
<span data-ttu-id="da303-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da303-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da303-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da303-124">-Name</span></span>
<span data-ttu-id="da303-125">Указывает имя для нового корневого сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="da303-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="da303-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="da303-126">-PublicCertData</span></span>
<span data-ttu-id="da303-127">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="da303-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="da303-128">Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="da303-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="da303-129">На экране должны отобразиться следующие данные (Обратите внимание на то, что реальный вывод содержит гораздо больше строк, чем сокращенный образец, показанный здесь):-----"начало сертификата-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----PublicCertData состоит из всех строк, находящихся между первой строкой (-----начинать сертификат-----), и последней строкой (-----конечный сертификат-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="da303-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="da303-130">Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже: $Text = Get-Content-путь "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="da303-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="da303-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da303-131">CommonParameters</span></span>
<span data-ttu-id="da303-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da303-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da303-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da303-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da303-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da303-134">INPUTS</span></span>

### <span data-ttu-id="da303-135">System. String</span><span class="sxs-lookup"><span data-stu-id="da303-135">System.String</span></span>

## <span data-ttu-id="da303-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da303-136">OUTPUTS</span></span>

### <span data-ttu-id="da303-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="da303-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="da303-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="da303-138">NOTES</span></span>

## <span data-ttu-id="da303-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da303-139">RELATED LINKS</span></span>

[<span data-ttu-id="da303-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="da303-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="da303-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="da303-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="da303-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="da303-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


