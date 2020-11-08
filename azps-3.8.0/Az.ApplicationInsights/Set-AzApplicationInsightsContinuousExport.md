---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072807"
---
# <span data-ttu-id="94b51-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="94b51-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="94b51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94b51-102">SYNOPSIS</span></span>
<span data-ttu-id="94b51-103">Обновление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="94b51-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="94b51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94b51-104">SYNTAX</span></span>

### <span data-ttu-id="94b51-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94b51-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b51-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94b51-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b51-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94b51-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b51-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94b51-108">DESCRIPTION</span></span>
<span data-ttu-id="94b51-109">Обновление конфигурации непрерывного экспорта в ресурсе Application Insights</span><span class="sxs-lookup"><span data-stu-id="94b51-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="94b51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94b51-110">EXAMPLES</span></span>

### <span data-ttu-id="94b51-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94b51-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="94b51-112">Обновление конфигурации непрерывного экспорта "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" для ресурсов "тест" в группе ресурсов "testgroup" для экспорта "запрос" и "Трассировка" документов в контейнер хранилища "testcontainer" в "teststorageaccount". Маркер SAS должен быть допустимым и иметь разрешение на запись в контейнер, в противном случае функция непрерывного экспорта не будет работать.</span><span class="sxs-lookup"><span data-stu-id="94b51-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="94b51-113">Если срок действия маркера SAS истек, функция непрерывного экспорта перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="94b51-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="94b51-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94b51-114">PARAMETERS</span></span>

### <span data-ttu-id="94b51-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="94b51-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="94b51-116">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="94b51-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="94b51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b51-117">-DefaultProfile</span></span>
<span data-ttu-id="94b51-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94b51-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94b51-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="94b51-119">-DisableConfiguration</span></span>
<span data-ttu-id="94b51-120">Отключите непрерывный экспорт или нет.</span><span class="sxs-lookup"><span data-stu-id="94b51-120">Disable continuous export or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b51-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="94b51-121">-DocumentType</span></span>
<span data-ttu-id="94b51-122">Типы документов, которые необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="94b51-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="94b51-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="94b51-123">-ExportId</span></span>
<span data-ttu-id="94b51-124">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="94b51-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="94b51-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94b51-125">-Name</span></span>
<span data-ttu-id="94b51-126">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="94b51-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="94b51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b51-127">-ResourceGroupName</span></span>
<span data-ttu-id="94b51-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94b51-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="94b51-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94b51-129">-ResourceId</span></span>
<span data-ttu-id="94b51-130">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="94b51-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="94b51-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="94b51-131">-StorageAccountId</span></span>
<span data-ttu-id="94b51-132">Идентификатор конечной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="94b51-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="94b51-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="94b51-133">-StorageLocation</span></span>
<span data-ttu-id="94b51-134">Идентификатор места назначения хранилища.</span><span class="sxs-lookup"><span data-stu-id="94b51-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="94b51-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="94b51-135">-StorageSASUri</span></span>
<span data-ttu-id="94b51-136">Универсальный код ресурса SAS хранилища назначения.</span><span class="sxs-lookup"><span data-stu-id="94b51-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="94b51-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94b51-137">-Confirm</span></span>
<span data-ttu-id="94b51-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94b51-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b51-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b51-139">-WhatIf</span></span>
<span data-ttu-id="94b51-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94b51-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94b51-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94b51-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b51-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b51-142">CommonParameters</span></span>
<span data-ttu-id="94b51-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94b51-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b51-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b51-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b51-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94b51-145">INPUTS</span></span>

### <span data-ttu-id="94b51-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="94b51-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="94b51-147">System. String</span><span class="sxs-lookup"><span data-stu-id="94b51-147">System.String</span></span>

## <span data-ttu-id="94b51-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94b51-148">OUTPUTS</span></span>

### <span data-ttu-id="94b51-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="94b51-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="94b51-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="94b51-150">NOTES</span></span>

## <span data-ttu-id="94b51-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94b51-151">RELATED LINKS</span></span>
