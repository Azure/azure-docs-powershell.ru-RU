---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079881"
---
# <span data-ttu-id="644ff-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="644ff-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="644ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="644ff-102">SYNOPSIS</span></span>
<span data-ttu-id="644ff-103">Создает экземпляр `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="644ff-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="644ff-104">Сертификат может быть выдан частным центром сертификации и будет установлен на службу управления API `CertificateAuthority` или в `Root` магазин.</span><span class="sxs-lookup"><span data-stu-id="644ff-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="644ff-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="644ff-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644ff-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="644ff-106">DESCRIPTION</span></span>
<span data-ttu-id="644ff-107">Командлет **New-AzApiManagementSystemCertificate** является вспомогательной командой, которая создает экземпляр **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="644ff-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="644ff-108">Эта команда используется с командлетом New-AzApiManagement и Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="644ff-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="644ff-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="644ff-109">EXAMPLES</span></span>

### <span data-ttu-id="644ff-110">Пример 1: создание и инициализация экземпляра PsApiManagementSystemCertificate с помощью SSL-сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="644ff-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="644ff-111">Эта команда создает и инициализирует экземпляр **PsApiManagementSystemCertificate** с сертификатом корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="644ff-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="644ff-112">Затем создается служба управления API, которая устанавливает сертификат ЦС в корневое хранилище.</span><span class="sxs-lookup"><span data-stu-id="644ff-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="644ff-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="644ff-113">PARAMETERS</span></span>

### <span data-ttu-id="644ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644ff-114">-DefaultProfile</span></span>
<span data-ttu-id="644ff-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="644ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="644ff-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="644ff-116">-PfxPassword</span></span>
<span data-ttu-id="644ff-117">Пароль для PFX-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="644ff-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="644ff-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="644ff-118">-PfxPath</span></span>
<span data-ttu-id="644ff-119">Путь к PFX-файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="644ff-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="644ff-120">-Столбец StoreName</span><span class="sxs-lookup"><span data-stu-id="644ff-120">-StoreName</span></span>
<span data-ttu-id="644ff-121">Столбец StoreName сертификата</span><span class="sxs-lookup"><span data-stu-id="644ff-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="644ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644ff-122">CommonParameters</span></span>
<span data-ttu-id="644ff-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="644ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644ff-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="644ff-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644ff-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="644ff-125">INPUTS</span></span>

### <span data-ttu-id="644ff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="644ff-126">System.String</span></span>

### <span data-ttu-id="644ff-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="644ff-127">System.Security.SecureString</span></span>

## <span data-ttu-id="644ff-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="644ff-128">OUTPUTS</span></span>

### <span data-ttu-id="644ff-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="644ff-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="644ff-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="644ff-130">NOTES</span></span>

## <span data-ttu-id="644ff-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="644ff-131">RELATED LINKS</span></span>

[<span data-ttu-id="644ff-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="644ff-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="644ff-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="644ff-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)