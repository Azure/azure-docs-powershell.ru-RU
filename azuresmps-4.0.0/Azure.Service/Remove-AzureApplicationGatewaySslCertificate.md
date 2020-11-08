---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076494"
---
# <span data-ttu-id="9cf8c-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cf8c-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9cf8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf8c-103">Удаление SSL-сертификата из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="9cf8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cf8c-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9cf8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf8c-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf8c-106">Командлет **Remove-AzureApplicationGatewaySslCertificate** УДАЛЯЕТ сертификат SSL (Secure Sockets Layer) из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="9cf8c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cf8c-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf8c-108">Пример 1: Удаление SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="9cf8c-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="9cf8c-109">Эта команда удаляет SSL-сертификат с именем SslCertificate13 с шлюза приложений с именем ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="9cf8c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cf8c-110">PARAMETERS</span></span>

### <span data-ttu-id="9cf8c-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9cf8c-111">-CertificateName</span></span>
<span data-ttu-id="9cf8c-112">Указывает имя сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="9cf8c-113">Этот командлет удаляет сертификат, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="9cf8c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cf8c-114">-Name</span></span>
<span data-ttu-id="9cf8c-115">Указывает имя шлюза приложений, из которого этот командлет удаляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="9cf8c-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="9cf8c-116">-Profile</span></span>
<span data-ttu-id="9cf8c-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cf8c-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf8c-119">CommonParameters</span></span>
<span data-ttu-id="9cf8c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cf8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf8c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf8c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf8c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cf8c-122">INPUTS</span></span>

### <span data-ttu-id="9cf8c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf8c-123">System.String</span></span>

## <span data-ttu-id="9cf8c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cf8c-124">OUTPUTS</span></span>

### <span data-ttu-id="9cf8c-125">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9cf8c-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9cf8c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cf8c-126">NOTES</span></span>

## <span data-ttu-id="9cf8c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cf8c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9cf8c-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cf8c-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9cf8c-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9cf8c-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
