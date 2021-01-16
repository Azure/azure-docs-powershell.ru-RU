---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413887"
---
# <span data-ttu-id="9c668-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c668-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="9c668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c668-102">SYNOPSIS</span></span>
<span data-ttu-id="9c668-103">Возвращает всю или определенную конфигурацию имени для существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="9c668-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="9c668-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c668-104">SYNTAX</span></span>

### <span data-ttu-id="9c668-105">GetByGatewayId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c668-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c668-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="9c668-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c668-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c668-107">DESCRIPTION</span></span>
<span data-ttu-id="9c668-108">Cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** получает всю или определенную конфигурацию имени хоста для существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="9c668-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="9c668-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c668-109">EXAMPLES</span></span>

### <span data-ttu-id="9c668-110">Пример 1. Получить все конфигурации имен хостов для шлюза</span><span class="sxs-lookup"><span data-stu-id="9c668-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="9c668-111">Эта команда получает все конфигурации имен хостов для шлюза 0123456789.</span><span class="sxs-lookup"><span data-stu-id="9c668-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="9c668-112">Пример 2. Настройка имени пользователя для шлюза</span><span class="sxs-lookup"><span data-stu-id="9c668-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="9c668-113">Эта команда получает конфигурацию 123 имени хоста для шлюза 0123456789.</span><span class="sxs-lookup"><span data-stu-id="9c668-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="9c668-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c668-114">PARAMETERS</span></span>

### <span data-ttu-id="9c668-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9c668-115">-Context</span></span>
<span data-ttu-id="9c668-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9c668-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9c668-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9c668-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9c668-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c668-118">-DefaultProfile</span></span>
<span data-ttu-id="9c668-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c668-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c668-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9c668-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="9c668-121">Идентификатор конфигурации hostname.</span><span class="sxs-lookup"><span data-stu-id="9c668-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="9c668-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9c668-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="9c668-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9c668-123">-GatewayId</span></span>
<span data-ttu-id="9c668-124">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="9c668-124">Gateway identifier.</span></span>
<span data-ttu-id="9c668-125">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9c668-125">This parameter is required.</span></span>

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

### <span data-ttu-id="9c668-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c668-126">CommonParameters</span></span>
<span data-ttu-id="9c668-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c668-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c668-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c668-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c668-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c668-129">INPUTS</span></span>

### <span data-ttu-id="9c668-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9c668-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c668-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9c668-131">System.String</span></span>

## <span data-ttu-id="9c668-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c668-132">OUTPUTS</span></span>

### <span data-ttu-id="9c668-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c668-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="9c668-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c668-134">NOTES</span></span>

## <span data-ttu-id="9c668-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c668-135">RELATED LINKS</span></span>
