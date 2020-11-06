---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568024"
---
# <span data-ttu-id="7cf91-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7cf91-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7cf91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cf91-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf91-103">Обновление конфигурации непрерывного экспорта в ресурсе applciation Insights</span><span class="sxs-lookup"><span data-stu-id="7cf91-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cf91-104">SYNTAX</span></span>

### <span data-ttu-id="7cf91-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cf91-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf91-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf91-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf91-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cf91-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf91-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf91-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf91-109">Обновление конфигурации непрерывного экспорта в ресурсе applciation Insights</span><span class="sxs-lookup"><span data-stu-id="7cf91-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="7cf91-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cf91-110">EXAMPLES</span></span>

### <span data-ttu-id="7cf91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7cf91-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="7cf91-112">Обновление конфигурации непрерывного экспорта "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" для ресурсов "тест" в группе ресурсов "testgroup" для экспорта "запрос" и "Трассировка" документов в контейнер хранилища "testcontainer" в "teststorageaccount". Маркер SAS должен быть допустимым и иметь разрешение на запись в контейнер, в противном случае функция непрерывного экспорта не будет работать.</span><span class="sxs-lookup"><span data-stu-id="7cf91-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="7cf91-113">Если срок действия маркера SAS истек, функция непрерывного экспорта перестанет работать.</span><span class="sxs-lookup"><span data-stu-id="7cf91-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="7cf91-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf91-114">PARAMETERS</span></span>

### <span data-ttu-id="7cf91-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7cf91-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7cf91-116">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7cf91-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7cf91-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf91-117">-Confirm</span></span>
<span data-ttu-id="7cf91-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf91-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf91-119">-DefaultProfile</span></span>
<span data-ttu-id="7cf91-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf91-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf91-121">-DisableConfiguration</span></span>
<span data-ttu-id="7cf91-122">Отключите непрерывный экспорт или нет.</span><span class="sxs-lookup"><span data-stu-id="7cf91-122">Disable continuous export or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="7cf91-123">-DocumentType</span></span>
<span data-ttu-id="7cf91-124">Типы документов, которые необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7cf91-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-125">-ExportId</span><span class="sxs-lookup"><span data-stu-id="7cf91-125">-ExportId</span></span>
<span data-ttu-id="7cf91-126">Идентификатор непрерывного экспорта Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7cf91-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cf91-127">-Name</span></span>
<span data-ttu-id="7cf91-128">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7cf91-128">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7cf91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf91-129">-ResourceGroupName</span></span>
<span data-ttu-id="7cf91-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cf91-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="7cf91-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf91-131">-ResourceId</span></span>
<span data-ttu-id="7cf91-132">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7cf91-132">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7cf91-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7cf91-133">-StorageAccountId</span></span>
<span data-ttu-id="7cf91-134">Идентификатор конечной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7cf91-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="7cf91-135">-StorageLocation</span></span>
<span data-ttu-id="7cf91-136">Идентификатор места назначения хранилища.</span><span class="sxs-lookup"><span data-stu-id="7cf91-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="7cf91-137">-StorageSASUri</span></span>
<span data-ttu-id="7cf91-138">Универсальный код ресурса SAS хранилища назначения.</span><span class="sxs-lookup"><span data-stu-id="7cf91-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf91-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf91-139">-WhatIf</span></span>
<span data-ttu-id="7cf91-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf91-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cf91-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cf91-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf91-142">CommonParameters</span></span>
<span data-ttu-id="7cf91-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cf91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf91-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf91-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf91-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cf91-145">INPUTS</span></span>

### <span data-ttu-id="7cf91-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf91-146">System.String</span></span>
<span data-ttu-id="7cf91-147">System. String [] System. Boolean.</span><span class="sxs-lookup"><span data-stu-id="7cf91-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="7cf91-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf91-148">OUTPUTS</span></span>

### <span data-ttu-id="7cf91-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf91-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="7cf91-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cf91-150">NOTES</span></span>

## <span data-ttu-id="7cf91-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf91-151">RELATED LINKS</span></span>

