---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249916"
---
# <span data-ttu-id="bb28f-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="bb28f-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="bb28f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb28f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb28f-103">Удаление группы действий.</span><span class="sxs-lookup"><span data-stu-id="bb28f-103">Removes an action group.</span></span>

## <span data-ttu-id="bb28f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb28f-104">SYNTAX</span></span>

### <span data-ttu-id="bb28f-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb28f-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb28f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb28f-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb28f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb28f-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb28f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb28f-108">DESCRIPTION</span></span>
<span data-ttu-id="bb28f-109">Командлет **Remove-AzActionGroup** удаляет группу действий.</span><span class="sxs-lookup"><span data-stu-id="bb28f-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="bb28f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb28f-110">EXAMPLES</span></span>

### <span data-ttu-id="bb28f-111">Пример 1: Удаление группы действий</span><span class="sxs-lookup"><span data-stu-id="bb28f-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="bb28f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb28f-112">PARAMETERS</span></span>

### <span data-ttu-id="bb28f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb28f-113">-DefaultProfile</span></span>
<span data-ttu-id="bb28f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb28f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb28f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb28f-115">-InputObject</span></span>
<span data-ttu-id="bb28f-116">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="bb28f-116">The action group resource</span></span>

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

### <span data-ttu-id="bb28f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb28f-117">-Name</span></span>
<span data-ttu-id="bb28f-118">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="bb28f-118">The name of the action group.</span></span>

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

### <span data-ttu-id="bb28f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb28f-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb28f-120">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="bb28f-120">The resource group nam</span></span>

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

### <span data-ttu-id="bb28f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb28f-121">-ResourceId</span></span>
<span data-ttu-id="bb28f-122">Ресурс</span><span class="sxs-lookup"><span data-stu-id="bb28f-122">The resource i</span></span>

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

### <span data-ttu-id="bb28f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb28f-123">-Confirm</span></span>
<span data-ttu-id="bb28f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb28f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb28f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb28f-125">-WhatIf</span></span>
<span data-ttu-id="bb28f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb28f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb28f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb28f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb28f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb28f-128">CommonParameters</span></span>
<span data-ttu-id="bb28f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb28f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb28f-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb28f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb28f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb28f-131">INPUTS</span></span>

### <span data-ttu-id="bb28f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bb28f-132">System.String</span></span>

### <span data-ttu-id="bb28f-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="bb28f-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="bb28f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb28f-134">OUTPUTS</span></span>

### <span data-ttu-id="bb28f-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb28f-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bb28f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb28f-136">NOTES</span></span>

## <span data-ttu-id="bb28f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb28f-137">RELATED LINKS</span></span>

<span data-ttu-id="bb28f-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="bb28f-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
