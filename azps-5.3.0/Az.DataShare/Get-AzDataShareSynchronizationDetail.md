---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420700"
---
# <span data-ttu-id="a3378-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="a3378-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="a3378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3378-102">SYNOPSIS</span></span>
<span data-ttu-id="a3378-103">Сведения о синхронизации для поделиться.</span><span class="sxs-lookup"><span data-stu-id="a3378-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="a3378-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3378-104">SYNTAX</span></span>

### <span data-ttu-id="a3378-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3378-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3378-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3378-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3378-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3378-107">DESCRIPTION</span></span>
<span data-ttu-id="a3378-108">**Cmdlet Get-AzDataShareSynchronizationDetail** предоставляет подробные сведения о синхронизации, начатой для поделиться.</span><span class="sxs-lookup"><span data-stu-id="a3378-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="a3378-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3378-109">EXAMPLES</span></span>

### <span data-ttu-id="a3378-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3378-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="a3378-111">Эта команда предоставляет сведения о синхронизации всех наборов данных, соответствующих предоставленному id синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a3378-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="a3378-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3378-112">PARAMETERS</span></span>

### <span data-ttu-id="a3378-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3378-113">-AccountName</span></span>
<span data-ttu-id="a3378-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="a3378-114">Azure data share account name</span></span>

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

### <span data-ttu-id="a3378-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3378-115">-DefaultProfile</span></span>
<span data-ttu-id="a3378-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3378-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3378-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3378-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3378-118">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="a3378-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a3378-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3378-119">-ResourceId</span></span>
<span data-ttu-id="a3378-120">Azure data share resource id</span><span class="sxs-lookup"><span data-stu-id="a3378-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="a3378-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a3378-121">-ShareName</span></span>
<span data-ttu-id="a3378-122">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="a3378-122">Azure data share name</span></span>

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

### <span data-ttu-id="a3378-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="a3378-123">-SynchronizationId</span></span>
<span data-ttu-id="a3378-124">Synchronization id of share synchronization</span><span class="sxs-lookup"><span data-stu-id="a3378-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3378-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3378-125">CommonParameters</span></span>
<span data-ttu-id="a3378-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3378-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3378-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3378-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3378-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3378-128">INPUTS</span></span>

### <span data-ttu-id="a3378-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a3378-129">System.String</span></span>

## <span data-ttu-id="a3378-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3378-130">OUTPUTS</span></span>

### <span data-ttu-id="a3378-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="a3378-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="a3378-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3378-132">NOTES</span></span>

## <span data-ttu-id="a3378-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3378-133">RELATED LINKS</span></span>
