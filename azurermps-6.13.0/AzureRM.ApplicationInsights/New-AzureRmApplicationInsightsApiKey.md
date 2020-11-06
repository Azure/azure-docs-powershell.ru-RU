---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: c60caa54f11fb2466631cf956cdc374b72265443
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561216"
---
# <span data-ttu-id="dca54-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="dca54-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="dca54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dca54-102">SYNOPSIS</span></span>
<span data-ttu-id="dca54-103">Создание ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="dca54-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dca54-104">SYNTAX</span></span>

### <span data-ttu-id="dca54-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dca54-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca54-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca54-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca54-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dca54-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca54-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dca54-108">DESCRIPTION</span></span>
<span data-ttu-id="dca54-109">Создание ключей API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="dca54-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="dca54-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dca54-110">EXAMPLES</span></span>

### <span data-ttu-id="dca54-111">Пример 1. Создайте новый ключ API для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dca54-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="dca54-112">Создание описания ключа API Application Insights как "testapiKey" с разрешениями "ReadTelemetry", "WriteAnnotations" для ресурсов "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="dca54-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="dca54-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dca54-113">PARAMETERS</span></span>

### <span data-ttu-id="dca54-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dca54-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="dca54-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dca54-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca54-116">-DefaultProfile</span></span>
<span data-ttu-id="dca54-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dca54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca54-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="dca54-118">-Description</span></span>
<span data-ttu-id="dca54-119">Описание, которое поможет идентифицировать этот ключ API.</span><span class="sxs-lookup"><span data-stu-id="dca54-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dca54-120">-Name</span></span>
<span data-ttu-id="dca54-121">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="dca54-121">Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="dca54-122">-Permissions</span></span>
<span data-ttu-id="dca54-123">Разрешения, которые ключ API разрешают для приложений.</span><span class="sxs-lookup"><span data-stu-id="dca54-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca54-124">-ResourceGroupName</span></span>
<span data-ttu-id="dca54-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dca54-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dca54-126">-ResourceId</span></span>
<span data-ttu-id="dca54-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="dca54-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca54-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dca54-128">-Confirm</span></span>
<span data-ttu-id="dca54-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dca54-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca54-130">-WhatIf</span></span>
<span data-ttu-id="dca54-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dca54-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dca54-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dca54-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca54-133">CommonParameters</span></span>
<span data-ttu-id="dca54-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dca54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca54-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca54-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca54-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dca54-136">INPUTS</span></span>

### <span data-ttu-id="dca54-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dca54-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="dca54-138">Параметры: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dca54-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="dca54-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dca54-139">System.String</span></span>

## <span data-ttu-id="dca54-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dca54-140">OUTPUTS</span></span>

### <span data-ttu-id="dca54-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="dca54-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="dca54-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="dca54-142">NOTES</span></span>

## <span data-ttu-id="dca54-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dca54-143">RELATED LINKS</span></span>
