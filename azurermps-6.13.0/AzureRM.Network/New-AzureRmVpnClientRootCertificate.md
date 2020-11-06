---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 18d634650248ea03c43b8ea24ec15aa3a2b79528
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562867"
---
# <span data-ttu-id="7bba3-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7bba3-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="7bba3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bba3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bba3-103">Создание нового корневого сертификата VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7bba3-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bba3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bba3-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bba3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bba3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bba3-106">Командлет **New-AzureRmVpnClientRootCertificate** создает новый корневой сертификат VPN для использования на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7bba3-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="7bba3-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="7bba3-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="7bba3-108">Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="7bba3-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="7bba3-109">Вместо этого сертификат, созданный с помощью **New-AzureRmVpnClientRootCertificate** , используется вместе с командлетом New-AzureRmVirtualNetworkGateway при создании нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="7bba3-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="7bba3-110">Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7bba3-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="7bba3-111">Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.</span><span class="sxs-lookup"><span data-stu-id="7bba3-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="7bba3-112">Например, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="7bba3-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="7bba3-113">Дополнительные сведения можно найти в документации по командлету New-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="7bba3-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="7bba3-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bba3-114">EXAMPLES</span></span>

### <span data-ttu-id="7bba3-115">Пример 1: создание корневого сертификата aclient</span><span class="sxs-lookup"><span data-stu-id="7bba3-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="7bba3-116">В этом примере создается корневой сертификат клиента и сохраняется объект сертификата в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7bba3-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="7bba3-117">Эта переменная может затем использоваться командлетом **New-AzureRmVirtualNetworkGateway** для добавления корневого сертификата в новый шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7bba3-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="7bba3-118">Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления корневого сертификата; текстовые данные хранятся в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="7bba3-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="7bba3-119">Вторая команда использует цикл for, чтобы извлечь весь текст, кроме первой строки и последней строки, сохранив извлеченный текст в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="7bba3-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="7bba3-120">Третья команда использует командлет **New-AzureRmVpnClientRootCertificate** , чтобы создать сертификат, сохранив созданный объект в переменной с именем $Certificate.</span><span class="sxs-lookup"><span data-stu-id="7bba3-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="7bba3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bba3-121">PARAMETERS</span></span>

### <span data-ttu-id="7bba3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bba3-122">-DefaultProfile</span></span>
<span data-ttu-id="7bba3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bba3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bba3-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bba3-124">-Name</span></span>
<span data-ttu-id="7bba3-125">Указывает имя для нового корневого сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="7bba3-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="7bba3-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="7bba3-126">-PublicCertData</span></span>
<span data-ttu-id="7bba3-127">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="7bba3-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="7bba3-128">Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="7bba3-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="7bba3-129">На экране должны отобразиться следующие данные (Обратите внимание на то, что реальный вывод содержит гораздо больше строк, чем сокращенный образец, показанный здесь):-----"начало сертификата-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----PublicCertData состоит из всех строк, находящихся между первой строкой (-----начинать сертификат-----), и последней строкой (-----конечный сертификат-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="7bba3-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="7bba3-130">Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже: $Text = Get-Content-путь "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="7bba3-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="7bba3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bba3-131">CommonParameters</span></span>
<span data-ttu-id="7bba3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bba3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bba3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bba3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bba3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bba3-134">INPUTS</span></span>

### <span data-ttu-id="7bba3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7bba3-135">System.String</span></span>

## <span data-ttu-id="7bba3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bba3-136">OUTPUTS</span></span>

### <span data-ttu-id="7bba3-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7bba3-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="7bba3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bba3-138">NOTES</span></span>

## <span data-ttu-id="7bba3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bba3-139">RELATED LINKS</span></span>

[<span data-ttu-id="7bba3-140">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7bba3-140">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="7bba3-141">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7bba3-141">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="7bba3-142">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7bba3-142">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


