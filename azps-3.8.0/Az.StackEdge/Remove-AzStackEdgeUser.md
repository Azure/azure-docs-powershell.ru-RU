---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073903"
---
# <span data-ttu-id="5d862-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="5d862-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="5d862-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d862-102">SYNOPSIS</span></span>
<span data-ttu-id="5d862-103">Удаление пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5d862-103">Removes a user on a device.</span></span>

## <span data-ttu-id="5d862-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d862-104">SYNTAX</span></span>

### <span data-ttu-id="5d862-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d862-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d862-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d862-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d862-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d862-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d862-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d862-108">DESCRIPTION</span></span>
<span data-ttu-id="5d862-109">Командлет **Remove-AzStackEdgeUser** удаляет пользователя на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="5d862-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="5d862-110">Поддерживается создание только пользователей типа `Share` .</span><span class="sxs-lookup"><span data-stu-id="5d862-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="5d862-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d862-111">EXAMPLES</span></span>

### <span data-ttu-id="5d862-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d862-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="5d862-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d862-113">PARAMETERS</span></span>

### <span data-ttu-id="5d862-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d862-114">-AsJob</span></span>
<span data-ttu-id="5d862-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5d862-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d862-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d862-116">-DefaultProfile</span></span>
<span data-ttu-id="5d862-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d862-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d862-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="5d862-118">-DeviceName</span></span>
<span data-ttu-id="5d862-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="5d862-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d862-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d862-120">-InputObject</span></span>
<span data-ttu-id="5d862-121">Объект input</span><span class="sxs-lookup"><span data-stu-id="5d862-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d862-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d862-122">-Name</span></span>
<span data-ttu-id="5d862-123">Действительно</span><span class="sxs-lookup"><span data-stu-id="5d862-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d862-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d862-124">-PassThru</span></span>
<span data-ttu-id="5d862-125">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="5d862-125">returns true if successful</span></span>

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

### <span data-ttu-id="5d862-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d862-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d862-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5d862-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d862-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d862-128">-ResourceId</span></span>
<span data-ttu-id="5d862-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d862-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d862-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d862-130">-Confirm</span></span>
<span data-ttu-id="5d862-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d862-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d862-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d862-132">-WhatIf</span></span>
<span data-ttu-id="5d862-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d862-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d862-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d862-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d862-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d862-135">CommonParameters</span></span>
<span data-ttu-id="5d862-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d862-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d862-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d862-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d862-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d862-138">INPUTS</span></span>

### <span data-ttu-id="5d862-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5d862-139">System.String</span></span>

### <span data-ttu-id="5d862-140">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="5d862-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="5d862-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d862-141">OUTPUTS</span></span>

### <span data-ttu-id="5d862-142">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5d862-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5d862-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d862-143">NOTES</span></span>

## <span data-ttu-id="5d862-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d862-144">RELATED LINKS</span></span>
