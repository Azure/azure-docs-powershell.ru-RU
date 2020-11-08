---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243975"
---
# <span data-ttu-id="d785b-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d785b-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="d785b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d785b-102">SYNOPSIS</span></span>
<span data-ttu-id="d785b-103">Удаление решения для обеспечения безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="d785b-103">Delete IoT security solution</span></span>

## <span data-ttu-id="d785b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d785b-104">SYNTAX</span></span>

### <span data-ttu-id="d785b-105">ResourceGroupLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d785b-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d785b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d785b-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d785b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d785b-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d785b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d785b-108">DESCRIPTION</span></span>
<span data-ttu-id="d785b-109">Командлет Remove-AzIotSecuritySolution удаляет конкретное решение для безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="d785b-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="d785b-110">Решение для обеспечения безопасности IoT собирает данные о безопасности и события на устройствах Интернет вещей и центре Интернета, которые помогают предотвратить и обнаруживать угрозы.</span><span class="sxs-lookup"><span data-stu-id="d785b-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="d785b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d785b-111">EXAMPLES</span></span>

### <span data-ttu-id="d785b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d785b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d785b-113">Удаление решения для безопасности IoT "MySample" с группой ресурсов "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="d785b-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d785b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d785b-114">PARAMETERS</span></span>

### <span data-ttu-id="d785b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d785b-115">-DefaultProfile</span></span>
<span data-ttu-id="d785b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d785b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d785b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d785b-117">-InputObject</span></span>
<span data-ttu-id="d785b-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="d785b-118">Input Object.</span></span>

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

### <span data-ttu-id="d785b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d785b-119">-Name</span></span>
<span data-ttu-id="d785b-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d785b-120">Resource name.</span></span>

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

### <span data-ttu-id="d785b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d785b-121">-PassThru</span></span>
<span data-ttu-id="d785b-122">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d785b-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d785b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d785b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d785b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d785b-124">Resource group name.</span></span>

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

### <span data-ttu-id="d785b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d785b-125">-ResourceId</span></span>
<span data-ttu-id="d785b-126">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="d785b-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d785b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d785b-127">-Confirm</span></span>
<span data-ttu-id="d785b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d785b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d785b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d785b-129">-WhatIf</span></span>
<span data-ttu-id="d785b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d785b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d785b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d785b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d785b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d785b-132">CommonParameters</span></span>
<span data-ttu-id="d785b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d785b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d785b-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d785b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d785b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d785b-135">INPUTS</span></span>

### <span data-ttu-id="d785b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d785b-136">System.String</span></span>

### <span data-ttu-id="d785b-137">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d785b-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="d785b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d785b-138">OUTPUTS</span></span>

### <span data-ttu-id="d785b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d785b-139">System.Boolean</span></span>

## <span data-ttu-id="d785b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d785b-140">NOTES</span></span>

## <span data-ttu-id="d785b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d785b-141">RELATED LINKS</span></span>
