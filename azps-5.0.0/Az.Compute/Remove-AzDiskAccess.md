---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245722"
---
# <span data-ttu-id="69dc0-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="69dc0-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="69dc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="69dc0-103">Удаляет ресурс "доступ к диску".</span><span class="sxs-lookup"><span data-stu-id="69dc0-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="69dc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69dc0-104">SYNTAX</span></span>

### <span data-ttu-id="69dc0-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69dc0-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69dc0-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="69dc0-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69dc0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69dc0-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69dc0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69dc0-108">DESCRIPTION</span></span>
<span data-ttu-id="69dc0-109">Командлет **Remove-AzDiskAccess** удаляет ресурс "доступ к диску".</span><span class="sxs-lookup"><span data-stu-id="69dc0-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="69dc0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="69dc0-111">Пример 1: удаление доступа к диску с использованием стандартной настройки параметров</span><span class="sxs-lookup"><span data-stu-id="69dc0-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="69dc0-112">Эта команда удаляет доступ к диску с именем "DiskAccess01" в группе ресурсов "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="69dc0-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="69dc0-113">Пример 2: удаление доступа к диску с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="69dc0-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="69dc0-114">Эта команда удаляет доступ к диску по ИДЕНТИФИКАТОРу ресурса.</span><span class="sxs-lookup"><span data-stu-id="69dc0-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="69dc0-115">Пример 3: удаление доступа к диску с помощью объекта input</span><span class="sxs-lookup"><span data-stu-id="69dc0-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="69dc0-116">Эта команда удаляет доступ к диску через InputObject</span><span class="sxs-lookup"><span data-stu-id="69dc0-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="69dc0-117">Пример 4: удаление доступа к диску с помощью объекта ввода по конвейеру</span><span class="sxs-lookup"><span data-stu-id="69dc0-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="69dc0-118">Эта команда удаляет доступ к диску через конвейер InputObject</span><span class="sxs-lookup"><span data-stu-id="69dc0-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="69dc0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69dc0-119">PARAMETERS</span></span>

### <span data-ttu-id="69dc0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69dc0-120">-AsJob</span></span>
<span data-ttu-id="69dc0-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="69dc0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69dc0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dc0-122">-DefaultProfile</span></span>
<span data-ttu-id="69dc0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69dc0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69dc0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69dc0-124">-InputObject</span></span>
<span data-ttu-id="69dc0-125">Объект доступа к диску PowerShell</span><span class="sxs-lookup"><span data-stu-id="69dc0-125">PowerShell Disk Access Object</span></span>

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

### <span data-ttu-id="69dc0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69dc0-126">-Name</span></span>
<span data-ttu-id="69dc0-127">Указывает имя доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="69dc0-127">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="69dc0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69dc0-128">-ResourceGroupName</span></span>
<span data-ttu-id="69dc0-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69dc0-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="69dc0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69dc0-130">-ResourceId</span></span>
<span data-ttu-id="69dc0-131">Идентификатор ресурса для доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="69dc0-131">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="69dc0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69dc0-132">-Confirm</span></span>
<span data-ttu-id="69dc0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69dc0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69dc0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69dc0-134">-WhatIf</span></span>
<span data-ttu-id="69dc0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69dc0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69dc0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69dc0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69dc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dc0-137">CommonParameters</span></span>
<span data-ttu-id="69dc0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69dc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dc0-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69dc0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dc0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69dc0-140">INPUTS</span></span>

### <span data-ttu-id="69dc0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="69dc0-141">System.String</span></span>

### <span data-ttu-id="69dc0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="69dc0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="69dc0-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69dc0-143">OUTPUTS</span></span>

### <span data-ttu-id="69dc0-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="69dc0-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="69dc0-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="69dc0-145">NOTES</span></span>

## <span data-ttu-id="69dc0-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69dc0-146">RELATED LINKS</span></span>
