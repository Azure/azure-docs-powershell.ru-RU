---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231868"
---
# <span data-ttu-id="cb291-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="cb291-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="cb291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb291-102">SYNOPSIS</span></span>
<span data-ttu-id="cb291-103">Повторно сгенерировать ключ доступа для службы signalr.</span><span class="sxs-lookup"><span data-stu-id="cb291-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="cb291-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb291-104">SYNTAX</span></span>

### <span data-ttu-id="cb291-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb291-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb291-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb291-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb291-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb291-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb291-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb291-108">DESCRIPTION</span></span>
<span data-ttu-id="cb291-109">Повторно сгенерировать ключ доступа для службы signalr.</span><span class="sxs-lookup"><span data-stu-id="cb291-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="cb291-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb291-110">EXAMPLES</span></span>

### <span data-ttu-id="cb291-111">Повторное сгенерировать первичный ключ</span><span class="sxs-lookup"><span data-stu-id="cb291-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="cb291-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb291-112">PARAMETERS</span></span>

### <span data-ttu-id="cb291-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb291-113">-DefaultProfile</span></span>
<span data-ttu-id="cb291-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb291-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb291-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb291-115">-InputObject</span></span>
<span data-ttu-id="cb291-116">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="cb291-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb291-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="cb291-117">-KeyType</span></span>
<span data-ttu-id="cb291-118">Тип ключа (первичный или дополнительный).</span><span class="sxs-lookup"><span data-stu-id="cb291-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb291-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cb291-119">-Name</span></span>
<span data-ttu-id="cb291-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="cb291-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb291-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb291-121">-PassThru</span></span>
<span data-ttu-id="cb291-122">Возвращается истина, если обновление завершено успешно.</span><span class="sxs-lookup"><span data-stu-id="cb291-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="cb291-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb291-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb291-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb291-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb291-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb291-125">-ResourceId</span></span>
<span data-ttu-id="cb291-126">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="cb291-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb291-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb291-127">-Confirm</span></span>
<span data-ttu-id="cb291-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb291-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb291-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb291-129">-WhatIf</span></span>
<span data-ttu-id="cb291-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb291-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb291-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb291-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb291-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb291-132">CommonParameters</span></span>
<span data-ttu-id="cb291-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb291-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb291-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb291-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb291-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb291-135">INPUTS</span></span>

### <span data-ttu-id="cb291-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cb291-136">System.String</span></span>
### <span data-ttu-id="cb291-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="cb291-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="cb291-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb291-138">OUTPUTS</span></span>

### <span data-ttu-id="cb291-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb291-139">System.Boolean</span></span>
## <span data-ttu-id="cb291-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb291-140">NOTES</span></span>

## <span data-ttu-id="cb291-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb291-141">RELATED LINKS</span></span>
