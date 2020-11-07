---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733515"
---
# <span data-ttu-id="659af-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="659af-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="659af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="659af-102">SYNOPSIS</span></span>
<span data-ttu-id="659af-103">Создает экземпляр `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="659af-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="659af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="659af-104">SYNTAX</span></span>

### <span data-ttu-id="659af-105">NoChangeCertificate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="659af-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="659af-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="659af-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="659af-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="659af-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="659af-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="659af-108">DESCRIPTION</span></span>
<span data-ttu-id="659af-109">Командлет **New-AzureRmApiManagementCustomHostnameConfiguration** является вспомогательной командой, которая создает экземпляр **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="659af-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="659af-110">Эта команда используется с командлетом New-AzureRmApiManagement и Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="659af-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="659af-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="659af-111">EXAMPLES</span></span>

### <span data-ttu-id="659af-112">Пример 1: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с помощью SSL-сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="659af-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="659af-113">Эта команда создает и инициализирует экземпляр **PsApiManagementCustomHostNameConfiguration** для портала.</span><span class="sxs-lookup"><span data-stu-id="659af-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="659af-114">Затем он создает новую службу ApiManagement с настраиваемой конфигурацией hostname.</span><span class="sxs-lookup"><span data-stu-id="659af-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="659af-115">Пример 2: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с помощью секретного ключа из KeyVault ресурсов</span><span class="sxs-lookup"><span data-stu-id="659af-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="659af-116">Эта команда создает и инициализирует экземпляр **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="659af-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="659af-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="659af-117">PARAMETERS</span></span>

### <span data-ttu-id="659af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659af-118">-DefaultProfile</span></span>
<span data-ttu-id="659af-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="659af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="659af-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="659af-120">-DefaultSslBinding</span></span>
<span data-ttu-id="659af-121">Определяет, является ли значение секретным, которое должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="659af-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="659af-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="659af-122">This parameter is optional.</span></span>
<span data-ttu-id="659af-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="659af-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="659af-124">-Hostname</span></span>
<span data-ttu-id="659af-125">Настраиваемое имя узла</span><span class="sxs-lookup"><span data-stu-id="659af-125">Custom Hostname</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="659af-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="659af-127">Существующая конфигурация сертификата.</span><span class="sxs-lookup"><span data-stu-id="659af-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="659af-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="659af-128">-HostnameType</span></span>
<span data-ttu-id="659af-129">Тип hostname</span><span class="sxs-lookup"><span data-stu-id="659af-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="659af-130">-KeyVaultId</span></span>
<span data-ttu-id="659af-131">KeyVaultId секретный код, который хранит собственный SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="659af-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="659af-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="659af-133">Определяет, является ли значение секретным, которое должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="659af-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="659af-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="659af-134">This parameter is optional.</span></span>
<span data-ttu-id="659af-135">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="659af-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="659af-136">-PfxPassword</span></span>
<span data-ttu-id="659af-137">Пароль для PFX-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="659af-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="659af-138">-PfxPath</span></span>
<span data-ttu-id="659af-139">Путь к PFX-файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="659af-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659af-140">CommonParameters</span></span>
<span data-ttu-id="659af-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="659af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659af-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659af-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="659af-143">INPUTS</span></span>

### <span data-ttu-id="659af-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="659af-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="659af-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="659af-145">OUTPUTS</span></span>

### <span data-ttu-id="659af-146">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="659af-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="659af-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="659af-147">NOTES</span></span>

## <span data-ttu-id="659af-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="659af-148">RELATED LINKS</span></span>

[<span data-ttu-id="659af-149">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="659af-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="659af-150">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="659af-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
