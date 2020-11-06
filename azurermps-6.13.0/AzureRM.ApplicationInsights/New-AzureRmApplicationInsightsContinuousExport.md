---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 73aa26491a86b0eba01adb3898dba803f1ecf0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561211"
---
# <span data-ttu-id="291ed-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="291ed-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="291ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="291ed-102">SYNOPSIS</span></span>
<span data-ttu-id="291ed-103">Создание конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="291ed-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="291ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="291ed-104">SYNTAX</span></span>

### <span data-ttu-id="291ed-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="291ed-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291ed-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="291ed-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="291ed-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="291ed-108">DESCRIPTION</span></span>
<span data-ttu-id="291ed-109">Создание конфигурации непрерывного экспорта данных Application Insights для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="291ed-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="291ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="291ed-110">EXAMPLES</span></span>

### <span data-ttu-id="291ed-111">Пример 1. Создание новой конфигурации непрерывного экспорта для ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="291ed-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="291ed-112">Создание новой конфигурации "непрерывное экспорт приложения" для экспорта "запрос" и "Трассировка" типы документов в хранилище содержат "testcontainer" в учетной записи хранения "teststorageaccount" в группе ресурсов "testgroup".</span><span class="sxs-lookup"><span data-stu-id="291ed-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="291ed-113">Маркер SAS должен быть допустимым и иметь разрешение на запись в контейнер, в противном случае функция непрерывного экспорта не будет работать. Если срок действия маркера SAS истек, функция непрерывного экспорта перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="291ed-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="291ed-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="291ed-114">PARAMETERS</span></span>

### <span data-ttu-id="291ed-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="291ed-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="291ed-116">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="291ed-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="291ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291ed-117">-DefaultProfile</span></span>
<span data-ttu-id="291ed-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="291ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="291ed-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="291ed-119">-DocumentType</span></span>
<span data-ttu-id="291ed-120">Типы документов, которые необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="291ed-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ed-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="291ed-121">-Name</span></span>
<span data-ttu-id="291ed-122">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="291ed-122">Component Name.</span></span>

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

### <span data-ttu-id="291ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="291ed-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="291ed-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="291ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="291ed-125">-ResourceId</span></span>
<span data-ttu-id="291ed-126">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="291ed-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="291ed-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="291ed-127">-StorageAccountId</span></span>
<span data-ttu-id="291ed-128">Идентификатор конечной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="291ed-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ed-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="291ed-129">-StorageLocation</span></span>
<span data-ttu-id="291ed-130">Идентификатор места назначения хранилища.</span><span class="sxs-lookup"><span data-stu-id="291ed-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ed-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="291ed-131">-StorageSASUri</span></span>
<span data-ttu-id="291ed-132">Универсальный код ресурса SAS хранилища назначения.</span><span class="sxs-lookup"><span data-stu-id="291ed-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291ed-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="291ed-133">-Confirm</span></span>
<span data-ttu-id="291ed-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="291ed-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291ed-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291ed-135">-WhatIf</span></span>
<span data-ttu-id="291ed-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="291ed-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="291ed-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="291ed-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291ed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291ed-138">CommonParameters</span></span>
<span data-ttu-id="291ed-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="291ed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291ed-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291ed-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291ed-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="291ed-141">INPUTS</span></span>

### <span data-ttu-id="291ed-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="291ed-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="291ed-143">Параметры: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="291ed-143">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="291ed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="291ed-144">System.String</span></span>

## <span data-ttu-id="291ed-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="291ed-145">OUTPUTS</span></span>

### <span data-ttu-id="291ed-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="291ed-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="291ed-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="291ed-147">NOTES</span></span>

## <span data-ttu-id="291ed-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="291ed-148">RELATED LINKS</span></span>
