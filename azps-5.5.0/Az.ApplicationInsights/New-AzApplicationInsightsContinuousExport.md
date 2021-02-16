---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216340"
---
# <span data-ttu-id="e486e-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="e486e-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="e486e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e486e-102">SYNOPSIS</span></span>
<span data-ttu-id="e486e-103">Создание новой конфигурации непрерывного экспорта аналитики приложений для ресурса аналитики приложений</span><span class="sxs-lookup"><span data-stu-id="e486e-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="e486e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e486e-104">SYNTAX</span></span>

### <span data-ttu-id="e486e-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e486e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e486e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e486e-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e486e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e486e-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e486e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e486e-108">DESCRIPTION</span></span>
<span data-ttu-id="e486e-109">Создание новой конфигурации непрерывного экспорта аналитики приложений для ресурса аналитики приложений</span><span class="sxs-lookup"><span data-stu-id="e486e-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="e486e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e486e-110">EXAMPLES</span></span>

### <span data-ttu-id="e486e-111">Пример 1. Создание новой конфигурации непрерывного экспорта для ресурса аналитики приложения</span><span class="sxs-lookup"><span data-stu-id="e486e-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="e486e-112">Создайте новую конфигурацию непрерывного экспорта аналитики приложений, чтобы экспортировать документы типов "Запрос" и "Трассировка" в хранилище, содержащие "testcontainer" в учетной записи хранения "testtorageaccount" в группе ресурсов "testgroup".</span><span class="sxs-lookup"><span data-stu-id="e486e-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="e486e-113">Маркер SAS должен быть действительным и иметь разрешение на написание контейнера, иначе функция непрерывного экспорта не будет работать. Если срок действия маркера SAS истек, функция непрерывного экспорта перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="e486e-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="e486e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e486e-114">PARAMETERS</span></span>

### <span data-ttu-id="e486e-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e486e-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e486e-116">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="e486e-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e486e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e486e-117">-DefaultProfile</span></span>
<span data-ttu-id="e486e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e486e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e486e-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="e486e-119">-DocumentType</span></span>
<span data-ttu-id="e486e-120">Типы документов, которые требуется экспортировать.</span><span class="sxs-lookup"><span data-stu-id="e486e-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="e486e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e486e-121">-Name</span></span>
<span data-ttu-id="e486e-122">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="e486e-122">Component Name.</span></span>

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

### <span data-ttu-id="e486e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e486e-123">-ResourceGroupName</span></span>
<span data-ttu-id="e486e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e486e-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="e486e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e486e-125">-ResourceId</span></span>
<span data-ttu-id="e486e-126">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="e486e-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e486e-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e486e-127">-StorageAccountId</span></span>
<span data-ttu-id="e486e-128">ИД учетной записи хранения назначения.</span><span class="sxs-lookup"><span data-stu-id="e486e-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="e486e-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="e486e-129">-StorageLocation</span></span>
<span data-ttu-id="e486e-130">ИД места назначения хранилища.</span><span class="sxs-lookup"><span data-stu-id="e486e-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="e486e-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="e486e-131">-StorageSASUri</span></span>
<span data-ttu-id="e486e-132">Uri хранилища.</span><span class="sxs-lookup"><span data-stu-id="e486e-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="e486e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e486e-133">-Confirm</span></span>
<span data-ttu-id="e486e-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e486e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e486e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e486e-135">-WhatIf</span></span>
<span data-ttu-id="e486e-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e486e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e486e-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e486e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e486e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e486e-138">CommonParameters</span></span>
<span data-ttu-id="e486e-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e486e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e486e-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e486e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e486e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e486e-141">INPUTS</span></span>

### <span data-ttu-id="e486e-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e486e-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="e486e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e486e-143">System.String</span></span>

## <span data-ttu-id="e486e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e486e-144">OUTPUTS</span></span>

### <span data-ttu-id="e486e-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="e486e-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="e486e-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e486e-146">NOTES</span></span>

## <span data-ttu-id="e486e-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e486e-147">RELATED LINKS</span></span>
