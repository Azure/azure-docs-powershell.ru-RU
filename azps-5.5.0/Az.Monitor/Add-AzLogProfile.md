---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219052"
---
# <span data-ttu-id="e741b-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="e741b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e741b-102">SYNOPSIS</span></span>
<span data-ttu-id="e741b-103">Создание профиля журнала действий.</span><span class="sxs-lookup"><span data-stu-id="e741b-103">Creates a new activity log profile.</span></span> <span data-ttu-id="e741b-104">Этот профиль используется для архивирования журнала действий в учетной записи хранилища Azure или его потокового передачи в центр событий Azure по той же подписке.</span><span class="sxs-lookup"><span data-stu-id="e741b-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="e741b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e741b-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e741b-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e741b-106">DESCRIPTION</span></span>
<span data-ttu-id="e741b-107">С **его учетом** создается профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="e741b-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="e741b-108">**Учетная запись хранения** — поддерживается только стандартная учетная запись хранения (учетная запись премиум-хранилища не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="e741b-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="e741b-109">Это может быть один из ARM или классический.</span><span class="sxs-lookup"><span data-stu-id="e741b-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="e741b-110">Если журнал регистрируется в учетной записи хранения, за хранение журнала действий выставлен счет по стандартным тарифам хранилища.</span><span class="sxs-lookup"><span data-stu-id="e741b-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="e741b-111">Косвенным образом для экспорта журнала действий можно использовать только один профиль журнала на одну подписку.</span><span class="sxs-lookup"><span data-stu-id="e741b-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="e741b-112">**Центр событий.** Для экспорта журнала действий может быть только один профиль журнала на подписку.</span><span class="sxs-lookup"><span data-stu-id="e741b-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="e741b-113">Если журнал действий потоковой передачи в центр событий, будет применяться стандартная цена в Центре событий.</span><span class="sxs-lookup"><span data-stu-id="e741b-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="e741b-114">В журнале действий события могут относится к региону или могут быть "глобальными".</span><span class="sxs-lookup"><span data-stu-id="e741b-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="e741b-115">Глобально это, по сути, означает, что эти события являются мгнистическими данными регионов и не зависят от региона, фактически большинство событий попадают в эту категорию.</span><span class="sxs-lookup"><span data-stu-id="e741b-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="e741b-116">Если профиль журнала действий настроен на портале, он неявно добавляет глобальный профиль, а также любой другой регион, выбранный в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e741b-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="e741b-117">При использовании этого cmdlet расположение должно быть явно упоминаться как глобальное.</span><span class="sxs-lookup"><span data-stu-id="e741b-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="e741b-118">**Примечание.** Если не установить глобальный в расположениях, большинство журналов действий не будут **экспортироваться.**</span><span class="sxs-lookup"><span data-stu-id="e741b-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="e741b-119">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="e741b-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e741b-120">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e741b-120">EXAMPLES</span></span>

### <span data-ttu-id="e741b-121">Пример 1. Добавление нового профиля журнала для экспорта журнала действий, совпадающих с условием расположения, в учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="e741b-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="e741b-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e741b-122">Example 2</span></span>

<span data-ttu-id="e741b-123">Создание профиля журнала действий.</span><span class="sxs-lookup"><span data-stu-id="e741b-123">Creates a new activity log profile.</span></span> <span data-ttu-id="e741b-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="e741b-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="e741b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e741b-125">PARAMETERS</span></span>

### <span data-ttu-id="e741b-126">-Category</span><span class="sxs-lookup"><span data-stu-id="e741b-126">-Category</span></span>
<span data-ttu-id="e741b-127">Список категорий.</span><span class="sxs-lookup"><span data-stu-id="e741b-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="e741b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-128">-DefaultProfile</span></span>
<span data-ttu-id="e741b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e741b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e741b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e741b-130">-Location</span></span>
<span data-ttu-id="e741b-131">Определяет расположение профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="e741b-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="e741b-132">Допустимые значения: запустите под cmdlet, чтобы получить актуальный список местоположений.</span><span class="sxs-lookup"><span data-stu-id="e741b-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="e741b-133">Get-AzLocation | Выберите DisplayName</span><span class="sxs-lookup"><span data-stu-id="e741b-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="e741b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e741b-134">-Name</span></span>
<span data-ttu-id="e741b-135">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="e741b-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e741b-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e741b-136">-RetentionInDays</span></span>
<span data-ttu-id="e741b-137">Определяет политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="e741b-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="e741b-138">Это количество дней, в течение дня журналы хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e741b-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="e741b-139">Чтобы сохранить данные навсегда, установите для этого **0.**</span><span class="sxs-lookup"><span data-stu-id="e741b-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="e741b-140">Если оно не задано, по умолчанию задано **значение 0.**</span><span class="sxs-lookup"><span data-stu-id="e741b-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="e741b-141">Для хранения данных будут применяться стандартные тарифы для хранения данных или выставление счета в центре событий.</span><span class="sxs-lookup"><span data-stu-id="e741b-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="e741b-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="e741b-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="e741b-143">Определяет ИД правила обслуживания для автобусов.</span><span class="sxs-lookup"><span data-stu-id="e741b-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="e741b-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e741b-144">-StorageAccountId</span></span>
<span data-ttu-id="e741b-145">Определяет ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e741b-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="e741b-146">Например, ID — это полное ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e741b-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="e741b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="e741b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="e741b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e741b-148">-Confirm</span></span>
<span data-ttu-id="e741b-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e741b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e741b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e741b-150">-WhatIf</span></span>
<span data-ttu-id="e741b-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e741b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e741b-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e741b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e741b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e741b-153">CommonParameters</span></span>
<span data-ttu-id="e741b-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e741b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e741b-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e741b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e741b-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e741b-156">INPUTS</span></span>

### <span data-ttu-id="e741b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="e741b-157">System.String</span></span>

### <span data-ttu-id="e741b-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e741b-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e741b-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e741b-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e741b-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e741b-160">OUTPUTS</span></span>

### <span data-ttu-id="e741b-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="e741b-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e741b-162">NOTES</span></span>

## <span data-ttu-id="e741b-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e741b-163">RELATED LINKS</span></span>

[<span data-ttu-id="e741b-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="e741b-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e741b-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


