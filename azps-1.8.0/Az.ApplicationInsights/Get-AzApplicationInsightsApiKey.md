---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: bf5051f22d06e9e248501ecfb602bd47d3faaf39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901533"
---
# <span data-ttu-id="d5d45-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="d5d45-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="d5d45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5d45-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d45-103">Получение ключей API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d5d45-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="d5d45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5d45-104">SYNTAX</span></span>

### <span data-ttu-id="d5d45-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5d45-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d45-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d45-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d45-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d45-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d45-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d45-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d45-109">Получение ключей API Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d5d45-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="d5d45-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5d45-110">EXAMPLES</span></span>

### <span data-ttu-id="d5d45-111">Пример 1 получение ключей API для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d5d45-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="d5d45-112">Получение ключей API Application Insights для ресурсов "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="d5d45-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="d5d45-113">Пример 2. получить конкретный ключ API для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="d5d45-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="d5d45-114">Получить конкретный ключ API Application Insights с идентификатором "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для ресурса "тест" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="d5d45-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="d5d45-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5d45-115">PARAMETERS</span></span>

### <span data-ttu-id="d5d45-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="d5d45-116">-ApiKeyId</span></span>
<span data-ttu-id="d5d45-117">Идентификатор ключа API Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d5d45-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="d5d45-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d5d45-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d5d45-119">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d5d45-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d5d45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d45-120">-DefaultProfile</span></span>
<span data-ttu-id="d5d45-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d45-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d45-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5d45-122">-Name</span></span>
<span data-ttu-id="d5d45-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d5d45-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d5d45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d45-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5d45-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5d45-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d5d45-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d45-126">-ResourceId</span></span>
<span data-ttu-id="d5d45-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d5d45-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d5d45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d45-128">CommonParameters</span></span>
<span data-ttu-id="d5d45-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5d45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d45-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d45-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d45-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5d45-131">INPUTS</span></span>

### <span data-ttu-id="d5d45-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d5d45-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="d5d45-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d45-133">System.String</span></span>

## <span data-ttu-id="d5d45-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d45-134">OUTPUTS</span></span>

### <span data-ttu-id="d5d45-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="d5d45-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="d5d45-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5d45-136">NOTES</span></span>

## <span data-ttu-id="d5d45-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5d45-137">RELATED LINKS</span></span>
