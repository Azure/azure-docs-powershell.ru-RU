---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913444"
---
# <span data-ttu-id="92278-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="92278-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92278-102">SYNOPSIS</span></span>
<span data-ttu-id="92278-103">Создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="92278-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92278-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92278-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92278-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92278-105">DESCRIPTION</span></span>
<span data-ttu-id="92278-106">Командлет **New-AzureRmApplicationGatewaySslCertificate** создает SSL-сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="92278-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="92278-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92278-107">EXAMPLES</span></span>

### <span data-ttu-id="92278-108">Пример 1: создание SSL-сертификата для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="92278-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="92278-109">Эта команда создает SSL-сертификат с именем Cert01 для шлюза приложений по умолчанию и сохраняет результат в переменной с именем $Cert.</span><span class="sxs-lookup"><span data-stu-id="92278-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="92278-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92278-110">PARAMETERS</span></span>

### <span data-ttu-id="92278-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="92278-111">-CertificateFile</span></span>
<span data-ttu-id="92278-112">Указывает путь PFX-файла SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92278-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="92278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92278-113">-DefaultProfile</span></span>
<span data-ttu-id="92278-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92278-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92278-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92278-115">-Name</span></span>
<span data-ttu-id="92278-116">Указывает имя SSL-сертификата, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92278-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="92278-117">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="92278-117">-Password</span></span>
<span data-ttu-id="92278-118">Указывает пароль SSL, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="92278-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92278-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92278-119">CommonParameters</span></span>
<span data-ttu-id="92278-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92278-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92278-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92278-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92278-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92278-122">INPUTS</span></span>

### <span data-ttu-id="92278-123">System. String</span><span class="sxs-lookup"><span data-stu-id="92278-123">System.String</span></span>

## <span data-ttu-id="92278-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92278-124">OUTPUTS</span></span>

### <span data-ttu-id="92278-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="92278-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="92278-126">NOTES</span></span>

## <span data-ttu-id="92278-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92278-127">RELATED LINKS</span></span>

[<span data-ttu-id="92278-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92278-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92278-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="92278-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="92278-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


