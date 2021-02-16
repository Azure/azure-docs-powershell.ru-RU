---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229364"
---
# <span data-ttu-id="ae36c-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="ae36c-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="ae36c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae36c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae36c-103">Настройка непрерывного экспорта аналитики приложений для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="ae36c-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="ae36c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae36c-104">SYNTAX</span></span>

### <span data-ttu-id="ae36c-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae36c-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae36c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae36c-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae36c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae36c-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae36c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae36c-108">DESCRIPTION</span></span>
<span data-ttu-id="ae36c-109">Настройка непрерывного экспорта аналитики приложений для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="ae36c-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="ae36c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae36c-110">EXAMPLES</span></span>

### <span data-ttu-id="ae36c-111">Пример 1. Непрерывный экспорт для ресурса, анализируемго приложением</span><span class="sxs-lookup"><span data-stu-id="ae36c-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="ae36c-112">Получение статистики приложения для непрерывного экспорта для ресурса с именем "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="ae36c-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="ae36c-113">Пример 2. Непрерывный экспорт для ресурса, анализируемго приложением</span><span class="sxs-lookup"><span data-stu-id="ae36c-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="ae36c-114">Настройка непрерывного экспорта аналитики приложений с именем "ZJrfffySPdtG3ESn3iRxЯFUNY=" для ресурса с именем "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="ae36c-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ae36c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae36c-115">PARAMETERS</span></span>

### <span data-ttu-id="ae36c-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ae36c-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ae36c-117">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="ae36c-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ae36c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae36c-118">-DefaultProfile</span></span>
<span data-ttu-id="ae36c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae36c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae36c-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="ae36c-120">-ExportId</span></span>
<span data-ttu-id="ae36c-121">Application Insights Continuous Export Id.</span><span class="sxs-lookup"><span data-stu-id="ae36c-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="ae36c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ae36c-122">-Name</span></span>
<span data-ttu-id="ae36c-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ae36c-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ae36c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae36c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae36c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae36c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae36c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae36c-126">-ResourceId</span></span>
<span data-ttu-id="ae36c-127">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ae36c-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ae36c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae36c-128">CommonParameters</span></span>
<span data-ttu-id="ae36c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae36c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae36c-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae36c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae36c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae36c-131">INPUTS</span></span>

### <span data-ttu-id="ae36c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ae36c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ae36c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ae36c-133">System.String</span></span>

## <span data-ttu-id="ae36c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae36c-134">OUTPUTS</span></span>

### <span data-ttu-id="ae36c-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae36c-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="ae36c-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae36c-136">NOTES</span></span>

## <span data-ttu-id="ae36c-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae36c-137">RELATED LINKS</span></span>
