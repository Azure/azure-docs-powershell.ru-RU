---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561223"
---
# <span data-ttu-id="6215c-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6215c-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="6215c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6215c-102">SYNOPSIS</span></span>
<span data-ttu-id="6215c-103">Задает настраиваемую конфигурацию hostname для прокси-сервера или портала службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6215c-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6215c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6215c-104">SYNTAX</span></span>

### <span data-ttu-id="6215c-105">SetSpecificService (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6215c-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6215c-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="6215c-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6215c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6215c-107">DESCRIPTION</span></span>
<span data-ttu-id="6215c-108">Командлет **Set-AzureRmApiManagementHostnames** применяет настраиваемую конфигурацию hostname для прокси-сервера или портала службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6215c-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="6215c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6215c-109">EXAMPLES</span></span>

### <span data-ttu-id="6215c-110">Пример 1: Настройка конфигурации настраиваемого hostname для прокси-сервера и портала</span><span class="sxs-lookup"><span data-stu-id="6215c-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="6215c-111">Эта команда задает настраиваемое имя HostName Configuration для прокси-сервера и портала.</span><span class="sxs-lookup"><span data-stu-id="6215c-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="6215c-112">Пример 2: Настройка настраиваемого имени узла для прокси-сервера и портала</span><span class="sxs-lookup"><span data-stu-id="6215c-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="6215c-113">В этом примере осуществляется настройка настраиваемого имени узла для прокси-сервера и портала.</span><span class="sxs-lookup"><span data-stu-id="6215c-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="6215c-114">Вам нужно импортировать соответствующие сертификаты и затем применить пользовательские имена узлов.</span><span class="sxs-lookup"><span data-stu-id="6215c-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="6215c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6215c-115">PARAMETERS</span></span>

### <span data-ttu-id="6215c-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6215c-116">-ApiManagement</span></span>
<span data-ttu-id="6215c-117">Указывает экземпляр **PsApiManagement** , который этот командлет получает для параметров *PortalHostnameConfiguration* и *ProxyHostnameConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="6215c-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6215c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6215c-118">-DefaultProfile</span></span>
<span data-ttu-id="6215c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6215c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6215c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6215c-120">-Name</span></span>
<span data-ttu-id="6215c-121">Указывает имя экземпляра управления API.</span><span class="sxs-lookup"><span data-stu-id="6215c-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6215c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6215c-122">-PassThru</span></span>
<span data-ttu-id="6215c-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6215c-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6215c-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6215c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6215c-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6215c-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="6215c-126">Указывает конфигурацию узла настраиваемого портала.</span><span class="sxs-lookup"><span data-stu-id="6215c-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="6215c-127">Передача $null командлету задает имя узла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6215c-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6215c-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6215c-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="6215c-129">Указывает конфигурацию имени пользователя прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="6215c-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="6215c-130">Передача $null задает имя узла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6215c-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6215c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6215c-131">-ResourceGroupName</span></span>
<span data-ttu-id="6215c-132">Указывает имя группы ресурсов, в которой находится экземпляр управления API.</span><span class="sxs-lookup"><span data-stu-id="6215c-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6215c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6215c-133">CommonParameters</span></span>
<span data-ttu-id="6215c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6215c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6215c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6215c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6215c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6215c-136">INPUTS</span></span>

### <span data-ttu-id="6215c-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6215c-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="6215c-138">Параметры: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6215c-138">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="6215c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6215c-139">System.String</span></span>

### <span data-ttu-id="6215c-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6215c-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="6215c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6215c-141">OUTPUTS</span></span>

### <span data-ttu-id="6215c-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6215c-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6215c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6215c-143">NOTES</span></span>

## <span data-ttu-id="6215c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6215c-144">RELATED LINKS</span></span>

[<span data-ttu-id="6215c-145">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6215c-145">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="6215c-146">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6215c-146">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


