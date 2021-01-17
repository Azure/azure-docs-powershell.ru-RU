---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420911"
---
# <span data-ttu-id="b4b9f-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b4b9f-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="b4b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b9f-103">Удаление решения для обеспечения безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="b4b9f-103">Delete IoT security solution</span></span>

## <span data-ttu-id="b4b9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4b9f-104">SYNTAX</span></span>

### <span data-ttu-id="b4b9f-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4b9f-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b9f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4b9f-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b9f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4b9f-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b9f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b9f-108">DESCRIPTION</span></span>
<span data-ttu-id="b4b9f-109">С Remove-AzIotSecuritySolution удаляется определенное решение для защиты iOT-данных.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="b4b9f-110">Решение для защиты IoT собирает данные безопасности и события с устройств iot и iot-концентратора для предотвращения и обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="b4b9f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4b9f-111">EXAMPLES</span></span>

### <span data-ttu-id="b4b9f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4b9f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b4b9f-113">Удаление решения безопасности IoT "MySample" с группой ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="b4b9f-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="b4b9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="b4b9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b9f-115">-DefaultProfile</span></span>
<span data-ttu-id="b4b9f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4b9f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4b9f-117">-InputObject</span></span>
<span data-ttu-id="b4b9f-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b9f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b4b9f-119">-Name</span></span>
<span data-ttu-id="b4b9f-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b9f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4b9f-121">-PassThru</span></span>
<span data-ttu-id="b4b9f-122">Возвращает, была ли операция успешной.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b4b9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4b9f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b9f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4b9f-125">-ResourceId</span></span>
<span data-ttu-id="b4b9f-126">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b9f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4b9f-127">-Confirm</span></span>
<span data-ttu-id="b4b9f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b9f-129">-WhatIf</span></span>
<span data-ttu-id="b4b9f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b9f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b9f-132">CommonParameters</span></span>
<span data-ttu-id="b4b9f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b9f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4b9f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b9f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b9f-135">INPUTS</span></span>

### <span data-ttu-id="b4b9f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b4b9f-136">System.String</span></span>

### <span data-ttu-id="b4b9f-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b4b9f-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="b4b9f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b9f-138">OUTPUTS</span></span>

### <span data-ttu-id="b4b9f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4b9f-139">System.Boolean</span></span>

## <span data-ttu-id="b4b9f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4b9f-140">NOTES</span></span>

## <span data-ttu-id="b4b9f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4b9f-141">RELATED LINKS</span></span>
