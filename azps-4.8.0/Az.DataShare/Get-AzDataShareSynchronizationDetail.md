---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077828"
---
# <span data-ttu-id="c91b6-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c91b6-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="c91b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c91b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c91b6-103">Получение сведений о сведениях о синхронизации для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c91b6-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="c91b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c91b6-104">SYNTAX</span></span>

### <span data-ttu-id="c91b6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c91b6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c91b6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c91b6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c91b6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c91b6-107">DESCRIPTION</span></span>
<span data-ttu-id="c91b6-108">Командлет **Get-AzDataShareSynchronizationDetail** содержит подробные сведения о синхронизации, инициированной для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c91b6-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="c91b6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c91b6-109">EXAMPLES</span></span>

### <span data-ttu-id="c91b6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c91b6-110">Example 1</span></span>
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

<span data-ttu-id="c91b6-111">Эта команда предоставляет сведения о синхронизации всех наборов данных, соответствующих указанному идентификатору синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c91b6-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="c91b6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c91b6-112">PARAMETERS</span></span>

### <span data-ttu-id="c91b6-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="c91b6-113">-AccountName</span></span>
<span data-ttu-id="c91b6-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="c91b6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c91b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91b6-115">-DefaultProfile</span></span>
<span data-ttu-id="c91b6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c91b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c91b6-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="c91b6-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c91b6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c91b6-119">-ResourceId</span></span>
<span data-ttu-id="c91b6-120">Идентификатор ресурса "общий доступ к данным Azure"</span><span class="sxs-lookup"><span data-stu-id="c91b6-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="c91b6-121">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c91b6-121">-ShareName</span></span>
<span data-ttu-id="c91b6-122">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="c91b6-122">Azure data share name</span></span>

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

### <span data-ttu-id="c91b6-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="c91b6-123">-SynchronizationId</span></span>
<span data-ttu-id="c91b6-124">Идентификатор синхронизации для синхронизации общего доступа</span><span class="sxs-lookup"><span data-stu-id="c91b6-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="c91b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91b6-125">CommonParameters</span></span>
<span data-ttu-id="c91b6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c91b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91b6-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c91b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91b6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c91b6-128">INPUTS</span></span>

### <span data-ttu-id="c91b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c91b6-129">System.String</span></span>

## <span data-ttu-id="c91b6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c91b6-130">OUTPUTS</span></span>

### <span data-ttu-id="c91b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="c91b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="c91b6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c91b6-132">NOTES</span></span>

## <span data-ttu-id="c91b6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c91b6-133">RELATED LINKS</span></span>
