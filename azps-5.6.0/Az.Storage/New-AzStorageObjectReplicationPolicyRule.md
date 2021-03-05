---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002440"
---
# <span data-ttu-id="a6aac-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a6aac-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a6aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6aac-102">SYNOPSIS</span></span>
<span data-ttu-id="a6aac-103">Создает правило политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="a6aac-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="a6aac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6aac-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6aac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6aac-105">DESCRIPTION</span></span>
<span data-ttu-id="a6aac-106">Для создания правила политики репликации объектов используется Set-AzStorageObjectReplicationPolicy **Get-AzStorageObjectReplicationPolicy.**</span><span class="sxs-lookup"><span data-stu-id="a6aac-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="a6aac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6aac-107">EXAMPLES</span></span>

### <span data-ttu-id="a6aac-108">Пример 1. Создание правила политики репликации объектов с только учетной записью источника и назначения и его свойства</span><span class="sxs-lookup"><span data-stu-id="a6aac-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="a6aac-109">Эта команда создает правило политики репликации объектов с только учетной записью источника и назначения и показывает его свойства.</span><span class="sxs-lookup"><span data-stu-id="a6aac-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="a6aac-110">Пример 2. Создание правила политики репликации объектов со всеми свойствами и его показ свойств</span><span class="sxs-lookup"><span data-stu-id="a6aac-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="a6aac-111">Эта команда для правила политики репликации объектов со всеми свойствами и его свойствами.</span><span class="sxs-lookup"><span data-stu-id="a6aac-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="a6aac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6aac-112">PARAMETERS</span></span>

### <span data-ttu-id="a6aac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6aac-113">-DefaultProfile</span></span>
<span data-ttu-id="a6aac-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6aac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6aac-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="a6aac-115">-DestinationContainer</span></span>
<span data-ttu-id="a6aac-116">Имя реплицируемых контейнеров.</span><span class="sxs-lookup"><span data-stu-id="a6aac-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="a6aac-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="a6aac-117">-MinCreationTime</span></span>
<span data-ttu-id="a6aac-118">BLOB-группы, созданные после этого времени, будут реплицированы в место назначения.</span><span class="sxs-lookup"><span data-stu-id="a6aac-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6aac-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="a6aac-119">-PrefixMatch</span></span>
<span data-ttu-id="a6aac-120">Фильтрует результаты, чтобы реплицировать только BLOB-группы, имена которых начинаются с указанного префикса.</span><span class="sxs-lookup"><span data-stu-id="a6aac-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6aac-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a6aac-121">-RuleId</span></span>
<span data-ttu-id="a6aac-122">ИД правила репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="a6aac-122">Object Replication Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6aac-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="a6aac-123">-SourceContainer</span></span>
<span data-ttu-id="a6aac-124">Имя контейнера источника, из которого нужно реплицировать.</span><span class="sxs-lookup"><span data-stu-id="a6aac-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="a6aac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6aac-125">CommonParameters</span></span>
<span data-ttu-id="a6aac-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6aac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6aac-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6aac-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6aac-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6aac-128">INPUTS</span></span>

### <span data-ttu-id="a6aac-129">Нет</span><span class="sxs-lookup"><span data-stu-id="a6aac-129">None</span></span>

## <span data-ttu-id="a6aac-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6aac-130">OUTPUTS</span></span>

### <span data-ttu-id="a6aac-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a6aac-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a6aac-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6aac-132">NOTES</span></span>

## <span data-ttu-id="a6aac-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6aac-133">RELATED LINKS</span></span>
