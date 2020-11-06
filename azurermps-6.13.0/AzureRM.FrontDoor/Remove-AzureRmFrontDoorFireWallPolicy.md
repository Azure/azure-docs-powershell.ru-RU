---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556632"
---
# <span data-ttu-id="22b44-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="22b44-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="22b44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22b44-102">SYNOPSIS</span></span>
<span data-ttu-id="22b44-103">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="22b44-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22b44-104">SYNTAX</span></span>

### <span data-ttu-id="22b44-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22b44-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b44-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22b44-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b44-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22b44-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b44-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22b44-108">DESCRIPTION</span></span>
<span data-ttu-id="22b44-109">Командлет **Remove-AzureRmFrontDoor** УДАЛЯЕТ политику WAF в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="22b44-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="22b44-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22b44-110">EXAMPLES</span></span>

### <span data-ttu-id="22b44-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22b44-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="22b44-112">Удалите политику WAF с именем $name в $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22b44-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="22b44-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="22b44-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="22b44-114">Удалите все WAF политики в $resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22b44-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="22b44-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22b44-115">PARAMETERS</span></span>

### <span data-ttu-id="22b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b44-116">-DefaultProfile</span></span>
<span data-ttu-id="22b44-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22b44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22b44-118">-InputObject</span></span>
<span data-ttu-id="22b44-119">Объект политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22b44-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="22b44-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22b44-120">-Name</span></span>
<span data-ttu-id="22b44-121">Имя удаляемой политики WAF.</span><span class="sxs-lookup"><span data-stu-id="22b44-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="22b44-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22b44-122">-PassThru</span></span>
<span data-ttu-id="22b44-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="22b44-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="22b44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b44-124">-ResourceGroupName</span></span>
<span data-ttu-id="22b44-125">Группа ресурсов, к которой относится политика WAF.</span><span class="sxs-lookup"><span data-stu-id="22b44-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="22b44-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22b44-126">-ResourceId</span></span>
<span data-ttu-id="22b44-127">Идентификатор ресурса политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22b44-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b44-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22b44-128">-Confirm</span></span>
<span data-ttu-id="22b44-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22b44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b44-130">-WhatIf</span></span>
<span data-ttu-id="22b44-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22b44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b44-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22b44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b44-133">CommonParameters</span></span>
<span data-ttu-id="22b44-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22b44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b44-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b44-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b44-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22b44-136">INPUTS</span></span>

### <span data-ttu-id="22b44-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="22b44-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="22b44-138">System. String</span><span class="sxs-lookup"><span data-stu-id="22b44-138">System.String</span></span>

### <span data-ttu-id="22b44-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22b44-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22b44-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22b44-140">OUTPUTS</span></span>

### <span data-ttu-id="22b44-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22b44-141">System.Boolean</span></span>

## <span data-ttu-id="22b44-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="22b44-142">NOTES</span></span>

## <span data-ttu-id="22b44-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22b44-143">RELATED LINKS</span></span>

<span data-ttu-id="22b44-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="22b44-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
