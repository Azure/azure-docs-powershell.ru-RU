---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404455"
---
# <span data-ttu-id="7ebb6-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7ebb6-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="7ebb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ebb6-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebb6-103">Удаляет пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-103">Removes a user on a device.</span></span>

## <span data-ttu-id="7ebb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ebb6-104">SYNTAX</span></span>

### <span data-ttu-id="7ebb6-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ebb6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebb6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ebb6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebb6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ebb6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebb6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ebb6-108">DESCRIPTION</span></span>
<span data-ttu-id="7ebb6-109">С **его учетной** записи удаляется пользователь с устройства Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="7ebb6-110">Поддерживается создание только пользователей `Share` разных типов.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="7ebb6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ebb6-111">EXAMPLES</span></span>

### <span data-ttu-id="7ebb6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ebb6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="7ebb6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ebb6-113">PARAMETERS</span></span>

### <span data-ttu-id="7ebb6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ebb6-114">-AsJob</span></span>
<span data-ttu-id="7ebb6-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ebb6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ebb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebb6-116">-DefaultProfile</span></span>
<span data-ttu-id="7ebb6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ebb6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7ebb6-118">-DeviceName</span></span>
<span data-ttu-id="7ebb6-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7ebb6-119">Device Name</span></span>

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

### <span data-ttu-id="7ebb6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ebb6-120">-InputObject</span></span>
<span data-ttu-id="7ebb6-121">Объект Input</span><span class="sxs-lookup"><span data-stu-id="7ebb6-121">Input Object</span></span>

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

### <span data-ttu-id="7ebb6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7ebb6-122">-Name</span></span>
<span data-ttu-id="7ebb6-123">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="7ebb6-123">Username</span></span>

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

### <span data-ttu-id="7ebb6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ebb6-124">-PassThru</span></span>
<span data-ttu-id="7ebb6-125">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-125">returns true if successful</span></span>

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

### <span data-ttu-id="7ebb6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebb6-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ebb6-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7ebb6-127">Resource Group Name</span></span>

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

### <span data-ttu-id="7ebb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ebb6-128">-ResourceId</span></span>
<span data-ttu-id="7ebb6-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ebb6-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="7ebb6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ebb6-130">-Confirm</span></span>
<span data-ttu-id="7ebb6-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebb6-132">-WhatIf</span></span>
<span data-ttu-id="7ebb6-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ebb6-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebb6-135">CommonParameters</span></span>
<span data-ttu-id="7ebb6-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebb6-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ebb6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebb6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ebb6-138">INPUTS</span></span>

### <span data-ttu-id="7ebb6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7ebb6-139">System.String</span></span>

### <span data-ttu-id="7ebb6-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7ebb6-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="7ebb6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ebb6-141">OUTPUTS</span></span>

### <span data-ttu-id="7ebb6-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7ebb6-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7ebb6-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ebb6-143">NOTES</span></span>

## <span data-ttu-id="7ebb6-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ebb6-144">RELATED LINKS</span></span>
