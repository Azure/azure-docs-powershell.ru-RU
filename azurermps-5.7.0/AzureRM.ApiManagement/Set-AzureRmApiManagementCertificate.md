---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565032"
---
# <span data-ttu-id="7a423-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7a423-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="7a423-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a423-102">SYNOPSIS</span></span>
<span data-ttu-id="7a423-103">Изменение сертификата управления API, настроенного для взаимной проверки подлинности на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="7a423-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a423-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a423-104">SYNTAX</span></span>

### <span data-ttu-id="7a423-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a423-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a423-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="7a423-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a423-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a423-107">DESCRIPTION</span></span>
<span data-ttu-id="7a423-108">Командлет **Set-AzureRmApiManagementCertificate** изменяет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="7a423-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="7a423-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a423-109">EXAMPLES</span></span>

### <span data-ttu-id="7a423-110">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="7a423-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="7a423-111">Эта команда изменяет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="7a423-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="7a423-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a423-112">PARAMETERS</span></span>

### <span data-ttu-id="7a423-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="7a423-113">-CertificateId</span></span>
<span data-ttu-id="7a423-114">Указывает ИД сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7a423-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="7a423-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7a423-115">-Context</span></span>
<span data-ttu-id="7a423-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7a423-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7a423-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a423-117">-DefaultProfile</span></span>
<span data-ttu-id="7a423-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a423-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7a423-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a423-119">-PassThru</span></span>
<span data-ttu-id="7a423-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="7a423-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a423-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="7a423-121">-PfxBytes</span></span>
<span data-ttu-id="7a423-122">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="7a423-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="7a423-123">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="7a423-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="7a423-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="7a423-124">-PfxFilePath</span></span>
<span data-ttu-id="7a423-125">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="7a423-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="7a423-126">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="7a423-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="7a423-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="7a423-127">-PfxPassword</span></span>
<span data-ttu-id="7a423-128">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="7a423-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="7a423-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a423-129">CommonParameters</span></span>
<span data-ttu-id="7a423-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a423-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a423-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a423-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a423-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a423-132">INPUTS</span></span>

### <span data-ttu-id="7a423-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="7a423-133">None</span></span>
<span data-ttu-id="7a423-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7a423-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a423-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a423-135">OUTPUTS</span></span>

### <span data-ttu-id="7a423-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7a423-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="7a423-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a423-137">NOTES</span></span>

## <span data-ttu-id="7a423-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a423-138">RELATED LINKS</span></span>

[<span data-ttu-id="7a423-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7a423-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="7a423-140">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7a423-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="7a423-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="7a423-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


