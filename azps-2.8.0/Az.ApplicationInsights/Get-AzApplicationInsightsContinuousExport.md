---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: e6e1e2319ade47557ddf07f34a9371a4bbd532b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727903"
---
# <span data-ttu-id="c5529-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c5529-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="c5529-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5529-102">SYNOPSIS</span></span>
<span data-ttu-id="c5529-103">Получение конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="c5529-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="c5529-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5529-104">SYNTAX</span></span>

### <span data-ttu-id="c5529-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5529-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5529-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5529-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5529-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5529-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5529-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5529-108">DESCRIPTION</span></span>
<span data-ttu-id="c5529-109">Получение конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="c5529-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="c5529-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5529-110">EXAMPLES</span></span>

### <span data-ttu-id="c5529-111">Пример 1. Получение непрерывного экспорта для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="c5529-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="c5529-112">Получение конфигураций непрерывного экспорта данных Application Insights для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="c5529-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="c5529-113">Пример 2 Получение непрерывного экспорта для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="c5529-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="c5529-114">Получение конфигурации "непрерывное экспорт" для Application Insights с идентификатором экспорта "ZJrfffySPdtG3ESn3iRxVIEFuNY =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="c5529-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c5529-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5529-115">PARAMETERS</span></span>

### <span data-ttu-id="c5529-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c5529-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c5529-117">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c5529-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c5529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5529-118">-DefaultProfile</span></span>
<span data-ttu-id="c5529-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5529-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5529-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="c5529-120">-ExportId</span></span>
<span data-ttu-id="c5529-121">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c5529-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="c5529-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5529-122">-Name</span></span>
<span data-ttu-id="c5529-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c5529-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c5529-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5529-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5529-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5529-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5529-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5529-126">-ResourceId</span></span>
<span data-ttu-id="c5529-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="c5529-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c5529-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5529-128">CommonParameters</span></span>
<span data-ttu-id="c5529-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5529-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5529-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5529-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5529-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5529-131">INPUTS</span></span>

### <span data-ttu-id="c5529-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c5529-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c5529-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c5529-133">System.String</span></span>

## <span data-ttu-id="c5529-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5529-134">OUTPUTS</span></span>

### <span data-ttu-id="c5529-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5529-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="c5529-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5529-136">NOTES</span></span>

## <span data-ttu-id="c5529-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5529-137">RELATED LINKS</span></span>
