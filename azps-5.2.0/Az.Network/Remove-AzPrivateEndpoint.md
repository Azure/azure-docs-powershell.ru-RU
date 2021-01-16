---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410532"
---
# <span data-ttu-id="030c2-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="030c2-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="030c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="030c2-102">SYNOPSIS</span></span>
<span data-ttu-id="030c2-103">Удаляет частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="030c2-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="030c2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="030c2-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="030c2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="030c2-105">DESCRIPTION</span></span>
<span data-ttu-id="030c2-106">Для **удаления закрытой** конечной точки удаляется личная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="030c2-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="030c2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="030c2-107">EXAMPLES</span></span>

### <span data-ttu-id="030c2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="030c2-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="030c2-109">В этом примере удаляется частная конечная точка с именем MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="030c2-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="030c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="030c2-110">PARAMETERS</span></span>

### <span data-ttu-id="030c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="030c2-111">-AsJob</span></span>
<span data-ttu-id="030c2-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="030c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="030c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030c2-113">-DefaultProfile</span></span>
<span data-ttu-id="030c2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="030c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="030c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="030c2-115">-Force</span></span>
<span data-ttu-id="030c2-116">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="030c2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="030c2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="030c2-117">-Name</span></span>
<span data-ttu-id="030c2-118">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="030c2-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="030c2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="030c2-119">-PassThru</span></span>
<span data-ttu-id="030c2-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="030c2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="030c2-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="030c2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="030c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="030c2-123">Имя группы ресурсов закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="030c2-123">The resource group name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="030c2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="030c2-124">-Confirm</span></span>
<span data-ttu-id="030c2-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="030c2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="030c2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="030c2-126">-WhatIf</span></span>
<span data-ttu-id="030c2-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="030c2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="030c2-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="030c2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="030c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030c2-129">CommonParameters</span></span>
<span data-ttu-id="030c2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="030c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030c2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="030c2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030c2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="030c2-132">INPUTS</span></span>

### <span data-ttu-id="030c2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="030c2-133">System.String</span></span>

## <span data-ttu-id="030c2-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="030c2-134">OUTPUTS</span></span>

### <span data-ttu-id="030c2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="030c2-135">System.Boolean</span></span>

## <span data-ttu-id="030c2-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="030c2-136">NOTES</span></span>

## <span data-ttu-id="030c2-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="030c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="030c2-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="030c2-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="030c2-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="030c2-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)