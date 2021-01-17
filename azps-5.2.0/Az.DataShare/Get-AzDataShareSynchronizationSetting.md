---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324480"
---
# <span data-ttu-id="da64e-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="da64e-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="da64e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da64e-102">SYNOPSIS</span></span>
<span data-ttu-id="da64e-103">Получает сведения о параметрах синхронизации для поделиться.</span><span class="sxs-lookup"><span data-stu-id="da64e-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="da64e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da64e-104">SYNTAX</span></span>

### <span data-ttu-id="da64e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da64e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da64e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da64e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da64e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da64e-107">DESCRIPTION</span></span>
<span data-ttu-id="da64e-108">**Cmdlet Get-AzDataShareSynchronizationSetting** предоставляет сведения о том, включена ли синхронизация в share.</span><span class="sxs-lookup"><span data-stu-id="da64e-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="da64e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da64e-109">EXAMPLES</span></span>

### <span data-ttu-id="da64e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da64e-110">Example 1</span></span>
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

<span data-ttu-id="da64e-111">Эта команда предоставляет сведения о синхронизации ShareSynchronization включена при совместном доступе AdsShare в share account WikiAds учетной записи.</span><span class="sxs-lookup"><span data-stu-id="da64e-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="da64e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da64e-112">PARAMETERS</span></span>

### <span data-ttu-id="da64e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da64e-113">-AccountName</span></span>
<span data-ttu-id="da64e-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="da64e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="da64e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da64e-115">-DefaultProfile</span></span>
<span data-ttu-id="da64e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da64e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da64e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da64e-117">-Name</span></span>
<span data-ttu-id="da64e-118">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="da64e-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="da64e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da64e-119">-ResourceGroupName</span></span>
<span data-ttu-id="da64e-120">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="da64e-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="da64e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da64e-121">-ResourceId</span></span>
<span data-ttu-id="da64e-122">ИД ресурса в параметре синхронизации обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="da64e-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="da64e-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="da64e-123">-ShareName</span></span>
<span data-ttu-id="da64e-124">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="da64e-124">Azure data share name</span></span>

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

### <span data-ttu-id="da64e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da64e-125">CommonParameters</span></span>
<span data-ttu-id="da64e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da64e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da64e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da64e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da64e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da64e-128">INPUTS</span></span>

### <span data-ttu-id="da64e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="da64e-129">System.String</span></span>

## <span data-ttu-id="da64e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da64e-130">OUTPUTS</span></span>

### <span data-ttu-id="da64e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="da64e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="da64e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da64e-132">NOTES</span></span>

## <span data-ttu-id="da64e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da64e-133">RELATED LINKS</span></span>
