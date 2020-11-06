---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565732"
---
# <span data-ttu-id="2c97d-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2c97d-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="2c97d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c97d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c97d-103">Создание сертификата управления API, который будет использоваться при проверке подлинности в серверной части.</span><span class="sxs-lookup"><span data-stu-id="2c97d-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c97d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c97d-104">SYNTAX</span></span>

### <span data-ttu-id="2c97d-105">Загрузить из файла (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c97d-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c97d-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="2c97d-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c97d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c97d-107">DESCRIPTION</span></span>
<span data-ttu-id="2c97d-108">Командлет **New-AzureRmApiManagementCertificate** создает сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2c97d-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="2c97d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c97d-109">EXAMPLES</span></span>

### <span data-ttu-id="2c97d-110">Пример 1: создание и отправка сертификата</span><span class="sxs-lookup"><span data-stu-id="2c97d-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="2c97d-111">Эта команда создает сертификат управления API и отправляет его.</span><span class="sxs-lookup"><span data-stu-id="2c97d-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="2c97d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c97d-112">PARAMETERS</span></span>

### <span data-ttu-id="2c97d-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2c97d-113">-CertificateId</span></span>
<span data-ttu-id="2c97d-114">Указывает идентификатор создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="2c97d-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="2c97d-115">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2c97d-115">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c97d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="2c97d-116">-Context</span></span>
<span data-ttu-id="2c97d-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2c97d-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c97d-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="2c97d-118">-PfxBytes</span></span>
<span data-ttu-id="2c97d-119">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="2c97d-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="2c97d-120">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="2c97d-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c97d-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="2c97d-121">-PfxFilePath</span></span>
<span data-ttu-id="2c97d-122">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="2c97d-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="2c97d-123">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="2c97d-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c97d-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="2c97d-124">-PfxPassword</span></span>
<span data-ttu-id="2c97d-125">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="2c97d-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="2c97d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c97d-126">-DefaultProfile</span></span>
<span data-ttu-id="2c97d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c97d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c97d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c97d-128">CommonParameters</span></span>
<span data-ttu-id="2c97d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c97d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c97d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c97d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c97d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c97d-131">INPUTS</span></span>

## <span data-ttu-id="2c97d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c97d-132">OUTPUTS</span></span>

### <span data-ttu-id="2c97d-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2c97d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="2c97d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c97d-134">NOTES</span></span>

## <span data-ttu-id="2c97d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c97d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c97d-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2c97d-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2c97d-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2c97d-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2c97d-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2c97d-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


