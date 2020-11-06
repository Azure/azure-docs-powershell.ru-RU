---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556915"
---
# <span data-ttu-id="e6484-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e6484-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="e6484-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6484-102">SYNOPSIS</span></span>
<span data-ttu-id="e6484-103">Изменение сертификата управления API, настроенного для взаимной проверки подлинности на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="e6484-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6484-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6484-104">SYNTAX</span></span>

### <span data-ttu-id="e6484-105">LoadFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6484-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6484-106">Сырь</span><span class="sxs-lookup"><span data-stu-id="e6484-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6484-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6484-107">DESCRIPTION</span></span>
<span data-ttu-id="e6484-108">Командлет **Set-AzureRmApiManagementCertificate** изменяет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="e6484-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="e6484-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6484-109">EXAMPLES</span></span>

### <span data-ttu-id="e6484-110">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="e6484-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="e6484-111">Эта команда изменяет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="e6484-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="e6484-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6484-112">PARAMETERS</span></span>

### <span data-ttu-id="e6484-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e6484-113">-CertificateId</span></span>
<span data-ttu-id="e6484-114">Указывает ИД сертификата, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="e6484-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="e6484-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e6484-115">-Context</span></span>
<span data-ttu-id="e6484-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e6484-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e6484-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6484-117">-DefaultProfile</span></span>
<span data-ttu-id="e6484-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6484-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6484-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6484-119">-PassThru</span></span>
<span data-ttu-id="e6484-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="e6484-120">passthru</span></span>

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

### <span data-ttu-id="e6484-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="e6484-121">-PfxBytes</span></span>
<span data-ttu-id="e6484-122">Задает массив байтов из файла сертификата в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="e6484-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="e6484-123">Этот параметр является обязательным, если не указан параметр *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="e6484-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="e6484-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="e6484-124">-PfxFilePath</span></span>
<span data-ttu-id="e6484-125">Задает путь к файлу сертификата в формате PFX для создания и отправки.</span><span class="sxs-lookup"><span data-stu-id="e6484-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="e6484-126">Этот параметр является обязательным, если не указан параметр *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="e6484-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="e6484-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="e6484-127">-PfxPassword</span></span>
<span data-ttu-id="e6484-128">Указывает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="e6484-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="e6484-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6484-129">CommonParameters</span></span>
<span data-ttu-id="e6484-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6484-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6484-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6484-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6484-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6484-132">INPUTS</span></span>

### <span data-ttu-id="e6484-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6484-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6484-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e6484-134">System.String</span></span>

### <span data-ttu-id="e6484-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="e6484-135">System.Byte[]</span></span>

### <span data-ttu-id="e6484-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6484-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6484-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6484-137">OUTPUTS</span></span>

### <span data-ttu-id="e6484-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e6484-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="e6484-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6484-139">NOTES</span></span>

## <span data-ttu-id="e6484-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6484-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6484-141">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e6484-141">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="e6484-142">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e6484-142">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="e6484-143">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e6484-143">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


