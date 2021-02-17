---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: b1c77b2a00f460e6d05483037a46e5472a25d266
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403040"
---
# <span data-ttu-id="9ca0a-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9ca0a-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="9ca0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca0a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca0a-103">Удаляет группу действий.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-103">Removes an action group.</span></span>

## <span data-ttu-id="9ca0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ca0a-104">SYNTAX</span></span>

### <span data-ttu-id="9ca0a-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ca0a-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca0a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca0a-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca0a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ca0a-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca0a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca0a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca0a-109">При **этом удаляется** группа действий.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="9ca0a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ca0a-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca0a-111">Пример 1. Удаление группы действий</span><span class="sxs-lookup"><span data-stu-id="9ca0a-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="9ca0a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ca0a-112">PARAMETERS</span></span>

### <span data-ttu-id="9ca0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca0a-113">-DefaultProfile</span></span>
<span data-ttu-id="9ca0a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ca0a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ca0a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca0a-115">-InputObject</span></span>
<span data-ttu-id="9ca0a-116">Resourc группы действий</span><span class="sxs-lookup"><span data-stu-id="9ca0a-116">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca0a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ca0a-117">-Name</span></span>
<span data-ttu-id="9ca0a-118">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ca0a-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ca0a-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca0a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca0a-121">-ResourceId</span></span>
<span data-ttu-id="9ca0a-122">Ресурс i</span><span class="sxs-lookup"><span data-stu-id="9ca0a-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca0a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ca0a-123">-Confirm</span></span>
<span data-ttu-id="9ca0a-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca0a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca0a-125">-WhatIf</span></span>
<span data-ttu-id="9ca0a-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ca0a-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca0a-128">CommonParameters</span></span>
<span data-ttu-id="9ca0a-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca0a-130">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca0a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ca0a-131">INPUTS</span></span>

### <span data-ttu-id="9ca0a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9ca0a-132">System.String</span></span>

### <span data-ttu-id="9ca0a-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9ca0a-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9ca0a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ca0a-134">OUTPUTS</span></span>

### <span data-ttu-id="9ca0a-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ca0a-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9ca0a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ca0a-136">NOTES</span></span>

## <span data-ttu-id="9ca0a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ca0a-137">RELATED LINKS</span></span>

<span data-ttu-id="9ca0a-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="9ca0a-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

