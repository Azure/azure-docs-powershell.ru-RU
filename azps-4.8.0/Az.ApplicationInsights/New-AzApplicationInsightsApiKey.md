---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080104"
---
# <span data-ttu-id="55a49-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="55a49-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="55a49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55a49-102">SYNOPSIS</span></span>
<span data-ttu-id="55a49-103">Создание ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="55a49-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="55a49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55a49-104">SYNTAX</span></span>

### <span data-ttu-id="55a49-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55a49-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a49-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a49-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a49-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55a49-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a49-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a49-108">DESCRIPTION</span></span>
<span data-ttu-id="55a49-109">Создание ключей API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="55a49-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="55a49-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55a49-110">EXAMPLES</span></span>

### <span data-ttu-id="55a49-111">Пример 1. Создайте новый ключ API для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="55a49-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="55a49-112">Создание описания ключа API Application Insights как "testapiKey" с разрешениями "ReadTelemetry", "WriteAnnotations" для ресурсов "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="55a49-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="55a49-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55a49-113">PARAMETERS</span></span>

### <span data-ttu-id="55a49-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="55a49-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="55a49-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="55a49-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="55a49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a49-116">-DefaultProfile</span></span>
<span data-ttu-id="55a49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55a49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55a49-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="55a49-118">-Description</span></span>
<span data-ttu-id="55a49-119">Описание, которое поможет идентифицировать этот ключ API.</span><span class="sxs-lookup"><span data-stu-id="55a49-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="55a49-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55a49-120">-Name</span></span>
<span data-ttu-id="55a49-121">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="55a49-121">Component Name.</span></span>

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

### <span data-ttu-id="55a49-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="55a49-122">-Permissions</span></span>
<span data-ttu-id="55a49-123">Разрешения, которые ключ API разрешают для приложений.</span><span class="sxs-lookup"><span data-stu-id="55a49-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="55a49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a49-124">-ResourceGroupName</span></span>
<span data-ttu-id="55a49-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55a49-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="55a49-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55a49-126">-ResourceId</span></span>
<span data-ttu-id="55a49-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="55a49-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="55a49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55a49-128">-Confirm</span></span>
<span data-ttu-id="55a49-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55a49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a49-130">-WhatIf</span></span>
<span data-ttu-id="55a49-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55a49-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55a49-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55a49-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a49-133">CommonParameters</span></span>
<span data-ttu-id="55a49-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55a49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a49-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a49-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a49-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55a49-136">INPUTS</span></span>

### <span data-ttu-id="55a49-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="55a49-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="55a49-138">System. String</span><span class="sxs-lookup"><span data-stu-id="55a49-138">System.String</span></span>

## <span data-ttu-id="55a49-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a49-139">OUTPUTS</span></span>

### <span data-ttu-id="55a49-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="55a49-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="55a49-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="55a49-141">NOTES</span></span>

## <span data-ttu-id="55a49-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55a49-142">RELATED LINKS</span></span>
