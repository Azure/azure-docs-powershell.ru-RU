---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317357"
---
# <span data-ttu-id="726c4-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="726c4-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="726c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="726c4-102">SYNOPSIS</span></span>
<span data-ttu-id="726c4-103">Создает экземпляр `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="726c4-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="726c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="726c4-104">SYNTAX</span></span>

### <span data-ttu-id="726c4-105">NoChangeCertificate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="726c4-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="726c4-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="726c4-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="726c4-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="726c4-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="726c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="726c4-108">DESCRIPTION</span></span>
<span data-ttu-id="726c4-109">Командлет **New-AzApiManagementCustomHostnameConfiguration** является вспомогательной командой, которая создает экземпляр **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="726c4-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="726c4-110">Эта команда используется с командлетом New-AzApiManagement и Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="726c4-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="726c4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="726c4-111">EXAMPLES</span></span>

### <span data-ttu-id="726c4-112">Пример 1: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с помощью SSL-сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="726c4-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="726c4-113">Эта команда создает и инициализирует экземпляр **PsApiManagementCustomHostNameConfiguration** для портала.</span><span class="sxs-lookup"><span data-stu-id="726c4-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="726c4-114">Затем он создает новую службу ApiManagement с настраиваемой конфигурацией hostname.</span><span class="sxs-lookup"><span data-stu-id="726c4-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="726c4-115">Пример 2: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с помощью секретного ключа из KeyVault ресурсов</span><span class="sxs-lookup"><span data-stu-id="726c4-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="726c4-116">Эта команда создает и инициализирует экземпляр **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="726c4-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="726c4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="726c4-117">PARAMETERS</span></span>

### <span data-ttu-id="726c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726c4-118">-DefaultProfile</span></span>
<span data-ttu-id="726c4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="726c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="726c4-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="726c4-120">-DefaultSslBinding</span></span>
<span data-ttu-id="726c4-121">Определяет, является ли значение секретным, которое должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="726c4-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="726c4-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="726c4-122">This parameter is optional.</span></span>
<span data-ttu-id="726c4-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="726c4-123">Default Value is false.</span></span>

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

### <span data-ttu-id="726c4-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="726c4-124">-Hostname</span></span>
<span data-ttu-id="726c4-125">Настраиваемое имя узла</span><span class="sxs-lookup"><span data-stu-id="726c4-125">Custom Hostname</span></span>

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

### <span data-ttu-id="726c4-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="726c4-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="726c4-127">Существующая конфигурация сертификата.</span><span class="sxs-lookup"><span data-stu-id="726c4-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="726c4-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="726c4-128">-HostnameType</span></span>
<span data-ttu-id="726c4-129">Тип hostname</span><span class="sxs-lookup"><span data-stu-id="726c4-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726c4-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="726c4-130">-KeyVaultId</span></span>
<span data-ttu-id="726c4-131">KeyVaultId секретный код, который хранит собственный SSL-сертификат.</span><span class="sxs-lookup"><span data-stu-id="726c4-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="726c4-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="726c4-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="726c4-133">Определяет, является ли значение секретным, которое должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="726c4-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="726c4-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="726c4-134">This parameter is optional.</span></span>
<span data-ttu-id="726c4-135">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="726c4-135">Default Value is false.</span></span>

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

### <span data-ttu-id="726c4-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="726c4-136">-PfxPassword</span></span>
<span data-ttu-id="726c4-137">Пароль для PFX-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="726c4-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="726c4-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="726c4-138">-PfxPath</span></span>
<span data-ttu-id="726c4-139">Путь к PFX-файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="726c4-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="726c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726c4-140">CommonParameters</span></span>
<span data-ttu-id="726c4-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="726c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726c4-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="726c4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726c4-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="726c4-143">INPUTS</span></span>

### <span data-ttu-id="726c4-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="726c4-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="726c4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="726c4-145">OUTPUTS</span></span>

### <span data-ttu-id="726c4-146">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="726c4-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="726c4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="726c4-147">NOTES</span></span>

## <span data-ttu-id="726c4-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="726c4-148">RELATED LINKS</span></span>

[<span data-ttu-id="726c4-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="726c4-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="726c4-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="726c4-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)