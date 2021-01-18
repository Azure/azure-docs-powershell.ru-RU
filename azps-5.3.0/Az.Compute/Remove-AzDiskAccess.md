---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519557"
---
# <span data-ttu-id="f655f-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f655f-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="f655f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f655f-102">SYNOPSIS</span></span>
<span data-ttu-id="f655f-103">Удаляет ресурс доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="f655f-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="f655f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f655f-104">SYNTAX</span></span>

### <span data-ttu-id="f655f-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f655f-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f655f-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="f655f-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f655f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f655f-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f655f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f655f-108">DESCRIPTION</span></span>
<span data-ttu-id="f655f-109">Для удаления ресурса доступа к диску удаляется cmdlet **Remove-AzDiskAccess.**</span><span class="sxs-lookup"><span data-stu-id="f655f-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="f655f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f655f-110">EXAMPLES</span></span>

### <span data-ttu-id="f655f-111">Пример 1. Удаление дискового доступа с помощью набора параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f655f-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="f655f-112">Эта команда удаляет дисковый доступ с именем "DiskAccess01" в группе ресурсов "Группа ресурсов01"</span><span class="sxs-lookup"><span data-stu-id="f655f-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="f655f-113">Пример 2. Удаление дискового доступа с помощью ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f655f-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="f655f-114">Эта команда удаляет доступ к диску по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f655f-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="f655f-115">Пример 3. Удаление диска с помощью объекта ввода</span><span class="sxs-lookup"><span data-stu-id="f655f-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="f655f-116">Эта команда удаляет доступ к диску с помощью InputObject.</span><span class="sxs-lookup"><span data-stu-id="f655f-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="f655f-117">Пример 4. Удаление доступа к диску путем с помощью piping Input Object</span><span class="sxs-lookup"><span data-stu-id="f655f-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="f655f-118">Эта команда удаляет доступ к диску путем перенакручки inputObject.</span><span class="sxs-lookup"><span data-stu-id="f655f-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="f655f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f655f-119">PARAMETERS</span></span>

### <span data-ttu-id="f655f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f655f-120">-AsJob</span></span>
<span data-ttu-id="f655f-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f655f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f655f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f655f-122">-DefaultProfile</span></span>
<span data-ttu-id="f655f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f655f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f655f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f655f-124">-InputObject</span></span>
<span data-ttu-id="f655f-125">Объект Диска PowerShell</span><span class="sxs-lookup"><span data-stu-id="f655f-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f655f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f655f-126">-Name</span></span>
<span data-ttu-id="f655f-127">Указывает имя дискового доступа.</span><span class="sxs-lookup"><span data-stu-id="f655f-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f655f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f655f-128">-ResourceGroupName</span></span>
<span data-ttu-id="f655f-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f655f-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f655f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f655f-130">-ResourceId</span></span>
<span data-ttu-id="f655f-131">ИД ресурса для доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="f655f-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f655f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f655f-132">-Confirm</span></span>
<span data-ttu-id="f655f-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f655f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f655f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f655f-134">-WhatIf</span></span>
<span data-ttu-id="f655f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f655f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f655f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f655f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f655f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f655f-137">CommonParameters</span></span>
<span data-ttu-id="f655f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f655f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f655f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f655f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f655f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f655f-140">INPUTS</span></span>

### <span data-ttu-id="f655f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f655f-141">System.String</span></span>

### <span data-ttu-id="f655f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIskAccess</span><span class="sxs-lookup"><span data-stu-id="f655f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="f655f-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f655f-143">OUTPUTS</span></span>

### <span data-ttu-id="f655f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f655f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f655f-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f655f-145">NOTES</span></span>

## <span data-ttu-id="f655f-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f655f-146">RELATED LINKS</span></span>
