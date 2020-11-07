---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 8dac5309533a769bf6d41c82f25f97ff4170340f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730680"
---
# <span data-ttu-id="893a4-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893a4-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="893a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="893a4-102">SYNOPSIS</span></span>
<span data-ttu-id="893a4-103">Добавляет корневой сертификат VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="893a4-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="893a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="893a4-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="893a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="893a4-105">DESCRIPTION</span></span>
<span data-ttu-id="893a4-106">Командлет **Add-AzVpnClientRootCertificate** добавляет корневой сертификат в шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="893a4-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="893a4-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="893a4-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="893a4-108">По дизайну все сертификаты, используемые на шлюзе, доверяют корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="893a4-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="893a4-109">Этот командлет назначает существующий сертификат как корневой сертификат шлюза.</span><span class="sxs-lookup"><span data-stu-id="893a4-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="893a4-110">Если у вас нет сертификата X. 509, вы можете создать его с помощью инфраструктуры открытых ключей или использовать генератор сертификатов, например makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="893a4-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="893a4-111">Чтобы добавить корневой сертификат, необходимо указать имя сертификата и предоставить текстовое представление сертификата (Подробнее об этом можно узнать в параметре *PublicCertData* ).</span><span class="sxs-lookup"><span data-stu-id="893a4-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="893a4-112">Azure позволяет назначать шлюзу более одного корневого сертификата.</span><span class="sxs-lookup"><span data-stu-id="893a4-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="893a4-113">Множественные корневые сертификаты часто развертываются организациями, которые включают пользователей из нескольких компаний.</span><span class="sxs-lookup"><span data-stu-id="893a4-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="893a4-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="893a4-114">EXAMPLES</span></span>

### <span data-ttu-id="893a4-115">Пример 1: Добавление корневого сертификата клиента на виртуальный шлюз</span><span class="sxs-lookup"><span data-stu-id="893a4-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="893a4-116">В этом примере добавляется корневой сертификат клиента на виртуальный шлюз с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="893a4-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="893a4-117">Первая команда использует командлет **Get-Content** для получения ранее экспортированного текстового представления корневого сертификата и сохраняет эти текстовые данные переменной с именем $text.</span><span class="sxs-lookup"><span data-stu-id="893a4-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="893a4-118">Вторая команда использует цикл for для извлечения всего текста за исключением первой строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="893a4-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="893a4-119">Извлеченный текст хранится в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="893a4-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="893a4-120">Третья команда затем использует текст, хранящийся в $CertificateText, с помощью командлета **Add-AzVpnClientRootCertificate** , чтобы добавить корневой сертификат в шлюз.</span><span class="sxs-lookup"><span data-stu-id="893a4-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="893a4-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="893a4-121">PARAMETERS</span></span>

### <span data-ttu-id="893a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893a4-122">-DefaultProfile</span></span>
<span data-ttu-id="893a4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="893a4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893a4-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="893a4-124">-PublicCertData</span></span>
<span data-ttu-id="893a4-125">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="893a4-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="893a4-126">Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="893a4-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="893a4-127">В этом случае вывод будет выглядеть примерно так, как показано ниже (Обратите внимание на то, что фактический вывод содержит много строк текста, чем сокращенный образец, показанный здесь):-----начало-----сертификата MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----PublicCertData состоит из всех строк, находящихся между первой строкой (-----начинать сертификат-----) и последней строкой (-----конечный сертификат-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="893a4-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="893a4-128">Эти данные можно получить с помощью команд Windows PowerShell, подобных приведенным ниже. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="893a4-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="893a4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893a4-129">-ResourceGroupName</span></span>
<span data-ttu-id="893a4-130">Указывает имя группы ресурсов, которой назначен корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="893a4-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="893a4-131">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="893a4-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="893a4-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="893a4-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="893a4-133">Указывает имя шлюза виртуальной сети, в который добавляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="893a4-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="893a4-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="893a4-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="893a4-135">Указывает имя корневого сертификата клиента, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="893a4-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="893a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893a4-136">CommonParameters</span></span>
<span data-ttu-id="893a4-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="893a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893a4-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893a4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893a4-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="893a4-139">INPUTS</span></span>

### <span data-ttu-id="893a4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="893a4-140">System.String</span></span>

## <span data-ttu-id="893a4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="893a4-141">OUTPUTS</span></span>

### <span data-ttu-id="893a4-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893a4-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="893a4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="893a4-143">NOTES</span></span>

## <span data-ttu-id="893a4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="893a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="893a4-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893a4-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="893a4-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893a4-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="893a4-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="893a4-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


