---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236541"
---
# <span data-ttu-id="1f67c-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1f67c-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="1f67c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f67c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f67c-103">Создание правила политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="1f67c-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="1f67c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f67c-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f67c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f67c-105">DESCRIPTION</span></span>
<span data-ttu-id="1f67c-106">Командлет **Get-AzStorageObjectReplicationPolicy** создает правило политики репликации объектов, которое будет использоваться в командлете Set-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="1f67c-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="1f67c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f67c-107">EXAMPLES</span></span>

### <span data-ttu-id="1f67c-108">Пример 1: Создание правила политики репликации объектов с использованием только исходной и конечной учетной записи и отображение его свойств</span><span class="sxs-lookup"><span data-stu-id="1f67c-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="1f67c-109">Эта команда создает правило политики репликации объектов, которое имеет только исходную и конечную учетную запись, и отображает ее свойства.</span><span class="sxs-lookup"><span data-stu-id="1f67c-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="1f67c-110">Пример 2: Создание правила политики репликации объектов со всеми свойствами и отображение его свойств</span><span class="sxs-lookup"><span data-stu-id="1f67c-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="1f67c-111">В этой команде правило политики репликации объектов со всеми свойствами и отображаются его свойства.</span><span class="sxs-lookup"><span data-stu-id="1f67c-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="1f67c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f67c-112">PARAMETERS</span></span>

### <span data-ttu-id="1f67c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f67c-113">-DefaultProfile</span></span>
<span data-ttu-id="1f67c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f67c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f67c-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="1f67c-115">-DestinationContainer</span></span>
<span data-ttu-id="1f67c-116">Имя целевого контейнера для репликации.</span><span class="sxs-lookup"><span data-stu-id="1f67c-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="1f67c-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="1f67c-117">-MinCreationTime</span></span>
<span data-ttu-id="1f67c-118">Большие двоичные объекты, созданные после того, как будут реплицированы во время назначения.</span><span class="sxs-lookup"><span data-stu-id="1f67c-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="1f67c-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="1f67c-119">-PrefixMatch</span></span>
<span data-ttu-id="1f67c-120">Фильтрует результаты для репликации только больших двоичных объектов, имена которых начинаются с указанного префикса.</span><span class="sxs-lookup"><span data-stu-id="1f67c-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="1f67c-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="1f67c-121">-RuleId</span></span>
<span data-ttu-id="1f67c-122">Идентификатор правила репликации объекта.</span><span class="sxs-lookup"><span data-stu-id="1f67c-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="1f67c-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="1f67c-123">-SourceContainer</span></span>
<span data-ttu-id="1f67c-124">Имя исходного контейнера для репликации.</span><span class="sxs-lookup"><span data-stu-id="1f67c-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="1f67c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f67c-125">CommonParameters</span></span>
<span data-ttu-id="1f67c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f67c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f67c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f67c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f67c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f67c-128">INPUTS</span></span>

### <span data-ttu-id="1f67c-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="1f67c-129">None</span></span>

## <span data-ttu-id="1f67c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f67c-130">OUTPUTS</span></span>

### <span data-ttu-id="1f67c-131">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1f67c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="1f67c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f67c-132">NOTES</span></span>

## <span data-ttu-id="1f67c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f67c-133">RELATED LINKS</span></span>
