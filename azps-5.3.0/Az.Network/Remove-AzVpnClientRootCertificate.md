---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518042"
---
# <span data-ttu-id="55b95-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="55b95-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="55b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b95-102">SYNOPSIS</span></span>
<span data-ttu-id="55b95-103">Удаляет существующий корневой сертификат клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="55b95-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="55b95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55b95-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55b95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55b95-105">DESCRIPTION</span></span>
<span data-ttu-id="55b95-106">Для **удаления из** виртуального сетевого шлюза удаляется указанный корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="55b95-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="55b95-107">Корневые сертификаты — это сертификаты X.509, которые определяют корневой сертификат сертификации: все остальные сертификаты, используемые на шлюзе, доверять корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="55b95-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="55b95-108">Если удалить корневой сертификат, компьютеры, на которые он используется в целях проверки подлинности, больше не смогут подключаться к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="55b95-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="55b95-109">При использовании **Remove-AzVpnClientRootCertificate** необходимо предоставить как имя сертификата, так и текстовое представление данных сертификата.</span><span class="sxs-lookup"><span data-stu-id="55b95-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="55b95-110">Дополнительные сведения о текстовом представлении сертификата см. в описании параметра *PublicCertData.*</span><span class="sxs-lookup"><span data-stu-id="55b95-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="55b95-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55b95-111">EXAMPLES</span></span>

### <span data-ttu-id="55b95-112">Пример 1. Удаление корневого сертификата клиента из виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="55b95-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="55b95-113">В этом примере из виртуального сетевого шлюза ContosoVirtualGateway удаляется корневой сертификат клиента с именем ContosoRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="55b95-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="55b95-114">Первая команда использует **командлет Get-Content** для получения ранее экспортируемого текстового представления сертификата; Это текстовое представление хранится в переменной с именем $Text.</span><span class="sxs-lookup"><span data-stu-id="55b95-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="55b95-115">Затем с помощью циклов вторая команда извлекает весь текст в $Text кроме первой и последней строк.</span><span class="sxs-lookup"><span data-stu-id="55b95-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="55b95-116">Извлеченный текст сохраняется в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="55b95-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="55b95-117">В третьей команде используются данные, хранимые в переменной $CertificateText, а также командлет **Remove-AzVpnClientRootCertificate,** чтобы удалить сертификат со шлюза.</span><span class="sxs-lookup"><span data-stu-id="55b95-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="55b95-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55b95-118">PARAMETERS</span></span>

### <span data-ttu-id="55b95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b95-119">-DefaultProfile</span></span>
<span data-ttu-id="55b95-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55b95-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b95-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="55b95-121">-PublicCertData</span></span>
<span data-ttu-id="55b95-122">Указывает текстовое представление корневого сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="55b95-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="55b95-123">Чтобы получить текстовое представление, экспортировать сертификат в формате CER (с использованием базовой 64-й кодиации), а затем откройте получивающийся файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="55b95-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="55b95-124">Результаты должны быть примерно такие же (обратите внимание, что фактический результат будет содержать намного больше строк текста, чем показано в сокращенном примере): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HGUNEW8343NMJklo0 Конечный сертификат -----СVFAw8w ----- PublicCertData состоит из всех линий между первой строкой (----- BEGIN CERTIFICATE -----) и последней строкой (----- END CERTIFICATE -----) в файле.</span><span class="sxs-lookup"><span data-stu-id="55b95-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="55b95-125">Получить PublicCertData можно с помощью команд Windows PowerShell примерно так: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="55b95-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="55b95-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b95-126">-ResourceGroupName</span></span>
<span data-ttu-id="55b95-127">Указывает имя группы ресурсов, которая назначена виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="55b95-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="55b95-128">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="55b95-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="55b95-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="55b95-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="55b95-130">Указывает имя виртуального сетевого шлюза, из которого удален сертификат.</span><span class="sxs-lookup"><span data-stu-id="55b95-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="55b95-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="55b95-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="55b95-132">Указывает имя корневого сертификата клиента, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b95-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="55b95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b95-133">CommonParameters</span></span>
<span data-ttu-id="55b95-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b95-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b95-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b95-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55b95-136">INPUTS</span></span>

### <span data-ttu-id="55b95-137">System.String</span><span class="sxs-lookup"><span data-stu-id="55b95-137">System.String</span></span>

## <span data-ttu-id="55b95-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55b95-138">OUTPUTS</span></span>

### <span data-ttu-id="55b95-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55b95-139">System.Boolean</span></span>

## <span data-ttu-id="55b95-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55b95-140">NOTES</span></span>

## <span data-ttu-id="55b95-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55b95-141">RELATED LINKS</span></span>

[<span data-ttu-id="55b95-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="55b95-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="55b95-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="55b95-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="55b95-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="55b95-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


