---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566248"
---
# <span data-ttu-id="2c614-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="2c614-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="2c614-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c614-102">SYNOPSIS</span></span>
<span data-ttu-id="2c614-103">Создание ключа API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="2c614-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c614-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c614-104">SYNTAX</span></span>

### <span data-ttu-id="2c614-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c614-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c614-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c614-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c614-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c614-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c614-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c614-108">DESCRIPTION</span></span>
<span data-ttu-id="2c614-109">Создание ключей API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="2c614-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="2c614-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c614-110">EXAMPLES</span></span>

### <span data-ttu-id="2c614-111">Пример 1. Создайте новый ключ API для ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2c614-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="2c614-112">Создание описания ключа API Application Insights как "testapiKey" с разрешениями "ReadTelemetry", "WriteAnnotations" для ресурсов "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="2c614-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="2c614-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c614-113">PARAMETERS</span></span>

### <span data-ttu-id="2c614-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2c614-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2c614-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2c614-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c614-116">-Confirm</span></span>
<span data-ttu-id="2c614-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c614-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c614-118">-DefaultProfile</span></span>
<span data-ttu-id="2c614-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c614-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="2c614-120">-Description</span></span>
<span data-ttu-id="2c614-121">Описание, которое поможет идентифицировать этот ключ API.</span><span class="sxs-lookup"><span data-stu-id="2c614-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c614-122">-Name</span></span>
<span data-ttu-id="2c614-123">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="2c614-123">Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="2c614-124">-Permissions</span></span>
<span data-ttu-id="2c614-125">Разрешения, которые ключ API разрешают для приложений.</span><span class="sxs-lookup"><span data-stu-id="2c614-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c614-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c614-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c614-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c614-128">-ResourceId</span></span>
<span data-ttu-id="2c614-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2c614-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c614-130">-WhatIf</span></span>
<span data-ttu-id="2c614-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c614-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c614-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c614-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c614-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c614-133">CommonParameters</span></span>
<span data-ttu-id="2c614-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c614-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c614-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c614-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c614-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c614-136">INPUTS</span></span>

### <span data-ttu-id="2c614-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2c614-137">System.String</span></span>
<span data-ttu-id="2c614-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="2c614-138">System.String[]</span></span>

## <span data-ttu-id="2c614-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c614-139">OUTPUTS</span></span>

### <span data-ttu-id="2c614-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="2c614-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="2c614-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c614-141">NOTES</span></span>

## <span data-ttu-id="2c614-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c614-142">RELATED LINKS</span></span>

