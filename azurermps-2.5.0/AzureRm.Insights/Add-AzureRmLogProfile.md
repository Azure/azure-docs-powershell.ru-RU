---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 4302aa7dbc0cf31b9a7aa61678d871e9da140d51
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913894"
---
# <span data-ttu-id="9c96c-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="9c96c-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="9c96c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c96c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c96c-103">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="9c96c-103">Creates a new activity log profile.</span></span> <span data-ttu-id="9c96c-104">Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="9c96c-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c96c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c96c-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c96c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c96c-106">DESCRIPTION</span></span>
<span data-ttu-id="9c96c-107">Командлет **Add-AzureRmLogProfile** создает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="9c96c-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="9c96c-108">**Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9c96c-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="9c96c-109">Возможно, он либо имеет тип ARM, либо классический.</span><span class="sxs-lookup"><span data-stu-id="9c96c-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="9c96c-110">Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение.</span><span class="sxs-lookup"><span data-stu-id="9c96c-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="9c96c-111">На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку.</span><span class="sxs-lookup"><span data-stu-id="9c96c-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="9c96c-112">**Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку.</span><span class="sxs-lookup"><span data-stu-id="9c96c-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="9c96c-113">Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий.</span><span class="sxs-lookup"><span data-stu-id="9c96c-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="9c96c-114">В журнале активности события могут относиться к региону или быть "глобальным".</span><span class="sxs-lookup"><span data-stu-id="9c96c-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="9c96c-115">Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="9c96c-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="9c96c-116">Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9c96c-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="9c96c-117">При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона.</span><span class="sxs-lookup"><span data-stu-id="9c96c-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="9c96c-118">**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.**</span><span class="sxs-lookup"><span data-stu-id="9c96c-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="9c96c-119">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="9c96c-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9c96c-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c96c-120">EXAMPLES</span></span>

### <span data-ttu-id="9c96c-121">Пример 1: Добавление нового профиля журнала для экспорта журнала активности, соответствующего условию расположения, в учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9c96c-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="9c96c-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c96c-122">PARAMETERS</span></span>

### <span data-ttu-id="9c96c-123">-Категория</span><span class="sxs-lookup"><span data-stu-id="9c96c-123">-Category</span></span>
<span data-ttu-id="9c96c-124">Указывает список категорий.</span><span class="sxs-lookup"><span data-stu-id="9c96c-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c96c-125">-DefaultProfile</span></span>
<span data-ttu-id="9c96c-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c96c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c96c-127">-Location</span><span class="sxs-lookup"><span data-stu-id="9c96c-127">-Location</span></span>
<span data-ttu-id="9c96c-128">Указывает расположение профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="9c96c-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="9c96c-129">Допустимые значения. чтобы получить актуальный список расположений, выполните указанные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="9c96c-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="9c96c-130">Get-AzureLocation | Выберите DisplayName</span><span class="sxs-lookup"><span data-stu-id="9c96c-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c96c-131">-Name</span></span>
<span data-ttu-id="9c96c-132">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="9c96c-132">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9c96c-133">-RetentionInDays</span></span>
<span data-ttu-id="9c96c-134">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="9c96c-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="9c96c-135">Количество дней, в течение которых журналы сохраняются в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9c96c-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="9c96c-136">Чтобы сохранить данные в неизменном виде, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="9c96c-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="9c96c-137">Если он не указан, по умолчанию используется значение **0**.</span><span class="sxs-lookup"><span data-stu-id="9c96c-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="9c96c-138">Для хранения данных обычно применяются нормы выставления счетов в стандартном хранилище или центрах событий.</span><span class="sxs-lookup"><span data-stu-id="9c96c-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="9c96c-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="9c96c-140">Указывает идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9c96c-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9c96c-141">-StorageAccountId</span></span>
<span data-ttu-id="9c96c-142">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9c96c-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="9c96c-143">Идентификатор — это полный ИД ресурса для учетной записи хранения, например</span><span class="sxs-lookup"><span data-stu-id="9c96c-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="9c96c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="9c96c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c96c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c96c-145">-Confirm</span></span>
<span data-ttu-id="9c96c-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c96c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c96c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c96c-147">-WhatIf</span></span>
<span data-ttu-id="9c96c-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c96c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c96c-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c96c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c96c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c96c-150">CommonParameters</span></span>
<span data-ttu-id="9c96c-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c96c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c96c-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c96c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c96c-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c96c-153">INPUTS</span></span>

### <span data-ttu-id="9c96c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="9c96c-154">System.String</span></span>

### <span data-ttu-id="9c96c-155">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9c96c-155">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9c96c-156">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9c96c-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9c96c-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c96c-157">OUTPUTS</span></span>

### <span data-ttu-id="9c96c-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="9c96c-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="9c96c-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c96c-159">NOTES</span></span>

## <span data-ttu-id="9c96c-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c96c-160">RELATED LINKS</span></span>

[<span data-ttu-id="9c96c-161">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="9c96c-161">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="9c96c-162">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="9c96c-162">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


