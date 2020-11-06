---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569020"
---
# <span data-ttu-id="2d142-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d142-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="2d142-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d142-102">SYNOPSIS</span></span>
<span data-ttu-id="2d142-103">Создание нового профиля журнала активности.</span><span class="sxs-lookup"><span data-stu-id="2d142-103">Creates a new activity log profile.</span></span> <span data-ttu-id="2d142-104">Этот профиль используется для архивации журнала активности в учетную запись хранения Azure или потоковой передачи в центр событий Azure в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="2d142-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d142-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d142-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d142-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d142-106">DESCRIPTION</span></span>
<span data-ttu-id="2d142-107">Командлет **Add-AzureRmLogProfile** создает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="2d142-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="2d142-108">**Учетная** запись хранилища (учетная запись хранилища Premium не поддерживается) поддерживается только для стандартной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d142-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="2d142-109">Возможно, он либо имеет тип ARM, либо классический.</span><span class="sxs-lookup"><span data-stu-id="2d142-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="2d142-110">Если он зарегистрирован в учетной записи хранения, стоимость хранения журнала активности оплачивается по обычным стандартным тарифам на хранение.</span><span class="sxs-lookup"><span data-stu-id="2d142-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="2d142-111">На каждую подписку может быть одновременно задан только один профиль, но для экспорта журнала активности можно использовать только одну учетную запись хранения на подписку.</span><span class="sxs-lookup"><span data-stu-id="2d142-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="2d142-112">**Центр событий** — для экспорта журнала активности может использоваться только один центр событий на каждую подписку.</span><span class="sxs-lookup"><span data-stu-id="2d142-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="2d142-113">Если журнал активности является потоком для концентратора событий, применяются стандартные цены центра событий.</span><span class="sxs-lookup"><span data-stu-id="2d142-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="2d142-114">В журнале активности события могут относиться к региону или быть "глобальным".</span><span class="sxs-lookup"><span data-stu-id="2d142-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="2d142-115">Глобально, это означает, что эти события не зависят от региона и не зависят от региона, в большинстве событий — в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="2d142-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="2d142-116">Если профиль журнала активности задан на портале, он неявно добавляет "Global" вместе с любым другим регионом, выбранным в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="2d142-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="2d142-117">При использовании командлета расположение как "Global" должно быть явно упомянуто отдельно от любого другого региона.</span><span class="sxs-lookup"><span data-stu-id="2d142-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="2d142-118">**Примечание** . Если **вы не можете установить "Global" в указанных ниже областях, это приведет к тому, что журнал активности не будет экспортирован.**</span><span class="sxs-lookup"><span data-stu-id="2d142-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="2d142-119">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="2d142-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2d142-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d142-120">EXAMPLES</span></span>

### <span data-ttu-id="2d142-121">Пример 1: Добавление нового профиля журнала для экспорта журнала активности, соответствующего условию расположения, в учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2d142-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="2d142-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d142-122">PARAMETERS</span></span>

### <span data-ttu-id="2d142-123">-Категория</span><span class="sxs-lookup"><span data-stu-id="2d142-123">-Category</span></span>
<span data-ttu-id="2d142-124">Указывает список категорий.</span><span class="sxs-lookup"><span data-stu-id="2d142-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d142-125">-DefaultProfile</span></span>
<span data-ttu-id="2d142-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d142-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d142-127">-Location</span><span class="sxs-lookup"><span data-stu-id="2d142-127">-Location</span></span>
<span data-ttu-id="2d142-128">Указывает расположение профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="2d142-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="2d142-129">Допустимые значения. чтобы получить актуальный список расположений, выполните указанные ниже командлеты.</span><span class="sxs-lookup"><span data-stu-id="2d142-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="2d142-130">Get-AzureLocation | Выберите DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d142-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d142-131">-Name</span></span>
<span data-ttu-id="2d142-132">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="2d142-132">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2d142-133">-RetentionInDays</span></span>
<span data-ttu-id="2d142-134">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="2d142-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="2d142-135">Количество дней, в течение которых журналы сохраняются в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d142-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="2d142-136">Чтобы сохранить данные в неизменном виде, установите для него значение **0**.</span><span class="sxs-lookup"><span data-stu-id="2d142-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="2d142-137">Если он не указан, по умолчанию используется значение **0**.</span><span class="sxs-lookup"><span data-stu-id="2d142-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="2d142-138">Для хранения данных обычно применяются нормы выставления счетов в стандартном хранилище или центрах событий.</span><span class="sxs-lookup"><span data-stu-id="2d142-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2d142-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="2d142-140">Указывает идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="2d142-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d142-141">-StorageAccountId</span></span>
<span data-ttu-id="2d142-142">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d142-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="2d142-143">Идентификатор — это полный ИД ресурса для учетной записи хранения, например</span><span class="sxs-lookup"><span data-stu-id="2d142-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="2d142-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="2d142-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d142-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d142-145">CommonParameters</span></span>
<span data-ttu-id="2d142-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d142-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d142-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d142-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d142-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d142-148">INPUTS</span></span>

### <span data-ttu-id="2d142-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="2d142-149">None</span></span>
<span data-ttu-id="2d142-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2d142-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d142-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d142-151">OUTPUTS</span></span>

### <span data-ttu-id="2d142-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d142-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="2d142-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d142-153">NOTES</span></span>

## <span data-ttu-id="2d142-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d142-154">RELATED LINKS</span></span>

[<span data-ttu-id="2d142-155">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d142-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="2d142-156">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="2d142-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


