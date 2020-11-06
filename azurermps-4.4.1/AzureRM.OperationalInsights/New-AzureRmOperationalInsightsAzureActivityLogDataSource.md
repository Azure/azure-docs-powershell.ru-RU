---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565204"
---
# <span data-ttu-id="1e6fd-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="1e6fd-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="1e6fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6fd-103">Сбор журнала активности Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e6fd-104">SYNTAX</span></span>

### <span data-ttu-id="1e6fd-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e6fd-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e6fd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e6fd-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6fd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="1e6fd-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource включения аналитики журнала для сбора журнала активности Azure из данной подписки.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="1e6fd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e6fd-109">EXAMPLES</span></span>

### <span data-ttu-id="1e6fd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e6fd-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1e6fd-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="1e6fd-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1e6fd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e6fd-112">PARAMETERS</span></span>

### <span data-ttu-id="1e6fd-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="1e6fd-113">-BackfillStartTime</span></span>
<span data-ttu-id="1e6fd-114">Вы можете отказаться от записи журнала за неделю назад.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1e6fd-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e6fd-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6fd-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e6fd-118">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-119">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="1e6fd-119">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e6fd-120">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e6fd-121">-Confirm</span></span>
<span data-ttu-id="1e6fd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6fd-123">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6fd-124">-DefaultProfile</span></span>
<span data-ttu-id="1e6fd-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6fd-126">CommonParameters</span></span>
<span data-ttu-id="1e6fd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6fd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6fd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e6fd-129">INPUTS</span></span>

### <span data-ttu-id="1e6fd-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e6fd-130">PSWorkspace</span></span>
<span data-ttu-id="1e6fd-131">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1e6fd-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1e6fd-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e6fd-132">OUTPUTS</span></span>

### <span data-ttu-id="1e6fd-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1e6fd-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1e6fd-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e6fd-134">NOTES</span></span>

## <span data-ttu-id="1e6fd-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e6fd-135">RELATED LINKS</span></span>

