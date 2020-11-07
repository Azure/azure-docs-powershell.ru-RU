---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 3d907295a862ee88d44db54ed3b0cd85b104fbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721187"
---
# <span data-ttu-id="b8955-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b8955-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="b8955-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8955-102">SYNOPSIS</span></span>
<span data-ttu-id="b8955-103">Получение сведений о триггере в подписке "общий доступ".</span><span class="sxs-lookup"><span data-stu-id="b8955-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="b8955-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8955-104">SYNTAX</span></span>

### <span data-ttu-id="b8955-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8955-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8955-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8955-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8955-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8955-107">DESCRIPTION</span></span>
<span data-ttu-id="b8955-108">Командлет **Get-AzDataShareTrigger** получает сведения о триггере "общий доступ к подписке" для общей учетной записи данных.</span><span class="sxs-lookup"><span data-stu-id="b8955-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="b8955-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8955-109">EXAMPLES</span></span>

### <span data-ttu-id="b8955-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8955-110">Example 1</span></span>
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

<span data-ttu-id="b8955-111">Эта команда получает сведения о триггере AdsTrigger для предоставления общего доступа к подписке AdsShareSubscription в разделе Учетная запись общего доступа к данным WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b8955-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="b8955-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8955-112">PARAMETERS</span></span>

### <span data-ttu-id="b8955-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b8955-113">-AccountName</span></span>
<span data-ttu-id="b8955-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b8955-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b8955-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8955-115">-DefaultProfile</span></span>
<span data-ttu-id="b8955-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8955-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8955-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8955-117">-Name</span></span>
<span data-ttu-id="b8955-118">Имя триггера общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b8955-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b8955-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8955-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8955-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b8955-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b8955-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8955-121">-ResourceId</span></span>
<span data-ttu-id="b8955-122">Идентификатор ресурса триггера.</span><span class="sxs-lookup"><span data-stu-id="b8955-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="b8955-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b8955-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="b8955-124">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b8955-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b8955-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8955-125">CommonParameters</span></span>
<span data-ttu-id="b8955-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8955-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8955-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8955-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8955-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8955-128">INPUTS</span></span>

### <span data-ttu-id="b8955-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8955-129">System.String</span></span>

## <span data-ttu-id="b8955-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8955-130">OUTPUTS</span></span>

### <span data-ttu-id="b8955-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b8955-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="b8955-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8955-132">NOTES</span></span>

## <span data-ttu-id="b8955-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8955-133">RELATED LINKS</span></span>
