---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242814"
---
# <span data-ttu-id="b43ed-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="b43ed-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="b43ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b43ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b43ed-103">Получение сведений о параметре синхронизации для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b43ed-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="b43ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b43ed-104">SYNTAX</span></span>

### <span data-ttu-id="b43ed-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b43ed-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b43ed-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b43ed-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b43ed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43ed-107">DESCRIPTION</span></span>
<span data-ttu-id="b43ed-108">Командлет **Get-AzDataShareSynchronizationSetting** содержит сведения о синхронизации, включенные в общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b43ed-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="b43ed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b43ed-109">EXAMPLES</span></span>

### <span data-ttu-id="b43ed-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b43ed-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="b43ed-111">Эта команда предоставляет сведения о ShareSynchronizationх синхронизации, включенных для общего доступа AdsShare в разделе Учетная запись общего доступа к данным WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b43ed-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="b43ed-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b43ed-112">PARAMETERS</span></span>

### <span data-ttu-id="b43ed-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b43ed-113">-AccountName</span></span>
<span data-ttu-id="b43ed-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b43ed-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b43ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43ed-115">-DefaultProfile</span></span>
<span data-ttu-id="b43ed-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b43ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b43ed-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b43ed-117">-Name</span></span>
<span data-ttu-id="b43ed-118">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="b43ed-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="b43ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="b43ed-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b43ed-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="b43ed-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b43ed-121">-ResourceId</span></span>
<span data-ttu-id="b43ed-122">Идентификатор ресурса параметра синхронизации общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b43ed-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="b43ed-123">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="b43ed-123">-ShareName</span></span>
<span data-ttu-id="b43ed-124">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="b43ed-124">Azure data share name</span></span>

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

### <span data-ttu-id="b43ed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43ed-125">CommonParameters</span></span>
<span data-ttu-id="b43ed-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b43ed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43ed-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b43ed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43ed-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b43ed-128">INPUTS</span></span>

### <span data-ttu-id="b43ed-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b43ed-129">System.String</span></span>

## <span data-ttu-id="b43ed-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43ed-130">OUTPUTS</span></span>

### <span data-ttu-id="b43ed-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="b43ed-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="b43ed-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b43ed-132">NOTES</span></span>

## <span data-ttu-id="b43ed-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b43ed-133">RELATED LINKS</span></span>