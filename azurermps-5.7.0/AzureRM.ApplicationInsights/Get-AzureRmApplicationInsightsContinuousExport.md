---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566251"
---
# <span data-ttu-id="31d2a-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="31d2a-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="31d2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="31d2a-103">Получение конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="31d2a-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31d2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31d2a-104">SYNTAX</span></span>

### <span data-ttu-id="31d2a-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31d2a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31d2a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d2a-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31d2a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d2a-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d2a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="31d2a-109">Получение конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="31d2a-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="31d2a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31d2a-110">EXAMPLES</span></span>

### <span data-ttu-id="31d2a-111">Пример 1. Получение непрерывного экспорта для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="31d2a-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="31d2a-112">Получение конфигураций непрерывного экспорта данных Application Insights для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="31d2a-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="31d2a-113">Пример 2 Получение непрерывного экспорта для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="31d2a-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="31d2a-114">Получение конфигурации "непрерывное экспорт" для Application Insights с идентификатором экспорта "ZJrfffySPdtG3ESn3iRxVIEFuNY =" для ресурса с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="31d2a-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="31d2a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31d2a-115">PARAMETERS</span></span>

### <span data-ttu-id="31d2a-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="31d2a-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="31d2a-117">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31d2a-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="31d2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d2a-118">-DefaultProfile</span></span>
<span data-ttu-id="31d2a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31d2a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d2a-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="31d2a-120">-ExportId</span></span>
<span data-ttu-id="31d2a-121">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31d2a-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d2a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31d2a-122">-Name</span></span>
<span data-ttu-id="31d2a-123">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31d2a-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="31d2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="31d2a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31d2a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="31d2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31d2a-126">-ResourceId</span></span>
<span data-ttu-id="31d2a-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="31d2a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="31d2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d2a-128">CommonParameters</span></span>
<span data-ttu-id="31d2a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31d2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d2a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d2a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d2a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31d2a-131">INPUTS</span></span>

### <span data-ttu-id="31d2a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31d2a-132">System.String</span></span>

## <span data-ttu-id="31d2a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d2a-133">OUTPUTS</span></span>

### <span data-ttu-id="31d2a-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="31d2a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="31d2a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="31d2a-135">NOTES</span></span>

## <span data-ttu-id="31d2a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31d2a-136">RELATED LINKS</span></span>

