---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247873"
---
# <span data-ttu-id="a5040-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5040-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="a5040-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5040-102">SYNOPSIS</span></span>
<span data-ttu-id="a5040-103">Создает имя узла configuratin для существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="a5040-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="a5040-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5040-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5040-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5040-105">DESCRIPTION</span></span>
<span data-ttu-id="a5040-106">Командлет **New-AzApiManagementGatewayHostnameConfiguration** создает имя узла configuratin для существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="a5040-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="a5040-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5040-107">EXAMPLES</span></span>

### <span data-ttu-id="a5040-108">Пример 1: создание конфигурации hostname для существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="a5040-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="a5040-109">Эта команда создает конфигурацию hostname "H01" для шлюза "G01".</span><span class="sxs-lookup"><span data-stu-id="a5040-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="a5040-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5040-110">PARAMETERS</span></span>

### <span data-ttu-id="a5040-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="a5040-111">-CertificateResourceId</span></span>
<span data-ttu-id="a5040-112">Идентификатор ресурса для существующего идентификатора сертификата. Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="a5040-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a5040-113">-Context</span></span>
<span data-ttu-id="a5040-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a5040-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a5040-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5040-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5040-116">-DefaultProfile</span></span>
<span data-ttu-id="a5040-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5040-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5040-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a5040-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="a5040-119">Идентификатор нового hostname (имя узла) confiuration.</span><span class="sxs-lookup"><span data-stu-id="a5040-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="a5040-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-120">This parameter is optional.</span></span>
<span data-ttu-id="a5040-121">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="a5040-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="a5040-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a5040-122">-GatewayId</span></span>
<span data-ttu-id="a5040-123">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="a5040-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="a5040-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a5040-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="a5040-125">-Hostname</span></span>
<span data-ttu-id="a5040-126">Имена.</span><span class="sxs-lookup"><span data-stu-id="a5040-126">Hostname.</span></span>
<span data-ttu-id="a5040-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a5040-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a5040-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="a5040-129">Пометка для принудительного применения NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a5040-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="a5040-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a5040-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5040-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5040-131">-Confirm</span></span>
<span data-ttu-id="a5040-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5040-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5040-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5040-133">-WhatIf</span></span>
<span data-ttu-id="a5040-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5040-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5040-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5040-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5040-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5040-136">CommonParameters</span></span>
<span data-ttu-id="a5040-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5040-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5040-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5040-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5040-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5040-139">INPUTS</span></span>

### <span data-ttu-id="a5040-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a5040-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a5040-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a5040-141">System.String</span></span>

### <span data-ttu-id="a5040-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5040-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a5040-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5040-143">OUTPUTS</span></span>

### <span data-ttu-id="a5040-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5040-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="a5040-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5040-145">NOTES</span></span>

## <span data-ttu-id="a5040-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5040-146">RELATED LINKS</span></span>