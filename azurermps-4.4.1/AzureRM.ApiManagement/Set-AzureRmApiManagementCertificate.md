---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734278"
---
# <span data-ttu-id="028c8-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="028c8-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="028c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="028c8-102">SYNOPSIS</span></span>
<span data-ttu-id="028c8-103">Изменение сертификата управления API.</span><span class="sxs-lookup"><span data-stu-id="028c8-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="028c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="028c8-104">SYNTAX</span></span>

### <span data-ttu-id="028c8-105">Загрузить из файла (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="028c8-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="028c8-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="028c8-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="028c8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="028c8-107">DESCRIPTION</span></span>
<span data-ttu-id="028c8-108">Командлет **Set-AzureRmApiManagementCertificate** изменяет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="028c8-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="028c8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="028c8-109">EXAMPLES</span></span>

### <span data-ttu-id="028c8-110">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="028c8-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="028c8-111">Эта команда изменяет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="028c8-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="028c8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="028c8-112">PARAMETERS</span></span>

### <span data-ttu-id="028c8-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="028c8-113">-CertificateId</span></span>
<span data-ttu-id="028c8-114">Указывает ИД сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="028c8-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="028c8-115">-Context</span><span class="sxs-lookup"><span data-stu-id="028c8-115">-Context</span></span>
<span data-ttu-id="028c8-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="028c8-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="028c8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="028c8-117">-PassThru</span></span>
<span data-ttu-id="028c8-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="028c8-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028c8-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="028c8-119">-PfxBytes</span></span>
<span data-ttu-id="028c8-120">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="028c8-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="028c8-121">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="028c8-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="028c8-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="028c8-122">-PfxFilePath</span></span>
<span data-ttu-id="028c8-123">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="028c8-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="028c8-124">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="028c8-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="028c8-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="028c8-125">-PfxPassword</span></span>
<span data-ttu-id="028c8-126">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="028c8-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="028c8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028c8-127">-DefaultProfile</span></span>
<span data-ttu-id="028c8-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="028c8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="028c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028c8-129">CommonParameters</span></span>
<span data-ttu-id="028c8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="028c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028c8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028c8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028c8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="028c8-132">INPUTS</span></span>

## <span data-ttu-id="028c8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="028c8-133">OUTPUTS</span></span>

### <span data-ttu-id="028c8-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="028c8-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="028c8-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="028c8-135">NOTES</span></span>

## <span data-ttu-id="028c8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="028c8-136">RELATED LINKS</span></span>

[<span data-ttu-id="028c8-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="028c8-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="028c8-138">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="028c8-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="028c8-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="028c8-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


