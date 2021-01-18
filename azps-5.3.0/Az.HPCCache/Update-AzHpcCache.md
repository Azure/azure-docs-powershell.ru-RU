---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507266"
---
# <span data-ttu-id="86c78-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="86c78-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="86c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c78-102">SYNOPSIS</span></span>
<span data-ttu-id="86c78-103">Обновляет кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="86c78-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="86c78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86c78-104">SYNTAX</span></span>

### <span data-ttu-id="86c78-105">FlushParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86c78-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c78-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c78-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c78-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c78-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c78-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c78-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c78-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c78-109">DESCRIPTION</span></span>
<span data-ttu-id="86c78-110">Для **обновления кэша HPC обновляется cmdlet Update-AzHpcCache.**</span><span class="sxs-lookup"><span data-stu-id="86c78-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="86c78-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86c78-111">EXAMPLES</span></span>

### <span data-ttu-id="86c78-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86c78-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="86c78-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86c78-113">PARAMETERS</span></span>

### <span data-ttu-id="86c78-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86c78-114">-AsJob</span></span>
<span data-ttu-id="86c78-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="86c78-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86c78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c78-116">-DefaultProfile</span></span>
<span data-ttu-id="86c78-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86c78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c78-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="86c78-118">-Flush</span></span>
<span data-ttu-id="86c78-119">Очистка кэша HPC.</span><span class="sxs-lookup"><span data-stu-id="86c78-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c78-120">-Force</span><span class="sxs-lookup"><span data-stu-id="86c78-120">-Force</span></span>
<span data-ttu-id="86c78-121">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="86c78-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="86c78-122">По умолчанию этот cmdlet запросит подтверждение обновления кэша.</span><span class="sxs-lookup"><span data-stu-id="86c78-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="86c78-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c78-123">-InputObject</span></span>
<span data-ttu-id="86c78-124">Обновляемый объект кэша.</span><span class="sxs-lookup"><span data-stu-id="86c78-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c78-125">-Name</span><span class="sxs-lookup"><span data-stu-id="86c78-125">-Name</span></span>
<span data-ttu-id="86c78-126">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="86c78-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c78-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c78-127">-PassThru</span></span>
<span data-ttu-id="86c78-128">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="86c78-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86c78-129">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="86c78-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86c78-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c78-130">-ResourceGroupName</span></span>
<span data-ttu-id="86c78-131">Имя группы ресурсов, под которой вы хотите обновить кэш.</span><span class="sxs-lookup"><span data-stu-id="86c78-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="86c78-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86c78-132">-ResourceId</span></span>
<span data-ttu-id="86c78-133">ИД ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="86c78-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="86c78-134">-Обновление</span><span class="sxs-lookup"><span data-stu-id="86c78-134">-Upgrade</span></span>
<span data-ttu-id="86c78-135">Обновив HpcCache.</span><span class="sxs-lookup"><span data-stu-id="86c78-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c78-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86c78-136">-Confirm</span></span>
<span data-ttu-id="86c78-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c78-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c78-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c78-138">-WhatIf</span></span>
<span data-ttu-id="86c78-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c78-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86c78-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86c78-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c78-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c78-141">CommonParameters</span></span>
<span data-ttu-id="86c78-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c78-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c78-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86c78-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c78-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86c78-144">INPUTS</span></span>

### <span data-ttu-id="86c78-145">System.String</span><span class="sxs-lookup"><span data-stu-id="86c78-145">System.String</span></span>

## <span data-ttu-id="86c78-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86c78-146">OUTPUTS</span></span>

## <span data-ttu-id="86c78-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86c78-147">NOTES</span></span>

## <span data-ttu-id="86c78-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c78-148">RELATED LINKS</span></span>
