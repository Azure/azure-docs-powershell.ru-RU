---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410559"
---
# <span data-ttu-id="07585-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07585-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="07585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07585-102">SYNOPSIS</span></span>
<span data-ttu-id="07585-103">Добавляет корневой сертификат клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="07585-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="07585-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07585-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07585-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07585-105">DESCRIPTION</span></span>
<span data-ttu-id="07585-106">Cmdlet **Add-AzVpnClientRootCertificate** добавляет корневой сертификат к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="07585-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="07585-107">Корневые сертификаты — это сертификаты X.509, которые определяют корневой орган сертификации.</span><span class="sxs-lookup"><span data-stu-id="07585-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="07585-108">По конструктору все сертификаты, используемые шлюзом, доверять корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="07585-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="07585-109">Этот cmdlet назначает существующий сертификат в качестве корневого сертификата шлюза.</span><span class="sxs-lookup"><span data-stu-id="07585-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="07585-110">Если у вас нет сертификата X.509, его можно создать в инфраструктуре общего ключа или использовать генератор сертификатов, например makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="07585-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="07585-111">Чтобы добавить корневой сертификат, необходимо указать его имя и предоставить только текстовое представление сертификата (дополнительные сведения см. в параметре *PublicCertData).*</span><span class="sxs-lookup"><span data-stu-id="07585-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="07585-112">Azure позволяет назначить шлюзу несколько корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="07585-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="07585-113">Несколько корневых сертификатов часто развертываются организациями, которые включают пользователей из нескольких компаний.</span><span class="sxs-lookup"><span data-stu-id="07585-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="07585-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07585-114">EXAMPLES</span></span>

### <span data-ttu-id="07585-115">Пример 1. Добавление корневого сертификата клиента к виртуальному шлюзу</span><span class="sxs-lookup"><span data-stu-id="07585-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="07585-116">В этом примере корневой сертификат клиента добавляется к виртуальному шлюзу с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="07585-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="07585-117">Первая команда использует командлет **Get-Content** для получения ранее экспортируемого текстового представления корневого сертификата и сохраняет текстовые данные переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="07585-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="07585-118">Затем вторая команда извлекает весь текст, кроме первой и последней строк, с помощью циклов.</span><span class="sxs-lookup"><span data-stu-id="07585-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="07585-119">Извлеченный текст хранится в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="07585-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="07585-120">Затем с помощью командлета **Add-AzVpnClientRootCertificate,** сохраненного в $CertificateText, можно добавить корневой сертификат к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="07585-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="07585-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07585-121">PARAMETERS</span></span>

### <span data-ttu-id="07585-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07585-122">-DefaultProfile</span></span>
<span data-ttu-id="07585-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07585-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07585-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="07585-124">-PublicCertData</span></span>
<span data-ttu-id="07585-125">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="07585-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="07585-126">Чтобы получить текстовое представление, экспортировать сертификат в формате CER (с использованием кодиента Base64), а затем откройте получивающийся файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="07585-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="07585-127">При этом вы увидите результат, аналогичный следующему (обратите внимание, что фактический результат будет содержать намного больше строк текста, чем показано в сокращенном примере): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- PublicCertData состоит из всех линий между первой строкой (----- BEGIN CERTIFICATE -----) и последней строкой (----- END CERTIFICATE -----) в файле.</span><span class="sxs-lookup"><span data-stu-id="07585-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="07585-128">Эти данные можно извлечь с помощью Windows PowerShell примерно так: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="07585-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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

### <span data-ttu-id="07585-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07585-129">-ResourceGroupName</span></span>
<span data-ttu-id="07585-130">Имя группы ресурсов, которая назначена корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="07585-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="07585-131">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="07585-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="07585-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="07585-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="07585-133">Указывает имя виртуального сетевого шлюза, в который добавляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="07585-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="07585-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="07585-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="07585-135">Указывает имя корневого сертификата клиента, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07585-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="07585-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07585-136">CommonParameters</span></span>
<span data-ttu-id="07585-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07585-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07585-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07585-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07585-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07585-139">INPUTS</span></span>

### <span data-ttu-id="07585-140">System.String</span><span class="sxs-lookup"><span data-stu-id="07585-140">System.String</span></span>

## <span data-ttu-id="07585-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07585-141">OUTPUTS</span></span>

### <span data-ttu-id="07585-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07585-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="07585-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07585-143">NOTES</span></span>

## <span data-ttu-id="07585-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07585-144">RELATED LINKS</span></span>

[<span data-ttu-id="07585-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07585-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="07585-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07585-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="07585-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07585-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

