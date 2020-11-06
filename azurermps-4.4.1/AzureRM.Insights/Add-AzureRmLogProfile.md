---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569416"
---
# <span data-ttu-id="78dfd-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="78dfd-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="78dfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="78dfd-103">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="78dfd-103">Creates a new activity log profile.</span></span> <span data-ttu-id="78dfd-104">Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="78dfd-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="78dfd-105">**Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="78dfd-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="78dfd-106">Возможно, он либо имеет тип ARM, либо классический.</span><span class="sxs-lookup"><span data-stu-id="78dfd-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="78dfd-107">Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение.</span><span class="sxs-lookup"><span data-stu-id="78dfd-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="78dfd-108">На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку.</span><span class="sxs-lookup"><span data-stu-id="78dfd-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="78dfd-109">**Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку.</span><span class="sxs-lookup"><span data-stu-id="78dfd-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="78dfd-110">Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий.</span><span class="sxs-lookup"><span data-stu-id="78dfd-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="78dfd-111">В журнале активности события могут относиться к региону или быть "глобальным".</span><span class="sxs-lookup"><span data-stu-id="78dfd-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="78dfd-112">Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="78dfd-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="78dfd-113">Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="78dfd-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="78dfd-114">При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона.</span><span class="sxs-lookup"><span data-stu-id="78dfd-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="78dfd-115">**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.**</span><span class="sxs-lookup"><span data-stu-id="78dfd-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78dfd-116">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78dfd-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78dfd-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78dfd-117">DESCRIPTION</span></span>
<span data-ttu-id="78dfd-118">Командлет **Add-AzureRmLogProfile** создает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="78dfd-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="78dfd-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78dfd-119">EXAMPLES</span></span>

### <span data-ttu-id="78dfd-120">Пример 1: Добавление нового профиля журнала для экспорта журнала активности, соответствующего условию расположения, в учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="78dfd-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="78dfd-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78dfd-121">PARAMETERS</span></span>

### <span data-ttu-id="78dfd-122">-Категории</span><span class="sxs-lookup"><span data-stu-id="78dfd-122">-Categories</span></span>
<span data-ttu-id="78dfd-123">Указывает список категорий.</span><span class="sxs-lookup"><span data-stu-id="78dfd-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="78dfd-124">-Расположения</span><span class="sxs-lookup"><span data-stu-id="78dfd-124">-Locations</span></span>
<span data-ttu-id="78dfd-125">Указывает расположение профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="78dfd-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="78dfd-126">Допустимые значения. чтобы получить актуальный список расположений, выполните указанные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="78dfd-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="78dfd-127">Get-AzureLocation | Выберите DisplayName</span><span class="sxs-lookup"><span data-stu-id="78dfd-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="78dfd-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78dfd-128">-Name</span></span>
<span data-ttu-id="78dfd-129">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="78dfd-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="78dfd-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="78dfd-130">-RetentionInDays</span></span>
<span data-ttu-id="78dfd-131">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="78dfd-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="78dfd-132">Количество дней, в течение которых журналы сохраняются в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="78dfd-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="78dfd-133">Чтобы сохранить данные в неизменном виде, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="78dfd-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="78dfd-134">Если он не указан, по умолчанию используется значение **0**.</span><span class="sxs-lookup"><span data-stu-id="78dfd-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="78dfd-135">Для хранения данных обычно применяются нормы выставления счетов в стандартном хранилище или центрах событий.</span><span class="sxs-lookup"><span data-stu-id="78dfd-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="78dfd-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="78dfd-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="78dfd-137">Указывает идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="78dfd-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="78dfd-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78dfd-138">-StorageAccountId</span></span>
<span data-ttu-id="78dfd-139">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="78dfd-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="78dfd-140">Идентификатор — это полный ИД ресурса для учетной записи хранения, например</span><span class="sxs-lookup"><span data-stu-id="78dfd-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="78dfd-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="78dfd-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="78dfd-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78dfd-142">-DefaultProfile</span></span>
<span data-ttu-id="78dfd-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78dfd-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78dfd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78dfd-144">CommonParameters</span></span>
<span data-ttu-id="78dfd-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78dfd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78dfd-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78dfd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78dfd-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78dfd-147">INPUTS</span></span>

## <span data-ttu-id="78dfd-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78dfd-148">OUTPUTS</span></span>

### <span data-ttu-id="78dfd-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="78dfd-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="78dfd-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="78dfd-150">NOTES</span></span>

## <span data-ttu-id="78dfd-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78dfd-151">RELATED LINKS</span></span>

[<span data-ttu-id="78dfd-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="78dfd-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="78dfd-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="78dfd-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


