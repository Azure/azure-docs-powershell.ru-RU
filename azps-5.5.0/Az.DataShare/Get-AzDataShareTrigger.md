---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234609"
---
# <span data-ttu-id="76a2e-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="76a2e-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="76a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="76a2e-103">Получает сведения о триггере в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="76a2e-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="76a2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76a2e-104">SYNTAX</span></span>

### <span data-ttu-id="76a2e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76a2e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76a2e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76a2e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76a2e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a2e-107">DESCRIPTION</span></span>
<span data-ttu-id="76a2e-108">С **его учетной** записью можно получить сведения о триггере для подписки на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="76a2e-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="76a2e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76a2e-109">EXAMPLES</span></span>

### <span data-ttu-id="76a2e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76a2e-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="76a2e-111">Эта команда получает сведения о триггере AdsTrigger для обмена подпиской AdsShareSubscription в wikiAds учетной записи обмена данными.</span><span class="sxs-lookup"><span data-stu-id="76a2e-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="76a2e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a2e-112">PARAMETERS</span></span>

### <span data-ttu-id="76a2e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76a2e-113">-AccountName</span></span>
<span data-ttu-id="76a2e-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="76a2e-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a2e-115">-DefaultProfile</span></span>
<span data-ttu-id="76a2e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a2e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a2e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="76a2e-117">-Name</span></span>
<span data-ttu-id="76a2e-118">Имя триггера передачи данных Azure</span><span class="sxs-lookup"><span data-stu-id="76a2e-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a2e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a2e-119">-ResourceGroupName</span></span>
<span data-ttu-id="76a2e-120">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="76a2e-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a2e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76a2e-121">-ResourceId</span></span>
<span data-ttu-id="76a2e-122">ИД ресурса триггера</span><span class="sxs-lookup"><span data-stu-id="76a2e-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a2e-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="76a2e-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="76a2e-124">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="76a2e-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a2e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a2e-125">CommonParameters</span></span>
<span data-ttu-id="76a2e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a2e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a2e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76a2e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a2e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76a2e-128">INPUTS</span></span>

### <span data-ttu-id="76a2e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="76a2e-129">System.String</span></span>

## <span data-ttu-id="76a2e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76a2e-130">OUTPUTS</span></span>

### <span data-ttu-id="76a2e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="76a2e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="76a2e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76a2e-132">NOTES</span></span>

## <span data-ttu-id="76a2e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a2e-133">RELATED LINKS</span></span>
