---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390868"
---
# <span data-ttu-id="169bd-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="169bd-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="169bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="169bd-102">SYNOPSIS</span></span>
<span data-ttu-id="169bd-103">Сведения о параметрах синхронизации для поделиться.</span><span class="sxs-lookup"><span data-stu-id="169bd-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="169bd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="169bd-104">SYNTAX</span></span>

### <span data-ttu-id="169bd-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="169bd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="169bd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="169bd-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="169bd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="169bd-107">DESCRIPTION</span></span>
<span data-ttu-id="169bd-108">**Cmdlet Get-AzDataShareSynchronization** предоставляет сведения обо всех параметрах синхронизации, которые есть в обойте в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="169bd-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="169bd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="169bd-109">EXAMPLES</span></span>

### <span data-ttu-id="169bd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="169bd-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="169bd-111">Эти команды предоставляют сведения обо всех параметрах синхронизации, присутствующих в share AdsShare в учетной записи вики-центрах обмена данными.</span><span class="sxs-lookup"><span data-stu-id="169bd-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="169bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="169bd-112">PARAMETERS</span></span>

### <span data-ttu-id="169bd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="169bd-113">-AccountName</span></span>
<span data-ttu-id="169bd-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="169bd-114">Azure data share account name</span></span>

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

### <span data-ttu-id="169bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169bd-115">-DefaultProfile</span></span>
<span data-ttu-id="169bd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="169bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="169bd-118">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="169bd-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="169bd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="169bd-119">-ResourceId</span></span>
<span data-ttu-id="169bd-120">Azure data share resource id</span><span class="sxs-lookup"><span data-stu-id="169bd-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="169bd-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="169bd-121">-ShareName</span></span>
<span data-ttu-id="169bd-122">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="169bd-122">Azure data share name</span></span>

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

### <span data-ttu-id="169bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169bd-123">CommonParameters</span></span>
<span data-ttu-id="169bd-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169bd-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="169bd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169bd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="169bd-126">INPUTS</span></span>

### <span data-ttu-id="169bd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="169bd-127">System.String</span></span>

## <span data-ttu-id="169bd-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="169bd-128">OUTPUTS</span></span>

### <span data-ttu-id="169bd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="169bd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="169bd-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="169bd-130">NOTES</span></span>

## <span data-ttu-id="169bd-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="169bd-131">RELATED LINKS</span></span>
