---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075736"
---
# <span data-ttu-id="b19c7-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b19c7-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b19c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b19c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b19c7-103">Добавление SSL-сертификата в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b19c7-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="b19c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b19c7-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b19c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19c7-105">DESCRIPTION</span></span>
<span data-ttu-id="b19c7-106">Командлет **Add-AzureApplicationGatewaySslCertificate** добавляет сертификат SSL (Secure Sockets Layer) в шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b19c7-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="b19c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b19c7-107">EXAMPLES</span></span>

### <span data-ttu-id="b19c7-108">Пример 1: Добавление SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="b19c7-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="b19c7-109">Эта команда добавляет SSL-сертификат с именем SslCertificate13 на шлюз приложений с именем ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="b19c7-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="b19c7-110">Команда задает путь к файлу сертификата и пароль сертификата.</span><span class="sxs-lookup"><span data-stu-id="b19c7-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="b19c7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b19c7-111">PARAMETERS</span></span>

### <span data-ttu-id="b19c7-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b19c7-112">-CertificateFile</span></span>
<span data-ttu-id="b19c7-113">Задает путь к файлу сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="b19c7-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="b19c7-114">Этот командлет добавляет сертификат в файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b19c7-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="b19c7-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b19c7-115">-CertificateName</span></span>
<span data-ttu-id="b19c7-116">Указывает имя сертификата SSL.</span><span class="sxs-lookup"><span data-stu-id="b19c7-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="b19c7-117">Этот командлет добавляет сертификат, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b19c7-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="b19c7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b19c7-118">-Name</span></span>
<span data-ttu-id="b19c7-119">Указывает имя шлюза приложений, с которым этот командлет добавляет сертификат SSL.</span><span class="sxs-lookup"><span data-stu-id="b19c7-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="b19c7-120">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="b19c7-120">-Password</span></span>
<span data-ttu-id="b19c7-121">Указывает пароль SSL-сертификата, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b19c7-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b19c7-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="b19c7-122">-Profile</span></span>
<span data-ttu-id="b19c7-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b19c7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b19c7-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b19c7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b19c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19c7-125">CommonParameters</span></span>
<span data-ttu-id="b19c7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b19c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19c7-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b19c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19c7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b19c7-128">INPUTS</span></span>

### <span data-ttu-id="b19c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b19c7-129">System.String</span></span>

## <span data-ttu-id="b19c7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19c7-130">OUTPUTS</span></span>

### <span data-ttu-id="b19c7-131">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b19c7-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="b19c7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b19c7-132">NOTES</span></span>

## <span data-ttu-id="b19c7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b19c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="b19c7-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b19c7-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b19c7-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b19c7-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
