---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 802dabc8373e1f3a97c66b9a9a7a121383b68287
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406839"
---
# <span data-ttu-id="8c2d4-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8c2d4-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8c2d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c2d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2d4-103">Получение ключей API для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="8c2d4-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8c2d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c2d4-104">SYNTAX</span></span>

### <span data-ttu-id="8c2d4-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c2d4-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c2d4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c2d4-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c2d4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c2d4-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c2d4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2d4-108">DESCRIPTION</span></span>
<span data-ttu-id="8c2d4-109">Получение ключей API для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="8c2d4-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8c2d4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c2d4-110">EXAMPLES</span></span>

### <span data-ttu-id="8c2d4-111">Пример 1. Получение ключей API для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="8c2d4-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="8c2d4-112">Получите ключи API аналитики приложений для "тестирования" ресурсов в группе ресурсов testGroup.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="8c2d4-113">Пример 2. Получение определенного ключа API для ресурса, анализного приложения</span><span class="sxs-lookup"><span data-stu-id="8c2d4-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="8c2d4-114">Получите ключ API конкретного приложения с ид "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для "test" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="8c2d4-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8c2d4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c2d4-115">PARAMETERS</span></span>

### <span data-ttu-id="8c2d4-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="8c2d4-116">-ApiKeyId</span></span>
<span data-ttu-id="8c2d4-117">ИД ключа API application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2d4-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8c2d4-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8c2d4-119">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="8c2d4-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8c2d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2d4-120">-DefaultProfile</span></span>
<span data-ttu-id="8c2d4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2d4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8c2d4-122">-Name</span></span>
<span data-ttu-id="8c2d4-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8c2d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c2d4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c2d4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c2d4-126">-ResourceId</span></span>
<span data-ttu-id="8c2d4-127">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8c2d4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2d4-128">CommonParameters</span></span>
<span data-ttu-id="8c2d4-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2d4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2d4-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2d4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2d4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c2d4-131">INPUTS</span></span>

### <span data-ttu-id="8c2d4-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8c2d4-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8c2d4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c2d4-133">System.String</span></span>

## <span data-ttu-id="8c2d4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c2d4-134">OUTPUTS</span></span>

### <span data-ttu-id="8c2d4-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="8c2d4-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="8c2d4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c2d4-136">NOTES</span></span>

## <span data-ttu-id="8c2d4-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c2d4-137">RELATED LINKS</span></span>
