---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 95442c724548119726aa466edf1b4fa223271865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568866"
---
# <span data-ttu-id="bf862-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bf862-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="bf862-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf862-102">SYNOPSIS</span></span>
<span data-ttu-id="bf862-103">Удаляет существующий корневой сертификат VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="bf862-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf862-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf862-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf862-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf862-105">DESCRIPTION</span></span>
<span data-ttu-id="bf862-106">Командлет **Remove-AzureRmVpnClientRootCertificate** удаляет указанный корневой сертификат из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bf862-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="bf862-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="bf862-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="bf862-108">Если удалить корневой сертификат на компьютерах, использующих сертификат для проверки подлинности, подключение к шлюзу станет недоступным.</span><span class="sxs-lookup"><span data-stu-id="bf862-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="bf862-109">При использовании **Remove-AzureRmVpnClientRootCertificate** необходимо указать как имя сертификата, так и текстовое представление данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="bf862-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="bf862-110">Дополнительные сведения о текстовом представлении сертификата можно найти в описании параметра *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="bf862-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="bf862-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf862-111">EXAMPLES</span></span>

### <span data-ttu-id="bf862-112">Пример 1: удаление корневого сертификата клиента из шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="bf862-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="bf862-113">В этом примере удаляется корневой сертификат клиента с именем ContosoRootCertificate из шлюза виртуальной сети ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="bf862-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="bf862-114">Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления сертификата; Это текстовое представление хранится в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="bf862-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="bf862-115">Вторая команда использует цикл for для извлечения всего текста в $Text за исключением первой строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="bf862-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="bf862-116">Извлеченный текст хранится в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="bf862-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="bf862-117">Третья команда использует данные, хранящиеся в переменной $CertificateText, вместе с командлетом **Remove-AzureRmVpnClientRootCertificate** , чтобы удалить сертификат из шлюза.</span><span class="sxs-lookup"><span data-stu-id="bf862-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="bf862-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf862-118">PARAMETERS</span></span>

### <span data-ttu-id="bf862-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf862-119">-DefaultProfile</span></span>
<span data-ttu-id="bf862-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf862-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf862-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="bf862-121">-PublicCertData</span></span>
<span data-ttu-id="bf862-122">Указывает текстовое представление корневого сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bf862-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="bf862-123">Чтобы получить текстовое представление, экспортируйте его в формате CER (с использованием Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="bf862-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="bf862-124">Результат должен выглядеть примерно следующим образом (Обратите внимание на то, что реальный результат будет содержать больше строк, чем сокращенный образец, показанный здесь):-----начальный-----сертификата MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----PublicCertData состоит из всех строк, находящихся между первой строкой (-----начинать сертификат-----), и последней строкой (-----конечный сертификат-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="bf862-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="bf862-125">Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже: $Text = Get-Content-путь "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="bf862-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="bf862-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf862-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf862-127">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="bf862-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="bf862-128">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="bf862-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bf862-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bf862-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bf862-130">Указывает имя шлюза виртуальной сети, из которого удаляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="bf862-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="bf862-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="bf862-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="bf862-132">Указывает имя корневого сертификата клиента, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bf862-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf862-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf862-133">CommonParameters</span></span>
<span data-ttu-id="bf862-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf862-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf862-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf862-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf862-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf862-136">INPUTS</span></span>

### <span data-ttu-id="bf862-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bf862-137">System.String</span></span>

## <span data-ttu-id="bf862-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf862-138">OUTPUTS</span></span>

### <span data-ttu-id="bf862-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf862-139">System.Boolean</span></span>

## <span data-ttu-id="bf862-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf862-140">NOTES</span></span>

## <span data-ttu-id="bf862-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf862-141">RELATED LINKS</span></span>

[<span data-ttu-id="bf862-142">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bf862-142">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="bf862-143">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bf862-143">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="bf862-144">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bf862-144">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


