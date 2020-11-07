---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: 1fe178b80a39d4587a97207b6bd2d8cf6f4c9731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731674"
---
# <span data-ttu-id="b52b3-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b52b3-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="b52b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b52b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b52b3-103">Создание сертификата управления API, который будет использоваться при проверке подлинности в серверной части.</span><span class="sxs-lookup"><span data-stu-id="b52b3-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="b52b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b52b3-104">SYNTAX</span></span>

### <span data-ttu-id="b52b3-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b52b3-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b52b3-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="b52b3-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b52b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b52b3-107">DESCRIPTION</span></span>
<span data-ttu-id="b52b3-108">Командлет **New-AzApiManagementCertificate** создает сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="b52b3-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="b52b3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b52b3-109">EXAMPLES</span></span>

### <span data-ttu-id="b52b3-110">Пример 1: создание и отправка сертификата</span><span class="sxs-lookup"><span data-stu-id="b52b3-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="b52b3-111">Эта команда отправляет сертификат на управление API.</span><span class="sxs-lookup"><span data-stu-id="b52b3-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="b52b3-112">Этот сертификат можно использовать для взаимной проверки подлинности с помощью политик.</span><span class="sxs-lookup"><span data-stu-id="b52b3-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="b52b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b52b3-113">PARAMETERS</span></span>

### <span data-ttu-id="b52b3-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b52b3-114">-CertificateId</span></span>
<span data-ttu-id="b52b3-115">Указывает идентификатор создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="b52b3-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="b52b3-116">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b52b3-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="b52b3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b52b3-117">-Context</span></span>
<span data-ttu-id="b52b3-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b52b3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b52b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b52b3-119">-DefaultProfile</span></span>
<span data-ttu-id="b52b3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b52b3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b52b3-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="b52b3-121">-PfxBytes</span></span>
<span data-ttu-id="b52b3-122">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="b52b3-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="b52b3-123">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="b52b3-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="b52b3-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="b52b3-124">-PfxFilePath</span></span>
<span data-ttu-id="b52b3-125">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="b52b3-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="b52b3-126">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="b52b3-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b52b3-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="b52b3-127">-PfxPassword</span></span>
<span data-ttu-id="b52b3-128">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="b52b3-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="b52b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52b3-129">CommonParameters</span></span>
<span data-ttu-id="b52b3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b52b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52b3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b52b3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52b3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b52b3-132">INPUTS</span></span>

### <span data-ttu-id="b52b3-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b52b3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b52b3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b52b3-134">System.String</span></span>

### <span data-ttu-id="b52b3-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="b52b3-135">System.Byte[]</span></span>

## <span data-ttu-id="b52b3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b52b3-136">OUTPUTS</span></span>

### <span data-ttu-id="b52b3-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b52b3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b52b3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b52b3-138">NOTES</span></span>

## <span data-ttu-id="b52b3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b52b3-139">RELATED LINKS</span></span>

[<span data-ttu-id="b52b3-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b52b3-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="b52b3-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b52b3-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="b52b3-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b52b3-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


