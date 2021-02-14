---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237743"
---
# <span data-ttu-id="d3a67-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d3a67-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="d3a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a67-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a67-103">Останавливает кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="d3a67-103">Stops HPC cache.</span></span>

## <span data-ttu-id="d3a67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3a67-104">SYNTAX</span></span>

### <span data-ttu-id="d3a67-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3a67-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a67-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a67-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a67-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a67-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a67-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a67-108">DESCRIPTION</span></span>
<span data-ttu-id="d3a67-109">При **этом кэш HPC Azure** останавливается.</span><span class="sxs-lookup"><span data-stu-id="d3a67-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="d3a67-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3a67-110">EXAMPLES</span></span>

### <span data-ttu-id="d3a67-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3a67-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="d3a67-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a67-112">PARAMETERS</span></span>

### <span data-ttu-id="d3a67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a67-113">-DefaultProfile</span></span>
<span data-ttu-id="d3a67-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a67-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3a67-115">-Force</span></span>
<span data-ttu-id="d3a67-116">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="d3a67-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d3a67-117">По умолчанию этот cmdlet запросит подтверждение остановки кэша.</span><span class="sxs-lookup"><span data-stu-id="d3a67-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="d3a67-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3a67-118">-InputObject</span></span>
<span data-ttu-id="d3a67-119">Объект кэша, который нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="d3a67-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="d3a67-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a67-120">-Name</span></span>
<span data-ttu-id="d3a67-121">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="d3a67-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a67-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3a67-122">-PassThru</span></span>
<span data-ttu-id="d3a67-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d3a67-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3a67-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d3a67-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a67-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3a67-126">Имя группы ресурсов, для которой нужно прекратить кэш.</span><span class="sxs-lookup"><span data-stu-id="d3a67-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a67-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a67-127">-ResourceId</span></span>
<span data-ttu-id="d3a67-128">ИД ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="d3a67-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="d3a67-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3a67-129">-Confirm</span></span>
<span data-ttu-id="d3a67-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a67-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a67-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a67-131">-WhatIf</span></span>
<span data-ttu-id="d3a67-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a67-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a67-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3a67-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a67-134">CommonParameters</span></span>
<span data-ttu-id="d3a67-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a67-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a67-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a67-137">INPUTS</span></span>

### <span data-ttu-id="d3a67-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a67-138">System.String</span></span>

## <span data-ttu-id="d3a67-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a67-139">OUTPUTS</span></span>

## <span data-ttu-id="d3a67-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3a67-140">NOTES</span></span>

## <span data-ttu-id="d3a67-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3a67-141">RELATED LINKS</span></span>
