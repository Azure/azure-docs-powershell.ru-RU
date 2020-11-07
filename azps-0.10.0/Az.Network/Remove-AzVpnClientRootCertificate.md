---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: e9a04e255c91df49471b5b7070f6b95c48d45ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911094"
---
# <span data-ttu-id="4f64b-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f64b-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="4f64b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f64b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f64b-103">Удаляет существующий корневой сертификат VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="4f64b-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="4f64b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f64b-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f64b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f64b-105">DESCRIPTION</span></span>
<span data-ttu-id="4f64b-106">Командлет **Remove-AzVpnClientRootCertificate** удаляет указанный корневой сертификат из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4f64b-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="4f64b-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="4f64b-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="4f64b-108">Если удалить корневой сертификат на компьютерах, использующих сертификат для проверки подлинности, подключение к шлюзу станет недоступным.</span><span class="sxs-lookup"><span data-stu-id="4f64b-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="4f64b-109">При использовании **Remove-AzVpnClientRootCertificate** необходимо указать как имя сертификата, так и текстовое представление данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="4f64b-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="4f64b-110">Дополнительные сведения о текстовом представлении сертификата можно найти в описании параметра *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="4f64b-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="4f64b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f64b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f64b-112">Пример 1: удаление корневого сертификата клиента из шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="4f64b-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="4f64b-113">В этом примере удаляется корневой сертификат клиента с именем ContosoRootCertificate из шлюза виртуальной сети ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f64b-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="4f64b-114">Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления сертификата; Это текстовое представление хранится в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="4f64b-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="4f64b-115">Вторая команда использует цикл for для извлечения всего текста в $Text за исключением первой строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="4f64b-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="4f64b-116">Извлеченный текст хранится в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="4f64b-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="4f64b-117">Третья команда использует данные, хранящиеся в переменной $CertificateText, вместе с командлетом **Remove-AzVpnClientRootCertificate** , чтобы удалить сертификат из шлюза.</span><span class="sxs-lookup"><span data-stu-id="4f64b-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="4f64b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f64b-118">PARAMETERS</span></span>

### <span data-ttu-id="4f64b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f64b-119">-DefaultProfile</span></span>
<span data-ttu-id="4f64b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f64b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f64b-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="4f64b-121">-PublicCertData</span></span>
<span data-ttu-id="4f64b-122">Указывает текстовое представление корневого сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4f64b-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="4f64b-123">Чтобы получить текстовое представление, экспортируйте его в формате CER (с использованием Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="4f64b-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="4f64b-124">Результат должен выглядеть примерно так: Обратите внимание на то, что реальный результат будет содержать гораздо больше строк, чем сокращенный образец, показанный ниже.</span><span class="sxs-lookup"><span data-stu-id="4f64b-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="4f64b-125">-----"Начало-----сертификата" MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----</span><span class="sxs-lookup"><span data-stu-id="4f64b-125">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="4f64b-126">PublicCertData состоит из всех строк между первой строкой (-----"начало-----сертификата") и последней строки (-----конец сертификата-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="4f64b-126">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="4f64b-127">Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4f64b-127">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="4f64b-128">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="4f64b-128">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f64b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f64b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4f64b-130">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4f64b-130">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="4f64b-131">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="4f64b-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f64b-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4f64b-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4f64b-133">Указывает имя шлюза виртуальной сети, из которого удаляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="4f64b-133">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f64b-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="4f64b-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="4f64b-135">Указывает имя корневого сертификата клиента, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4f64b-135">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f64b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f64b-136">CommonParameters</span></span>
<span data-ttu-id="4f64b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f64b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f64b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f64b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f64b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f64b-139">INPUTS</span></span>

## <span data-ttu-id="4f64b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f64b-140">OUTPUTS</span></span>

## <span data-ttu-id="4f64b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f64b-141">NOTES</span></span>

## <span data-ttu-id="4f64b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f64b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4f64b-143">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f64b-143">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4f64b-144">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f64b-144">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4f64b-145">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4f64b-145">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


