---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075664"
---
# <span data-ttu-id="a9a74-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a74-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a9a74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9a74-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a74-103">Возвращает сертификаты для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a9a74-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="a9a74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9a74-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a9a74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9a74-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a74-106">Командлет **Get-AzureApplicationGatewaySslCertificate** получает сертификаты SSL (Secure Sockets Layer) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a74-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="a9a74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9a74-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a74-108">Пример 1: получение сертификата SSL</span><span class="sxs-lookup"><span data-stu-id="a9a74-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="a9a74-109">Эта команда получает сертификат SSL с именем SslCertificate13 на шлюзе приложений с именем ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="a9a74-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="a9a74-110">Пример 2: получение всех SSL-сертификатов</span><span class="sxs-lookup"><span data-stu-id="a9a74-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="a9a74-111">Эта команда получает все сертификаты SSL на шлюзе приложений с именем ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="a9a74-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="a9a74-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9a74-112">PARAMETERS</span></span>

### <span data-ttu-id="a9a74-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a9a74-113">-CertificateName</span></span>
<span data-ttu-id="a9a74-114">Указывает имя сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="a9a74-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="a9a74-115">Этот командлет получает сертификат, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a9a74-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a74-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9a74-116">-Name</span></span>
<span data-ttu-id="a9a74-117">Указывает имя шлюза приложений, из которого этот командлет получает сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="a9a74-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

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

### <span data-ttu-id="a9a74-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9a74-118">-Profile</span></span>
<span data-ttu-id="a9a74-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a9a74-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9a74-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9a74-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9a74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a74-121">CommonParameters</span></span>
<span data-ttu-id="a9a74-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9a74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a74-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a74-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a74-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9a74-124">INPUTS</span></span>

### <span data-ttu-id="a9a74-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a9a74-125">System.String</span></span>

## <span data-ttu-id="a9a74-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9a74-126">OUTPUTS</span></span>

### <span data-ttu-id="a9a74-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, список<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="a9a74-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="a9a74-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9a74-128">NOTES</span></span>

## <span data-ttu-id="a9a74-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9a74-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9a74-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a74-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a9a74-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9a74-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
