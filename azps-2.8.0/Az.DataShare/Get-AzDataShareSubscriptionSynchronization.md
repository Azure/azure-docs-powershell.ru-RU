---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721196"
---
# <span data-ttu-id="62244-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="62244-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="62244-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62244-102">SYNOPSIS</span></span>
<span data-ttu-id="62244-103">Получение сведений о выполнении синхронизации через подписку на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="62244-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="62244-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62244-104">SYNTAX</span></span>

### <span data-ttu-id="62244-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62244-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62244-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62244-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62244-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62244-107">DESCRIPTION</span></span>
<span data-ttu-id="62244-108">Командлет **Get-AzDataShareSubscriptionSynchronization** предоставляет informaiton обо всех возможностях синхронизации в общей подписке с учетной записью общего доступа к данным на потребителе.</span><span class="sxs-lookup"><span data-stu-id="62244-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="62244-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62244-109">EXAMPLES</span></span>

### <span data-ttu-id="62244-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62244-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="62244-111">Эта команда предоставляет сведения обо всех возможностях синхронизации для общей подписки AdsShareSubscription в разделе "учетная запись для общего доступа к данным" WikiAds.</span><span class="sxs-lookup"><span data-stu-id="62244-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="62244-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62244-112">PARAMETERS</span></span>

### <span data-ttu-id="62244-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="62244-113">-AccountName</span></span>
<span data-ttu-id="62244-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="62244-114">Azure data share account name</span></span>

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

### <span data-ttu-id="62244-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62244-115">-DefaultProfile</span></span>
<span data-ttu-id="62244-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62244-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62244-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62244-117">-ResourceGroupName</span></span>
<span data-ttu-id="62244-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="62244-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="62244-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62244-119">-ResourceId</span></span>
<span data-ttu-id="62244-120">Идентификатор ресурса подписки на Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="62244-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="62244-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="62244-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="62244-122">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="62244-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="62244-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62244-123">CommonParameters</span></span>
<span data-ttu-id="62244-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62244-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62244-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62244-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62244-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62244-126">INPUTS</span></span>

### <span data-ttu-id="62244-127">System. String</span><span class="sxs-lookup"><span data-stu-id="62244-127">System.String</span></span>

## <span data-ttu-id="62244-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62244-128">OUTPUTS</span></span>

### <span data-ttu-id="62244-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="62244-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="62244-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="62244-130">NOTES</span></span>

## <span data-ttu-id="62244-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62244-131">RELATED LINKS</span></span>
