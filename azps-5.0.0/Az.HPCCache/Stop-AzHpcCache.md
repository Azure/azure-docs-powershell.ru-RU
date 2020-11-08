---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245349"
---
# <span data-ttu-id="e37fa-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e37fa-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="e37fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e37fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e37fa-103">Остановка кэша HPC.</span><span class="sxs-lookup"><span data-stu-id="e37fa-103">Stops HPC cache.</span></span>

## <span data-ttu-id="e37fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e37fa-104">SYNTAX</span></span>

### <span data-ttu-id="e37fa-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e37fa-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37fa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e37fa-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37fa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e37fa-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e37fa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e37fa-108">DESCRIPTION</span></span>
<span data-ttu-id="e37fa-109">Командлет **Stop-AzHpcCache** останавливает кэш Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="e37fa-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="e37fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e37fa-110">EXAMPLES</span></span>

### <span data-ttu-id="e37fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e37fa-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e37fa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e37fa-112">PARAMETERS</span></span>

### <span data-ttu-id="e37fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37fa-113">-DefaultProfile</span></span>
<span data-ttu-id="e37fa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e37fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e37fa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e37fa-115">-Force</span></span>
<span data-ttu-id="e37fa-116">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e37fa-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e37fa-117">По умолчанию этот командлет предлагает подтвердить, что вы хотите остановить кэш.</span><span class="sxs-lookup"><span data-stu-id="e37fa-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="e37fa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e37fa-118">-InputObject</span></span>
<span data-ttu-id="e37fa-119">Объект кэша, который нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="e37fa-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="e37fa-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e37fa-120">-Name</span></span>
<span data-ttu-id="e37fa-121">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="e37fa-121">Name of cache.</span></span>

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

### <span data-ttu-id="e37fa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e37fa-122">-PassThru</span></span>
<span data-ttu-id="e37fa-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e37fa-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e37fa-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e37fa-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e37fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e37fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="e37fa-126">Имя группы ресурсов, в которой вы хотите остановить кэширование.</span><span class="sxs-lookup"><span data-stu-id="e37fa-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="e37fa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e37fa-127">-ResourceId</span></span>
<span data-ttu-id="e37fa-128">Идентификатор ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="e37fa-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e37fa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e37fa-129">-Confirm</span></span>
<span data-ttu-id="e37fa-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e37fa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e37fa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e37fa-131">-WhatIf</span></span>
<span data-ttu-id="e37fa-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e37fa-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e37fa-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e37fa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e37fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37fa-134">CommonParameters</span></span>
<span data-ttu-id="e37fa-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e37fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37fa-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e37fa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37fa-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e37fa-137">INPUTS</span></span>

### <span data-ttu-id="e37fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e37fa-138">System.String</span></span>

## <span data-ttu-id="e37fa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e37fa-139">OUTPUTS</span></span>

## <span data-ttu-id="e37fa-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e37fa-140">NOTES</span></span>

## <span data-ttu-id="e37fa-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e37fa-141">RELATED LINKS</span></span>
