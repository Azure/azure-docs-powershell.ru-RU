---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244447"
---
# <span data-ttu-id="7fb8b-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7fb8b-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="7fb8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fb8b-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb8b-103">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-103">Creates a new activity log profile.</span></span> <span data-ttu-id="7fb8b-104">Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="7fb8b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fb8b-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb8b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb8b-106">DESCRIPTION</span></span>
<span data-ttu-id="7fb8b-107">Командлет **Add-AzLogProfile** создает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="7fb8b-108">**Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="7fb8b-109">Возможно, он либо имеет тип ARM, либо классический.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="7fb8b-110">Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="7fb8b-111">На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="7fb8b-112">**Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="7fb8b-113">Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="7fb8b-114">В журнале активности события могут относиться к региону или быть "глобальным".</span><span class="sxs-lookup"><span data-stu-id="7fb8b-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="7fb8b-115">Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="7fb8b-116">Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="7fb8b-117">При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="7fb8b-118">**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="7fb8b-119">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7fb8b-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fb8b-120">EXAMPLES</span></span>

### <span data-ttu-id="7fb8b-121">Пример 1: Добавление нового профиля журнала для экспорта журнала активности, соответствующего условию расположения, в учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7fb8b-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="7fb8b-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7fb8b-122">Example 2</span></span>

<span data-ttu-id="7fb8b-123">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-123">Creates a new activity log profile.</span></span> <span data-ttu-id="7fb8b-124">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="7fb8b-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="7fb8b-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fb8b-125">PARAMETERS</span></span>

### <span data-ttu-id="7fb8b-126">-Категория</span><span class="sxs-lookup"><span data-stu-id="7fb8b-126">-Category</span></span>
<span data-ttu-id="7fb8b-127">Указывает список категорий.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="7fb8b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb8b-128">-DefaultProfile</span></span>
<span data-ttu-id="7fb8b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7fb8b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb8b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="7fb8b-130">-Location</span></span>
<span data-ttu-id="7fb8b-131">Указывает расположение профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="7fb8b-132">Допустимые значения. чтобы получить актуальный список расположений, выполните указанные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="7fb8b-133">Get-AzLocation | Выберите DisplayName</span><span class="sxs-lookup"><span data-stu-id="7fb8b-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="7fb8b-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fb8b-134">-Name</span></span>
<span data-ttu-id="7fb8b-135">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7fb8b-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7fb8b-136">-RetentionInDays</span></span>
<span data-ttu-id="7fb8b-137">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="7fb8b-138">Количество дней, в течение которых журналы сохраняются в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="7fb8b-139">Чтобы сохранить данные в неизменном виде, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="7fb8b-140">Если он не указан, по умолчанию используется значение **0**.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="7fb8b-141">Для хранения данных обычно применяются нормы выставления счетов в стандартном хранилище или центрах событий.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="7fb8b-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="7fb8b-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="7fb8b-143">Указывает идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="7fb8b-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7fb8b-144">-StorageAccountId</span></span>
<span data-ttu-id="7fb8b-145">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="7fb8b-146">Идентификатор — это полный ИД ресурса для учетной записи хранения, например</span><span class="sxs-lookup"><span data-stu-id="7fb8b-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="7fb8b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="7fb8b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="7fb8b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fb8b-148">-Confirm</span></span>
<span data-ttu-id="7fb8b-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb8b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb8b-150">-WhatIf</span></span>
<span data-ttu-id="7fb8b-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb8b-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb8b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb8b-153">CommonParameters</span></span>
<span data-ttu-id="7fb8b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb8b-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb8b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb8b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fb8b-156">INPUTS</span></span>

### <span data-ttu-id="7fb8b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb8b-157">System.String</span></span>

### <span data-ttu-id="7fb8b-158">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7fb8b-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7fb8b-159">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7fb8b-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7fb8b-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb8b-160">OUTPUTS</span></span>

### <span data-ttu-id="7fb8b-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="7fb8b-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="7fb8b-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fb8b-162">NOTES</span></span>

## <span data-ttu-id="7fb8b-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fb8b-163">RELATED LINKS</span></span>

[<span data-ttu-id="7fb8b-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7fb8b-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="7fb8b-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7fb8b-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


