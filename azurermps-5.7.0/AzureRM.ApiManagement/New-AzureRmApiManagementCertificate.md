---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563771"
---
# <span data-ttu-id="471ce-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="471ce-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="471ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="471ce-102">SYNOPSIS</span></span>
<span data-ttu-id="471ce-103">Создание сертификата управления API, который будет использоваться при проверке подлинности в серверной части.</span><span class="sxs-lookup"><span data-stu-id="471ce-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="471ce-104">SYNTAX</span></span>

### <span data-ttu-id="471ce-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="471ce-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="471ce-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="471ce-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="471ce-107">DESCRIPTION</span></span>
<span data-ttu-id="471ce-108">Командлет **New-AzureRmApiManagementCertificate** создает сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="471ce-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="471ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="471ce-109">EXAMPLES</span></span>

### <span data-ttu-id="471ce-110">Пример 1: создание и отправка сертификата</span><span class="sxs-lookup"><span data-stu-id="471ce-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="471ce-111">Эта команда отправляет сертификат на управление API.</span><span class="sxs-lookup"><span data-stu-id="471ce-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="471ce-112">Этот сертификат можно использовать для взаимной проверки подлинности с помощью политик.</span><span class="sxs-lookup"><span data-stu-id="471ce-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="471ce-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="471ce-113">PARAMETERS</span></span>

### <span data-ttu-id="471ce-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="471ce-114">-CertificateId</span></span>
<span data-ttu-id="471ce-115">Указывает идентификатор создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="471ce-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="471ce-116">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="471ce-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="471ce-117">-Context</span><span class="sxs-lookup"><span data-stu-id="471ce-117">-Context</span></span>
<span data-ttu-id="471ce-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="471ce-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471ce-119">-DefaultProfile</span></span>
<span data-ttu-id="471ce-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="471ce-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="471ce-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="471ce-121">-PfxBytes</span></span>
<span data-ttu-id="471ce-122">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="471ce-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="471ce-123">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="471ce-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471ce-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="471ce-124">-PfxFilePath</span></span>
<span data-ttu-id="471ce-125">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="471ce-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="471ce-126">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="471ce-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471ce-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="471ce-127">-PfxPassword</span></span>
<span data-ttu-id="471ce-128">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="471ce-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="471ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471ce-129">CommonParameters</span></span>
<span data-ttu-id="471ce-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="471ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471ce-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471ce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471ce-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="471ce-132">INPUTS</span></span>

### <span data-ttu-id="471ce-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="471ce-133">None</span></span>
<span data-ttu-id="471ce-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="471ce-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="471ce-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="471ce-135">OUTPUTS</span></span>

### <span data-ttu-id="471ce-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="471ce-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="471ce-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="471ce-137">NOTES</span></span>

## <span data-ttu-id="471ce-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="471ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="471ce-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="471ce-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="471ce-140">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="471ce-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="471ce-141">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="471ce-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


