---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315413"
---
# <span data-ttu-id="b15e1-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15e1-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="b15e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b15e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b15e1-103">Возвращает для существующего шлюза все или определенную конфигурацию имени узла.</span><span class="sxs-lookup"><span data-stu-id="b15e1-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="b15e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b15e1-104">SYNTAX</span></span>

### <span data-ttu-id="b15e1-105">GetByGatewayId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b15e1-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b15e1-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="b15e1-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b15e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b15e1-107">DESCRIPTION</span></span>
<span data-ttu-id="b15e1-108">Командлет **Get-AzApiManagementGatewayHostnameConfiguration** возвращает все или определенные параметры hostname для существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="b15e1-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="b15e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b15e1-109">EXAMPLES</span></span>

### <span data-ttu-id="b15e1-110">Пример 1: получение всех конфигураций hostname для шлюза</span><span class="sxs-lookup"><span data-stu-id="b15e1-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="b15e1-111">Эта команда получает все конфигурации имен узлов для шлюза 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b15e1-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="b15e1-112">Пример 2: получение конфигурации имени узла для шлюза</span><span class="sxs-lookup"><span data-stu-id="b15e1-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="b15e1-113">Эта команда возвращает конфигурацию hostname "123" для шлюза "0123456789".</span><span class="sxs-lookup"><span data-stu-id="b15e1-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="b15e1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b15e1-114">PARAMETERS</span></span>

### <span data-ttu-id="b15e1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b15e1-115">-Context</span></span>
<span data-ttu-id="b15e1-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b15e1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b15e1-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b15e1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b15e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15e1-118">-DefaultProfile</span></span>
<span data-ttu-id="b15e1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b15e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15e1-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b15e1-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="b15e1-121">Идентификатор конфигурации hostname.</span><span class="sxs-lookup"><span data-stu-id="b15e1-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="b15e1-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b15e1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b15e1-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b15e1-123">-GatewayId</span></span>
<span data-ttu-id="b15e1-124">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="b15e1-124">Gateway identifier.</span></span>
<span data-ttu-id="b15e1-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b15e1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="b15e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15e1-126">CommonParameters</span></span>
<span data-ttu-id="b15e1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b15e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15e1-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b15e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15e1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b15e1-129">INPUTS</span></span>

### <span data-ttu-id="b15e1-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b15e1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b15e1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b15e1-131">System.String</span></span>

## <span data-ttu-id="b15e1-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b15e1-132">OUTPUTS</span></span>

### <span data-ttu-id="b15e1-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b15e1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="b15e1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b15e1-134">NOTES</span></span>

## <span data-ttu-id="b15e1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b15e1-135">RELATED LINKS</span></span>
