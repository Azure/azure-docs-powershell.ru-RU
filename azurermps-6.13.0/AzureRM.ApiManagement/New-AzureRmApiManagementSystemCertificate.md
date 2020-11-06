---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556963"
---
# <span data-ttu-id="e2251-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="e2251-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="e2251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2251-102">SYNOPSIS</span></span>
<span data-ttu-id="e2251-103">Создает экземпляр `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="e2251-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="e2251-104">Сертификат может быть выдан частным центром сертификации и будет установлен на службу управления API `CertificateAuthority` или в `Root` магазин.</span><span class="sxs-lookup"><span data-stu-id="e2251-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2251-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2251-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2251-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2251-106">DESCRIPTION</span></span>
<span data-ttu-id="e2251-107">Командлет **New-AzureRmApiManagementSystemCertificate** является вспомогательной командой, которая создает экземпляр **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="e2251-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="e2251-108">Эта команда используется с командлетом New-AzureRmApiManagement и Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e2251-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="e2251-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2251-109">EXAMPLES</span></span>

### <span data-ttu-id="e2251-110">Пример 1: создание и инициализация экземпляра PsApiManagementSystemCertificate с помощью SSL-сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="e2251-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="e2251-111">Эта команда создает и инициализирует экземпляр **PsApiManagementSystemCertificate** с сертификатом корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="e2251-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="e2251-112">Затем создается служба управления API, которая устанавливает сертификат ЦС в корневое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e2251-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="e2251-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2251-113">PARAMETERS</span></span>

### <span data-ttu-id="e2251-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2251-114">-DefaultProfile</span></span>
<span data-ttu-id="e2251-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2251-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2251-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="e2251-116">-PfxPassword</span></span>
<span data-ttu-id="e2251-117">Пароль для PFX-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="e2251-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2251-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="e2251-118">-PfxPath</span></span>
<span data-ttu-id="e2251-119">Путь к PFX-файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="e2251-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="e2251-120">-Столбец StoreName</span><span class="sxs-lookup"><span data-stu-id="e2251-120">-StoreName</span></span>
<span data-ttu-id="e2251-121">Столбец StoreName сертификата</span><span class="sxs-lookup"><span data-stu-id="e2251-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2251-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2251-122">CommonParameters</span></span>
<span data-ttu-id="e2251-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2251-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2251-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2251-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2251-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2251-125">INPUTS</span></span>

### <span data-ttu-id="e2251-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e2251-126">System.String</span></span>

### <span data-ttu-id="e2251-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e2251-127">System.Security.SecureString</span></span>

## <span data-ttu-id="e2251-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2251-128">OUTPUTS</span></span>

### <span data-ttu-id="e2251-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="e2251-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="e2251-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2251-130">NOTES</span></span>

## <span data-ttu-id="e2251-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2251-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2251-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2251-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e2251-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e2251-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
