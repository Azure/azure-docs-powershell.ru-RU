---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: f081d403a47f457c48320238436d72ca4ebd15fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900586"
---
# <span data-ttu-id="c0d23-101">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="c0d23-101">Remove-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="c0d23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0d23-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d23-103">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="c0d23-103">Remove WAF policy</span></span>

## <span data-ttu-id="c0d23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0d23-104">SYNTAX</span></span>

### <span data-ttu-id="c0d23-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0d23-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d23-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d23-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d23-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d23-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d23-109">Командлет **Remove-AzFrontDoorFireWallPolicy** УДАЛЯЕТ политику WAF в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c0d23-109">The **Remove-AzFrontDoorFireWallPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="c0d23-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0d23-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d23-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0d23-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="c0d23-112">Удалите политику WAF с именем $policyName в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="c0d23-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="c0d23-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0d23-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorFireWallPolicy
```

<span data-ttu-id="c0d23-114">Удалите все WAF политики в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="c0d23-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="c0d23-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0d23-115">PARAMETERS</span></span>

### <span data-ttu-id="c0d23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d23-116">-DefaultProfile</span></span>
<span data-ttu-id="c0d23-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d23-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d23-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0d23-118">-InputObject</span></span>
<span data-ttu-id="c0d23-119">Объект политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0d23-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0d23-120">-Name</span></span>
<span data-ttu-id="c0d23-121">Имя удаляемой политики WAF.</span><span class="sxs-lookup"><span data-stu-id="c0d23-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="c0d23-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0d23-122">-PassThru</span></span>
<span data-ttu-id="c0d23-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="c0d23-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="c0d23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d23-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0d23-125">Группа ресурсов, к которой относится политика WAF.</span><span class="sxs-lookup"><span data-stu-id="c0d23-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="c0d23-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d23-126">-ResourceId</span></span>
<span data-ttu-id="c0d23-127">Идентификатор ресурса политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0d23-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="c0d23-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0d23-128">-Confirm</span></span>
<span data-ttu-id="c0d23-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0d23-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d23-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d23-130">-WhatIf</span></span>
<span data-ttu-id="c0d23-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0d23-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0d23-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0d23-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d23-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d23-133">CommonParameters</span></span>
<span data-ttu-id="c0d23-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0d23-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d23-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0d23-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d23-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0d23-136">INPUTS</span></span>

### <span data-ttu-id="c0d23-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c0d23-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="c0d23-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d23-138">System.String</span></span>

## <span data-ttu-id="c0d23-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d23-139">OUTPUTS</span></span>

### <span data-ttu-id="c0d23-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0d23-140">System.Boolean</span></span>

## <span data-ttu-id="c0d23-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0d23-141">NOTES</span></span>

## <span data-ttu-id="c0d23-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0d23-142">RELATED LINKS</span></span>

<span data-ttu-id="c0d23-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c0d23-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span></span>
